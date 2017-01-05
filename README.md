# Ember Wordpress Starter Kit

Ember Wordpress Starter Kit is a simple starting point for developing a WordPress site utilizing EmberJS on the client side, using the [ember-wordpress](https://github.com/oskarrough/ember-wordpress) Ember addon and [WPLib Box](https://github.com/wplib/wplib-box), a Vagrant local development environment.

## Prerequisites

You will need the following things properly installed on your computer.

* [Git](http://git-scm.com/)
* [Node.js](http://nodejs.org/) (with NPM)
* [Bower](http://bower.io/)
* [Ember CLI](http://ember-cli.com/)
* [PhantomJS](http://phantomjs.org/)
* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](https://www.vagrantup.com/)
* [Vagrant Hosts Updater](https://github.com/cogitatio/vagrant-hostsupdater) - Install by running `vagrant plugin install vagrant-hostsupdater`
* [Vagrant Triggers](https://github.com/emyl/vagrant-triggers) - Install by running `vagrant plugin install vagrant-triggers`

## Installation

* `git clone <this-repository>`
* `cd ember-wordpress-starter-kit` (or whatever you named the directory
* `cd ember-app`
* `npm install`
* `bower install`

## Running Ember

In the project's directory:

* `cd ember-app`
* `ember serve`
* Visit your app at [http://localhost:4200](http://localhost:4200).

## Running WPLib Box

In the project's directory:

* `cd wplib-box`
* `vagrant up`
* open "http://ember-wordpress.dev"

Tip: Here's how to [change the local domain](https://github.com/wplib/wplib-box#setting-the-domain-name).

#### Logging into the WordPress Admin

To login to [ember-wordpress.dev/wp-admin/](http://ember-wordpress.dev/wp-admin) use the following credentials:

Credential|Value
---------|------
Username:|`admin`
Password:| `password`

We will probably change to using different username and password in the future.

<a id="wpdb"></a>
#### The WordPress Database Credentials

If you want to access the database using a tool such as Sequel Pro the MySQL database name, username and password are all `wordpress`.

In other words:

	define( 'DB_NAME', 'wordpress' );
	define( 'DB_USER', 'wordpress' );
	define( 'DB_PASSWORD', 'wordpress' );

We may change to using different MySQL credentials in the future.

<a id="mysql-credentials"></a>
#### The MySQL Credentials

Here are the credentials you can use for accessing the MySQL database using a GUI such as Sequel Pro, Navicat, et al:

Credential|Value
----------|----------
Host Name   | `ember-wordpress.dev` _(or `your-domain.dev`)_
Port        | `3306`
Username    | `wordpress`
Password    | `wordpress`

<a id="mysql-terminal"></a>
#### Connecting to MySQL in Terminal

The MySQL server listens on all interfaces on port 3306. If you have the MySQL command-line client installed on your host machine, you can simply `mysql --host wplib.box -u wordpress -pwordpress` (assuming you are using the `wplib.box` hostname). 

#### Customization

To change the local domain, switch versions of PHP, find instructions for Windows users, etc. refer to the [WPLib Box repository](https://github.com/wplib/wplib-box).
