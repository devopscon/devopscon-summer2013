The 2013 Summer Israel DevOps Summer Summit 
===========================================

___Call for papers deadline: June 1, 2013___  

```ruby
require 'speaker'
require 'israel'

module Israel
  module DevOps
    def call_for_papers(speaker, subject)
      # Speakers, please apply for the call for papers if you have talks on the subjects of Continuous 
      # Deployment, DevOps tooling and DevOps case studies, assuming you are available on Jan 15.
      apply(spekaer) if ["Continuous Deployment", 
                         "DevOps tooling", 
                         "DevOps Case Studies", 
                         "Culture",
                         "Web Operations"].include(subject) 
                        and speaker.available?(Date.new(2013,7,2))
    end
    def apply(speaker)
      # We prefer github, but also settle for goo-ol emails
      if speaker.has_github?
        speaker.make_pull_request('/devopscon/devopsisrael-summer2013')
      else
        speaker.send_mail('proposals@devopscon.com')
    end
  end
end
```

If you need it in plain English, here goes:

This repo provides means to propose speaking sessions for the 2013 Israel DevOps Summer Summit. To submit a proposal, fork the repo, add a text file named `your-session.md` (there's a sample template named `sample-proposal.md` in this repo), and submit a pull request. Alternatively, if you're not into github, email your proposal to proposals@devopscon.com. *You should plan for 45 minutes including Q&A*. In your email, make sure to specify the following:

- Session title
- Session abstract
- Speaker bio
- Any references for the speaker's record will be highly appriciated - videos, slide decks, etc.

Ignite Talks
----
We're playing with the idea of having ignite talks (5 minutes, 20 slides which rollover every 15 seconds). 
If you're interesting in having an ignite talk, email us at proposals@devopscon.com. If we have enough of these we'll dedicate 

Labs
----
We're also open to lab sessions as part of the conference. Lab sessions can be up to 1:50 long, and cover DevOps related tools and parctices. They have to be technical, preferably hands on sessions that will give practical knowledge to attendees. If you have a lab session in mind, feel free to submit it via github or email as any other session. In addition to all the details above, make sure to specify: 
- The exact duration of the lab
- Any prequisites you have for participants to take part in the lab 


