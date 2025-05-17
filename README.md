# iCare Vision Platform

> 🏆 **2nd Place Winner - SITAC 2025 Competition** 

## Vision for Vision: Affordable Eyecare for 100M+ People

iCare is a non-profit initiative committed to providing affordable prescription glasses to people with Uncorrected Refractive Error (URE), particularly targeting the 100M people and 48M children in India who cannot afford eyeglasses.

This README provides an overview of our award-winning solution developed over six months for the SITAC 2025 competition. The detailed deliverables and technical documentation are available in the repository.

## The Challenge

- Of the 7.95B world population, 4B wear eyeglasses
- 950M people globally have vision impairment from URE and cannot afford eyeglasses (100M in India)
- 239M children globally have vision impairment from URE whose families cannot afford eyeglasses (48M in India)
- Average cost for a pair of glasses is $5-10, with lens processing taking only 15 minutes
- WHO estimates $411 billion loss globally due to productivity, with India losing $2 billion due to reduced schooling outcomes

## Our Mission

At iCare, our mission is simple: bring clarity, quite literally, to the lives of those who've lived too long in blur. We're not inventing a new cure. We're solving an access problem.

Imagine a classroom where a child keeps falling behind, not because they aren't trying, but because they simply can't see the blackboard. Now multiply that by 48 million. This isn't just a health concern; it's an economic one.

Children with untreated URE perform worse in school and have higher dropout rates. The cost of inaction far exceeds the investment required for corrective measures.

But in many parts of India, seeing an optometrist requires:
1. Taking a day off work
2. Traveling to another district
3. Convincing a parent who may not even believe the child has a problem
4. Overcoming cultural stigma, low awareness, and cost barriers

We realized that solving this isn't about replacing doctors: it's about ensuring doctors are used where they're needed most.

## Five-Pillar Approach

Our solution is built on five core pillars:

1. **Universal Access**: Vision care for everyone, regardless of agency, literacy or location. Enables voice-based navigation and offline-first design.

2. **Intelligent Diagnostics**: AI-powered vision tests that scale specialist care. Retina imaging & predictive models for early detection.

3. **Frictionless Communication**: No language should block access to healthcare. Built-in real-time translation for patient-optometrist interactions.

4. **Sustainable by Design**: Recycling and reuse built into our delivery system (pickup of old glasses + low-waste operations).

5. **Transparent & Patient-First**: You own your data, and your choices (downloadable reports, no vendor lock-in, second-opinion friendly).

## User Journey

Meet Asha, a 10-year-old girl from rural Jharkhand who has no idea that the world isn't supposed to look this blurry.

1. She starts her journey on her family's phone. The app welcomes her in Hindi and guides her through voice-based navigation, because reading ability shouldn't be a barrier to better vision.

2. Asha looks into the camera, and in just a few seconds, our system uses predictive diagnostics powered by retina imaging to detect signs of uncorrected refractive error. It works even offline.

3. She's matched with a nearby optometrist. Her parents speak Hindi. The doctor speaks Marathi. But iCare enables real-time language translation, so nothing gets lost between diagnosis and understanding.

4. Once her glasses are ready, they're delivered to her doorstep, and our end-to-end process includes collecting her old glasses for recycling.

5. Asha's family can download all her reports at any time, because we believe in building trust, not walls.

## Technical Architecture

Our architecture is designed to be lean, modular, and human-first, with three key layers:

1. **Engagement Layer**: What users see - built for smartphones, works offline-first, and speaks in the user's voice with voice-based navigation and multilingual UI.

2. **Intelligence Layer**: Where the magic happens - AI-driven retina scans for early triaging and real-time translations between patients and doctors.

3. **Infrastructure Layer**: Cloud-native, modular, and built to scale - containerized microservices that keep costs down and availability up, even on a 2G signal and old device.

The trick isn't building everything. It's building only what delivers the most impact.

### Build, Borrow, Buy Strategy

We made early decisions around a simple question: Should we build it, borrow it, or buy it?

- We **built** what needed empathy and local context: our offline-first mobile interface and vision test flow, tailored for underserved regions.

- We **borrowed** great open-source tools: TensorFlow for AI diagnostics, OpenMRS components for health record handling, and community-validated UI libraries.

