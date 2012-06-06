Drools Planner on OpenShift Express
===================================
Installing the Drools Planner tool on OpenShift was never easier!

Running on OpenShift
--------------------

Create an account at http://openshift.redhat.com/

Create a jbossas-7 application

    rhc app create -a planner -t jbossas-7

Add this upstream openshift-droolsplanner repo

    cd planner
    git remote add upstream -m master git://github.com/eschabell/openshift-droolsplanner.git
    git pull -s recursive -X theirs upstream master
    # note that the git pull above can be used later to pull updates.
    
Then push the repo upstream

    git push

That's it, you can now checkout your application at:

    http://planner-$your_domain.rhcloud.com/droolsplanner

