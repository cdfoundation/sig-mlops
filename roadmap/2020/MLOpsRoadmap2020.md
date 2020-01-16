# MLOps SIG Roadmap Draft 2020

## NOT YET PUBLISHED

This document sets out the current state of MLOps and provides a five year roadmap for future customer needs which is intended to support pre-competitive collaboration across the industry with a view to improving the overall state of MLOps as a capability for all.

It is intended that this document be iteratively refined by group consensus within the MLOps SIG across a series of regular meetings and then published annually whilst relevant.

Acknowledgements

Current active contributors to the MLOps SIG Roadmap: 

Terry Cox, Bootstrap Ltd <terry@bootstrap.je>

> Amend list of contributors here



# Introduction

## Current State of MLOps

> NOTES: Overview of the current state of MLOps for this year - revised annually. Define principles and methodologies.

### What is MLOps?

MLOps could be narrowly defined as "the ability to apply DevOps principles to Machine Learning applications" however as we shall see shortly, this narrow definition misses the true value of MLOps to the customer. Instead, we define MLOps as “the extension of the DevOps methodology to include Machine Learning and Data Science assets as first class citizens within the DevOps ecology”.

MLOps should be viewed as a practice for consistently managing the ML aspects of products in a way that is unified with all of the other technical and non-technical elements necessary to successfully commercialise those products with maximum potential for viability in the marketplace.

### What is MLOps not?

It sometimes helps to consider what anti-patterns exist around a concept in order to better understand it.

For example, MLOps is not "putting Jupyter Notebooks into production environments".

RAD tools like Jupyter Notebooks can be extremely useful, both in classroom environments and in exploring problem spaces to understand potential approaches to mathematical problems. However, like all Rapid Application Development tools, they achieve the rapid element of their name by trading off other key non-functional requirements like maintainability, testability and scalability.

In the next section, we will discuss the key drivers for MLOps and expand upon the requirements for a true DevOps approach to managing ML assets. At this point in the development of the practice, it perhaps helps to understand that much of ML and AI research and development activity has been driven by Data Science rather than Computer Science teams. This specialisation has enabled great leaps in the ML field but at the same time means that a significant proportion of ML practitioners have never been exposed to the lessons of the past seventy years of managing software assets in commercial environments.

As we shall see, this can result in large conceptual gaps between what is involved in creating a viable proof of concept of a trained ML model on a Data Scientist’s laptop vs what it subsequently takes to be able to safely transition that asset into a commercial product in production environments. It is not therefore unfair to describe the current state of MLOps in 2020 as still on the early path towards maturity and to consider that much of the early challenge for adoption will be one of education and communication rather than purely technical refinements to tooling.

Compounding this challenge, Machine Learning solutions tend to be decision-making systems rather than just data processing systems and thus will be required to be held accountable to much higher standards than those applied to the best quality software delivery projects. The bar for quality and governance processes is therefore very high, in many cases representing legal compliance processes mandated by regional legislation.

As these decision-making solutions increasingly displace human decision-makers in commerce and government, we encounter a new class of governance problems, collectively known as ‘Responsible AI’. These introduce a range of challenges around complex issues such as ethics, fairness and bias in ML models and often fall under government regulation requiring interpretability and explainability of models, often to a standard higher than that applied to human staff.

As a result, it will be necessary for MLOps to develop in a manner that facilitates complex and sensitive governance processes that are of a standard appropriate to what is expected to become a highly regulated area.



## Drivers

> NOTES: Driving forces for the current snapshot of the roadmap.

### General DevOps drivers applied to MLOps

* Optimising the process of taking ML features into production by reducing Lead Time

* Optimising the feedback loop between production and development for ML assets

* Supporting the problem-solving cycle of experimentation and feedback for ML applications

* Unifying the release cycle for ML and conventional assets

* Enabling automated testing of ML assets

* Application of Agile principles to ML projects

* Supporting ML assets as first class citizens within CI/CD systems

* Enabling shift-left on Security to include ML assets

* Improving quality through standardisation across conventional and ML assets

* Applying Static Analysis, Dynamic Analysis, Dependency Scanning and Integrity Checking to ML assets

* Reducing Mean Time To Restore for ML applications

* Reducing Change Fail Percentage for ML applications

* Management of technical debt across ML assets

* Enabling whole-of-life cost savings at a product level

* Reducing overheads of IT management through economies of scale

* Facilitating the re-use of ML approaches through template or ‘quickstart’ projects

* Managing risk by aligning ML deliveries to appropriate governance processes



### Drivers unique to Machine Learning solutions that represent MLOps requirements

