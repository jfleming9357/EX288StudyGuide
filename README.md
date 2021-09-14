# EX288 Study Guide

- Grades have been posted in slack channel previously without NDA issues, so this will follow the grading format
- All chapter references are for __DO288 version 4.6 unless otherwise specified__
- Provided information is __based on the section titles from posted exam results, not specific content within the exam__, which I will not discuss
- As this is by no means an exhaustive guide, the best study method is to be able to complete __all DO288 labs__ without showing the answers. I would encourage you to consult the docs if you are stuck, as you will have them during the exam.
- Best practice is to be able to complete all functionality in __both the CLI and web console__ where possible, however I may specify where one might be easier than the other in some cases, though bear in mind that these are opinions
- [Full exam study points for the exam, from Red Hat](https://www.redhat.com/en/services/training/ex288-red-hat-certified-specialist-openshift-application-development-exam?section=Objectives)
  - As this is the full list, this is exactly what you should study. Some of my guide is definitely redundant with this. My goal is to provide relevant information for where to find some topics, along with things that have tripped up myself or others while learning OpenShift
- If anyone thinks that too much has been shared, information is incorrect or could be improved, or you have any questions, please contact me at jason.fleming@ibm.com, or @jason.fleming on IBM slack channels


__General tips__
- Use the ‘latest’ version of an image unless you have a good reason to use a previous version
- __Use the provided docs during the exam__. Control+f is your friend.
  - Emphasis placed on linking to docs, so that you are faster at navigating them during the exam
- If you only have experience with one programming language, know how to run files for popular programming languages you might not know (python, javascript, java, etc)

__Exam Sections__

1. __Application Deployment__
    - Chapter 1 and 6
    - What you learned in DO180 is also quite useful here
    - Be able to deploy apps with both the CLI and web console
2. __Maintenance__
    - Fairly general title, so this can cover a wide variety of topics. __Be comfortable with searching through the docs__
3. __Troubleshooting__
    - Chapter 1.8
    - DO180 v4.6 Chapter 8 for more depth + guided exercises + lab
    - Easiest to identify errors/check logs/etc in the web console. Fixing the errors varies.
4. __Customizing Dockerfiles and S2I Builder Images__
    - Chapter 5
    - Remember that s2i repositories have a __hidden s2i folder (.s2i)__. You can check for them with ```ls -a```. Know how to customize the assemble/run scripts within, similar to dockerfiles (.s2i/bin)
    - [S2I in RHOCP docs](https://docs.openshift.com/container-platform/4.6/openshift_images/create-images.html#images-create-s2i_create-images)
5. __Using Openshift ConfigMaps and Secrets__
    - Chapter 2
    - Know how to create a configmap using CLI or web console
    - Applying a configmap to an application is referring to setting env/secrets/etc from configmaps, not just creating the cm within the project
    - Oc set env|secret dc/{dc name} --from cm/{cm name}
    - [ConfigMaps in RHOCP docs](https://docs.openshift.com/container-platform/4.6/authentication/configmaps.html)
    - Can be done with CLI or web console
6. __Implementing Hooks and Triggers__
    - Chapter 4
    - [Openshift Hooks/Triggers in RHOCP docs](https://docs.openshift.com/container-platform/4.6/builds/triggering-builds-build-hooks.html)
    - Easiest in web console
7. __Working with Templates__
    - Chapter 6 __VERSION 4.5__
    - Version 4.6 does not provide enough template content in my opinion
    - Be able to edit/troubleshoot templates, load them into openshift, then create an application using that template
    - Understand parameters and their different fields (name, description, value, required, etc)
    - [Templates in RHOCP docs](https://docs.openshift.com/container-platform/4.6/openshift_images/using-templates.html#templates-uploading_using-templates)
8. __Application Health Monitoring__
    - Chapters 7.1, 7.2
    - Very easy in web console
    - [Health checks using the developer perspective in RHOCP docs](https://docs.openshift.com/container-platform/4.6/applications/application-health.html#odc-adding-health-checks)


__General exam prep resources (that you probably know if you have taken EX180)__

- Install [Codeready Containers (crc)](https://console.redhat.com/openshift/install/crc/installer-provisioned?intcmp=7013a000002CtetAAC) to save on lab hours or experiment on your own
  - Red Hat developer sandbox also works
- Get your exam environment ready early
  - To use your IBM laptop for the exam, you need to disable secure boot
  - [Exam PDF](https://www.redhat.com/rhdc/managed-files/tr-remote-exams-preparation-ebook-f27382-202103-en_1.pdf) (includes link to most recent ISO)
  - May need to use an [older ISO](https://static.redhat.com/downloads/training-certification/rhrexboot-2020-08.iso)
  - If the above do not work, you may need to try a different computer
- Exam scheduler is in a 24 hour time format. Be mindful of this fact. You will not get your exam credit back if you miss it. And don’t ask why I feel the need to mention this.


__Exam Taking Tips__

- During the exam, be sure to manage your time efficiently
- Don't spend too much time on one question if you can’t figure it out
- Try to leave time at the end to go back and test your answers
- Use the -h | --help flag
- If you fail your first attempt (or think you did), immediately create a practice test __for yourself__ from what you can remember while the exam is fresh in your mind. Figure out the answers, then make sure you can do them quickly. It is important that you do not share this with anyone else, as that is against the NDA for obvious reasons.
- Don’t stress if you don’t pass the first time. From what I have seen, most people don’t. And if you don’t have any retakes available for whatever reason, you can take a different version of the exam (until they remove it on 10/1/2021).
