Finance-CaVirtex-API
====================

CaVirtex public and private API interface

Also available on MetaCPAN: 

     https://metacpan.org/pod/Finance::CaVirtex::API

Install using CPAN:

     $ perl -MCPAN -e 'install Finance::CaVirtex::API'

Sample Usage:

    my $api  = Finance::CaVirtex::API->new(token => $key, secret => $secret, client_id => $client_id);
    my $order = $api->order(currencypair => 'USDCAD', mode => 'bid', amount => '4.5', price => '1000.00');

    if ($order) {
        printf "The CaVirtex invoice ID is %s. You can see it here: %s\n", @{$order}{qw(id url)};
    }
    else {
        printf "An error occurred: %s\n", $api->error;
    }


COPYRIGHT AND LICENSE

    Copyright (C) 2014 by Jeff Anderson

    Additional licensing in LICENSE