* Mitigating the risks associated with producing decision-making products

* Provide specific testing support for detecting ML-specific errors

* Verifying that algorithms make decisions aligned to customer values

* Tracking long term stability of ML asset performance

* Incorporate ethical governance into management of ML assets

* Enabling automated bias detection testing

* Ensuring explainability of decisions

* Providing  transparency and audit-ability of ML assets

* Allowing for provability of decision-making algorithms

* Ensuring long term supportability of long-lived ML assets

* Manage ML-specific security risks such as adversarial attacks

* Providing clear action paths to suspend or revert failed ML assets in production environments

* Managing economic risks associated with deployment of key decision-making systems on customer infrastructure

* Leveraging ML techniques to improve MLOps solutions

* Mitigating liability risk and accountability through appropriate due-diligence over ML assets

* Facilitating compliance verification against regional AI legislation



## Vision

> NOTES: Narrative vision for the future of MLOps.

An optimal MLOps experience is one where Machine Learning assets are treated consistently with all other software assets within a CI/CD environment. Machine Learning models can be deployed alongside the services that wrap them and the services that consume them as part of a unified release process.

MLOps must be language-agnostic. Training scripts for ML models can be written in a wide range of different programming languages, so a focus on Python is artificially limiting to widespread adoption.

MLOps must be framework-agnostic. There are a plethora of different Machine Learning frameworks commonly in use today and it is to be expected that these will continue to proliferate over time. It must be possible to use any desired framework within an MLOps context and be possible to combine multiple frameworks in any given deployment.

MLOps must be platform and infrastructure agnostic. Adoption of MLOps is predicated upon being able to operate using this approach within the constraints of previously defined corporate infrastructure. It should be presumed unlikely that MLOps alone is a sufficient driver to motivate fundamental change to infrastructure.

MLOps should strive to be agnostic to target hardware. Models may expect to be trained or executed on CPU, GPU, TPU, dedicated ASICs or custom neuro-morphic silicon. It should be possible to use MLOps across the widest possible range of target hardware. In some scenarios, it may also be desirable to facilitate ‘cross-compilation’ where models are trained on one class of hardware to optimise for training speed and are deployed onto a different class of hardware to optimise for cost/performance.

MLOps implementations should follow a ‘convention over configuration’ pattern, seeking to minimise the level of build-specific assets that need to be maintained on top of the desired solution. Where configuration is necessary, it should be synthesised where possible and operate on the principle of always creating working examples that can be modified incrementally by customers to meet their needs.

The use of MLOps should teach best known methods of applying MLOps. It should be recognised that many customers will be experts in the field of Data Science but may have had relatively little exposure to DevOps or other SDLC principles. To minimise the learning curve, MLOps defaults should always align to best practice in production environments rather than ‘quick-and-dirty’ as might be the case for expert users wishing to trial an instance of the tooling in a test bench environment.



# Scope

The focus of this roadmap is upon aspects relating to extending DevOps principles to the area of Machine Learning and does not discuss basic features of DevOps or CI/CD approaches that are common across both domains. The intention is for MLOps to decorate DevOps rather than differentiate.



# Summary and Updates

> NOTES: Executive summary of the roadmap and what’s new in revised versions.

This is the first edition of the MLOps Roadmap and sets out the initial challenges for the approach with suggested potential solutions.



# Challenges

> NOTES: Identify challenges in the near and far term that constrain the customer from successfully adopting and benefiting from MLOps principles.

<table>
  <tr>
    <td>Educating data science teams regarding the risks of trying to use Jupyter Notebooks in production</td>
    <td>Communicating the SDLC and the lessons of DevOps in a way that is comfortable for the audience
Highlighting the dangers of using RAD tools in production
Demonstrate simple alternatives that are easy to use as part of an MLOps process</td>
  </tr>
  <tr>
    <td>Treat ML assets as first class citizens in DevOps processes</td>
    <td>Extend CI/CD tools to support ML assets
Integrate ML assets with version control systems</td>
  </tr>
  <tr>
    <td>Providing mechanisms by which training sets, training scripts and service wrappers may all be versioned appropriately</td>
    <td>All assets under version control
ML assets include sets of data
Data volumes may be large
Data may be sensitive
Data ownership may be complex
Multiple platforms may be involved</td>
  </tr>
  <tr>
    <td>Providing mechanisms by which changes to training sets, training scripts and service wrappers may all be auditable across their full lifecycle</td>
    <td>Models may be retrained based upon new training data
