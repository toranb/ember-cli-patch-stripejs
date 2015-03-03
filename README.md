This addon will add Stripe or patch it depending on your enviornment

In development/test/server builds you will get the following

<script type="text/javascript">
    var Stripe = {
        setPublishableKey: function(){
            console.log("Setting publishable key.");
        },
        card: {
            createToken: function() {
                console.log("createToken was called.");
            }
        }
    };
</script>

In production you will get the real stripe client library

<script type="text/javascript" src="//static.twilio.com/libs/twiliojs/1.2/twilio.min.js"></script>
