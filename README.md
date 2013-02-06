Drools Planner on OpenShift Express
===================================
Installing the Drools Planner tool on OpenShift was never easier!

Running on OpenShift
--------------------

Create an account at http://openshift.redhat.com/

Create a jbossas-7 application

    rhc app create -a droolsplanner -t jbosseap-6.0 --from-code git://github.com/eschabell/openshift-droolsplanner.git
    
That's it, you can now checkout your application at:

    http://droolsplanner-$your_domain.rhcloud.com/droolsplanner