Models may be retrained based upon new training approaches
Models may be self-learning
Models may degrade over time
Models may be deployed in new applications
Models may be subject to attack and require revision
Incidents may occur that require root cause analysis and change
Corporate or government compliance may require audit or investigation</td>
  </tr>
  <tr>
    <td>Treating training sets as managed assets under a MLOps workflow</td>
    <td>Content of training sets is essential to audit process, root cause analysis
Data is not typically treated as a managed asset under conventional CI/CD
Data may reside across multiple systems
Data may only be able to reside in restricted jurisdictions
Data storage may not be immutable
Data ownership may be a factor</td>
  </tr>
  <tr>
    <td>Managing the security of data in the MLOps process with particular focus upon the increased risk associated with aggregated data sets used for training or batch processing</td>
    <td>Aggregated data carries additional risk and represents a higher value target
Migration of data into Cloud environments, particularly for training, may be problematic</td>
  </tr>
  <tr>
    <td>Implications of privacy, GDPR and the right to be forgotten upon training sets and deployed models</td>
    <td>The right to use data for training purposes may require audit
Legal compliance may require removing data from audited training sets, which in turn implies the need to retrain and redeploy models built from that data.</td>
  </tr>
  <tr>
    <td>Methods for wrapping trained models as deployable services in scenarios where data scientists training the models may not be experienced software developers with a background in service-oriented design</td>
    <td>Operational use of a model brings new architectural requirements that may sit outside the domain of expertise of the data scientists who created it
Model developers may not be software developers and therefore experience challenges implementing APIs around their models and integrating within solutions</td>
  </tr>
  <tr>
    <td>Approaches for enabling all Machine Learning frameworks to be used within the scope of MLOps, regardless of language or platform</td>
    <td>Common mistake to assume ML = Python
Many commonly used frameworks such as PyTorch and TensorFlow exist and can be expected to continue to proliferate
MLOps must not be opinionated about frameworks or languages</td>
  </tr>
  <tr>
    <td>Approaches for enabling MLOps to support a broad range of target platforms, including but not limited to CPU, GPU, TPU, custom ASICs and neuromorphic silicon.</td>
    <td>Choice of training platform and operational platform may be varied and could be different for separate models in a single project</td>
  </tr>
  <tr>
    <td>Methods for ensuring efficient use of hardware in both training and operational scenarios</td>
    <td>Hardware accelerators are expensive and difficult to virtualise
Cadence of training activities impacts cost of ownership
Elastic scaling of models against demand in operation is challenging when based upon hardware acceleration</td>
  </tr>
  <tr>
    <td>Approaches for applying MLOps to very large scale problems at petabyte scale and beyond</td>
    <td>Problems associated with moving and refreshing large training sets
Problems associated with distributing training loads across hardware accelerators
Problems with speed of distributing training data to correct hardware accelerators
Problems of provisioning / releasing large pools of hardware resources</td>
  </tr>
  <tr>
    <td>Providing appropriate pipeline tools to manage MLOps workflows transparently as part of existing DevOps solutions</td>
    <td>Integration of ML assets with existing CD/CD solutions
Extending Cloud-native build tools to support allocation of ML assets, data and hardware during training builds
Hardware pool management</td>
  </tr>
  <tr>
    <td>Testing ML assets appropriately</td>
    <td>Conventional Unit / Integration / BDD / UAT testing
Adversarial testing
Bias detection
Fairness testing
Ethics testing
Interpretability
Stress testing
Security testing</td>
  </tr>
  <tr>
    <td>Governance processes for managing the release cycle of MLOps assets, including Responsible AI principles</td>
    <td>Managing release of new training sets to data science team
Establishing thresholds for acceptable models
Managing competitive training of model variants against each other in dev environments
Managing release of preferred models into staging environments for integration and UAT
Managing release of specific model versions into production environments for specific clients/deployments
Managing root cause analysis for incident investigation
Observability / interpretability
Explainability and compliance</td>
  </tr>
</table>



# Technology Requirements

> NOTES: Identify specific technology requirements to enable progress against the challenges identified above.