- We **bought** where stability mattered: Google's real-time translation API and trusted cloud messaging platforms.

### Technology Stack

- **Mobile Frontend**: React Native for cross-platform mobile application development
- **Image Processing**: OpenCV supports image processing on both server (Python) and client sides (JavaScript)
- **AI/ML**: TensorFlow for AI models, with Google Translation API for language services
- **Healthcare Records**: OpenMRS for standardized health records management
- **Messaging**: Cloud messaging (e.g., Firebase) for notifications and communication
- **Infrastructure**: AWS Cloud with auto-scaling Lambda functions (currently at $0/month thanks to AWS nonprofit credits)
- **API Gateway**: Manages and secures all service interactions
- **Database**: PostgreSQL for structured data management
- **Development**: SCRUM Agile sprints to learn fast, test quickly, and stay close to the people we're building for

### AI Strategy: "AI Where It Helps. Humans Where It Matters."

Our AI is used strictly for triage, not final diagnosis:

1. **User opens app**: Vision test begins, AI module activated on edge device
2. **AI analyzes**: Reviews retina image or vision test pattern
3. **AI flags risk level**: Categorizes as Low, Medium, or High
4. **Optometrist reviews**: A human professional confirms/updates results
5. **Final diagnosis issued**: By human, not algorithm
6. **Treatment ordered**: Glasses ordered or follow-up scheduled

Key AI architectural decisions:

- Edge-based AI for offline functionality and lower costs
- Human-in-the-loop for ethical, safe diagnosis
- Graceful fallback for older devices to ensure inclusive access
- Loose coupling for faster iteration and swappable AI components

### Security Architecture: "Security by Default. Privacy by Design."

- **End-to-End Encryption**: At rest and in transit
- **Role-Based Access Control**: Powered by Okta
- **Full Audit Trails**: System-wide activity logging
- **Real-Time Monitoring**: Via AWS GuardDuty + CloudWatch
- **Zero-Trust Architecture**: Services are containerized and isolated
- **GDPR & CCPA-Conscious**: Regional compliance awareness
- **User Data Ownership**: Patients control their health records

### Trusted Nonprofit Tech Stack
- **Okta**: Identity & access control
- **Box**: Secure document storage
- **AWS**: Cloud infrastructure + monitoring
- **Zoho One**: Admin ops & analytics
- **Slack**: Secure internal communications
- **Webex**: Team & partner coordination

## Implementation Strategy

Our execution strategy follows a phased approach:

### Phase 1: Pilot Programs
- Schools & vision camps in select districts
- Manual + digital hybrid testing
- Community health workers involved

### Phase 2: NGO & Local Partner Expansion
- Training local organizations to run iCare assessments
- Integrating regional dialects + device testing
- Testing in both low- and high-connectivity areas

### Phase 3: Regional Scale via Modular Rollouts
- Incremental cloud-based deployments
- Regional optometrist network onboarding
- Local storage + language compliance

### Phase 4: Continuous Feedback + Iteration
- 2-week SCRUM sprints
- On-ground user feedback loops
- Agile release updates (fail fast, fix fast)

## Global Expansion Readiness

iCare was built to go beyond borders from the start. Our architecture is modular, region-aware, and regulation-conscious:

- **Language & UX**: Multilingual voice navigation with text + audio layer swaps
- **Compliance**: GDPR, HIPAA, CCPA ready with modular data policy engine
- **Infrastructure**: Region-based deployment through cloud-native & loosely coupled services

We don't need to rebuild iCare for every country. We just need to translate it: ethically, securely, and efficiently.

## SITAC 2025 Competition

This project was developed as part of the SITAC 2025 competition, where our team won 2nd place. The competition spanned six months, during which we developed a comprehensive solution addressing the challenge of Uncorrected Refractive Error in India.

The repository contains our complete submission, including:
- Detailed architectural documentation
- User experience design
- Implementation strategy
- Security framework
- Deployment infrastructure

Our solution was recognized for its innovative approach to healthcare access, technical excellence, and potential for real-world impact.

## Get Involved

We welcome contributions from developers, healthcare professionals, and organizations interested in making vision care accessible to everyone. To contribute or learn more, please contact us through the information on our website.
