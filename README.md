<h1>T2</h1>

<p>The new public square</p>

---

# Preview

![preview](.github/assets/t2_screenshot.png)

# TODOs

Next steps in priority order:

P0:
- [ ] *Deploy to Cloud* - need to be able to deploy to AWS or Google Cloud. If Google Cloud, we need to rewrite the image uploader which currently uploads to AWS. Initially I think the url should be http://beta.t2.social/

P1: 
- [ ] *Make just-posted tweet appear at top of feed* - when I post something, the post should appear at the top of my feed.
- [ ] *Email setup* - need to be able to send emails. I have an authenticated SendGrid account which we could use.
- [ ] *Forgot Password?* - User enters email, password change link is sent to that email. User can enter new password. We'll also need to create a new SendGrid email template for this [mockup](.github/assets/mocks/forgot_password_screen.png)

P2:
- [ ] *Signup with handle key* - Close the current signup flow. Let Gabor send a special link that allows the person who receives that link to claim a handle. E.g. going to http://beta.t2.social/signup?handle=alex&key=1234567890 would let me reserve the handle "alex" - they key could just be a SHA1 hash of the handle + a magic key. [mockup](.github/assets/mocks/handle_reservation.png)
- [ ] *Disallow open signups* - turn off open signups, steer users to [this waitlist form](https://docs.google.com/forms/d/e/1FAIpQLScRy1aytEWKJ_cevFilEjUmTkj_Rwh4dWfb2YNQ0nzGF21KKA/formResponse) - we will invite them one-by-one per "Signup with guaranteed handle key"

P3:
- [ ] *Timeline loading bugs* - Timeline should show your my own tweets along with everyone I follow.
- [ ] *Logged out views* - Show profile and post pages even when people aren't logged in. The logged-out home (/) should just say "sign up" / "log in" [mockup](.github/assets/mocks/logged_out.png)
- [ ] *Notifications* - a screen to show notifications when others like, reply, retweet, or dislike [mockup](.github/assets/mocks/notifications_mock.png)
- [ ] *Dislike button on each post* - There's a dislike button on each post. When you dislike a post, ask for the reason you dislike it (this person is being mean, not relevant, not interested in this topic) [mockup](.github/assets/mocks/dislike_button.png)
- [ ] *Search for people* - allow searching for people's names, not just post content
- [ ] *Show a filled-out heart when I've liked something* - right now the heart icon doesn't change when the user has liked something

P4:
- [ ] *Trust and Safety test* - take a quick test about trust and safety before you are allowed to post
- [ ] *Badging system* - show that people are verified, have taken the trust and safety test. Needs to support more badges eventually. [conversation starter mock](.github/assets/mocks/badging_draft.png)
- [ ] *Add links to Terms and Conditions* - Add links to Terms and Conditions throughout

P5:
- [ ] *Embed* - allow embedding content on other sites

P6:
- [ ] *DMs* - A basic DM implementation
- [ ] *New backend* - right now this is all on Postgres which I doubt will scale - perhaps move to Cassandra, Pulsar
- [ ] *New tweet indicator* - When there are new posts in the screen you're looking at, an indicator pops in to that effect

P6:
- [ ] *iOS client*
- [ ] *Android client*

# How to run

Check [here](RUNNING_LOCALLY.md) on how to run locally