<table>
  <tr>
    <td>Educating data science teams regarding the risks of trying to use Jupyter Notebooks in production</td>
    <td></td>
  </tr>
  <tr>
    <td>Treat ML assets as first class citizens in DevOps processes</td>
    <td></td>
  </tr>
  <tr>
    <td>Providing mechanisms by which training sets, training scripts and service wrappers may all be versioned appropriately</td>
    <td></td>
  </tr>
  <tr>
    <td>Providing mechanisms by which changes to training sets, training scripts and service wrappers may all be auditable across their full lifecycle</td>
    <td></td>
  </tr>
  <tr>
    <td>Treating training sets as managed assets under a MLOps workflow</td>
    <td></td>
  </tr>
  <tr>
    <td>Managing the security of data in the MLOps process with particular focus upon the increased risk associated with aggregated data sets used for training or batch processing</td>
    <td></td>
  </tr>
  <tr>
    <td>Implications of privacy, GDPR and the right to be forgotten upon training sets and deployed models</td>
    <td></td>
  </tr>
  <tr>
    <td>Methods for wrapping trained models as deployable services in scenarios where data scientists training the models may not be experienced software developers with a background in service-oriented design</td>
    <td></td>
  </tr>
  <tr>
    <td>Approaches for enabling all Machine Learning frameworks to be used within the scope of MLOps, regardless of language or platform</td>
    <td></td>
  </tr>
  <tr>
    <td>Approaches for enabling MLOps to support a broad range of target platforms, including but not limited to CPU, GPU, TPU, custom ASICs and neuromorphic silicon.</td>
    <td></td>
  </tr>
  <tr>
    <td>Methods for ensuring efficient use of hardware in both training and operational scenarios</td>
    <td></td>
  </tr>
  <tr>
    <td>Approaches for applying MLOps to very large scale problems at petabyte scale and beyond</td>
    <td></td>
  </tr>
  <tr>
    <td>Providing appropriate pipeline tools to manage MLOps workflows transparently as part of existing DevOps solutions</td>
    <td></td>
  </tr>
  <tr>
    <td>Testing ML assets appropriately</td>
    <td></td>
  </tr>
  <tr>
    <td>Governance processes for managing the release cycle of MLOps assets, including Responsible AI principles</td>
    <td></td>
  </tr>
</table>



# Potential Solutions

> NOTES: Identify potential solutions that could address the challenges above and meet technical requirements.

> TODO: Fix colour coding.

Show a timeline of potential solutions to set expectations.

**Key:**

<table>
  <tr>
    <td bgcolor="#fff598"> </td>
    <td> To Be Determined</td>
  </tr>
  <tr>
    <td bgcolor="#000000"> </td>
    <td> Research Required</td>
  </tr>
  <tr>
    <td bgcolor="#2562ff"> </td>
    <td> Development Underway</td>
  </tr>
  <tr>
    <td bgcolor="#999999"> </td>
    <td> Continuous Improvement</td>
  </tr>
  <tr>
    <td bgcolor="#ffffff"> </td>
    <td> Qualification / Pre-production</td>
  </tr>
</table>


<table>
  <tr>
    <td>Solution</td>
    <td>2020</td>
    <td>2021</td>
    <td>2022</td>
    <td>2023</td>
    <td>2024</td>
  </tr>
  <tr>
    <td>Educating data science teams regarding the risks of trying to use Jupyter Notebooks in production</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Treat ML assets as first class citizens in DevOps processes</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Providing mechanisms by which training sets, training scripts and service wrappers may all be versioned appropriately</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Providing mechanisms by which changes to training sets, training scripts and service wrappers may all be auditable across their full lifecycle</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Treating training sets as managed assets under a MLOps workflow</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Managing the security of data in the MLOps process with particular focus upon the increased risk associated with aggregated data sets used for training or batch processing</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Implications of privacy, GDPR and the right to be forgotten upon training sets and deployed models</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Methods for wrapping trained models as deployable services in scenarios where data scientists training the models may not be experienced software developers with a background in service-oriented design</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Approaches for enabling all Machine Learning frameworks to be used within the scope of MLOps, regardless of language or platform</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Approaches for enabling MLOps to support a broad range of target platforms, including but not limited to CPU, GPU, TPU, custom ASICs and neuromorphic silicon.</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Methods for ensuring efficient use of hardware in both training and operational scenarios</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Approaches for applying MLOps to very large scale problems at petabyte scale and beyond</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Providing appropriate pipeline tools to manage MLOps workflows transparently as part of existing DevOps solutions</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Testing ML assets appropriately</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Governance processes for managing the release cycle of MLOps assets, including Responsible AI principles</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</table>



# Cross-Cutting Concerns

> NOTES: Identify aspects of MLOps that overlap with issues covered by other SIGs and ensure alignment of work on cross-cutting concerns.

The following cross-cutting concerns are identified:

* CI/CD tooling across DevOps and MLOps scenarios

* Pipeline management

* Common testing aspects such as code coverage, code quality, licence tracking, CVE checking etc.

* Security



# Conclusions and Recommendations

> NOTES: Conclusions and recommendations for the current year.



# References

> NOTES: List of references.



