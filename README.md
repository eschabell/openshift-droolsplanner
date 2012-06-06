jBPM Migration Tooling on OpenShift Express
============================================
Installing the jBPM Migration tool on OpenShift was never easier!

This git repository helps you get up and running quickly with the jBPM
Migration Tooling.


Running on OpenShift
----------------------------

Create an account at http://openshift.redhat.com/

Create a jbossas-7 application

    rhc app create -a jbpmmigration -t jbossas-7

Add this upstream openshift-jbpmmigration repo

    cd jbpmmigration
    git remote add upstream -m master git://github.com/eschabell/openshift-jbpmmigration.git
    git pull -s recursive -X theirs upstream master
    # note that the git pull above can be used later to pull updates to jbpmmigration
    
Then push the repo upstream

    git push

That's it, you can now checkout your application at:

    http://jbpmmigration-$your_domain.rhcloud.com/jbpmmigration_upload-0.4

USAGE NOTES:

You can submit a jBPM jPDL 3.2 process definition as an xml file upload, the
resulting page will show you first your submitted file (if all goes well) and
the resulting BPMN2 process definition. This can be cut and paste into your IDE
for formatting and testing against the jBPM5 editor(s).

