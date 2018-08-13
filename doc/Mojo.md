# Mojolicious

## The Hello World

The hello world example

    #!/usr/bin/env perl
	use Mojolicious::Lite;

    get '/' => sub {
	  my $c = shift;
	  $c->render(text => 'Hello World!');
    };

    app->start;

## Run the Server

    $ ./myapp.pl daemon
    Server available at http://127.0.0.1:3000

    $ ./myapp.pl daemon -l http://*:8080
    Server available at http://127.0.0.1:8080

    $ ./myapp.pl cgi
    ...CGI output...

    $ ./myapp.pl get /
    Hello World!

    $ ./myapp.pl
    ...List of available commands (or automatically detected environment)...

In the Script:

    # Use @ARGV to pick a command
    app->start;

    # Start the "daemon" command
    app->start('daemon', '-l', 'http://*:8080');
