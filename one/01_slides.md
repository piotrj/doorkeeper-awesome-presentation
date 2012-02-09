!SLIDE center
![Start](start.jpg)

!SLIDE center
![Not Sure](not_sure_oauth.jpg)

!SLIDE center
![Y U NO](y_u_no.jpg)

!SLIDE center
![SUCCESS](success.jpg)

!SLIDE center
![dawg](dawg.jpg)

!SLIDE center
![awesome](awesome.jpg)

!SLIDE center
    @@@ ruby
    gem 'doorkeeper'
    rails generate doorkeeper:install
    rake db:migrate

!SLIDE smaller
    @@@ ruby
    Doorkeeper.configure do
      resource_owner_authenticator do |routes|
        current_user ||
        redirect_to('/sign_in', :alert => "Needs sign in.")
      end
    end

!SLIDE smaller
    @@@ ruby
    class Api::V1::ProductsController < Api::V1::ApiController
      doorkeeper_for :all

      def index; end
    end

!SLIDE center
# Awesome developers
![bros](devs.jpeg)

!SLIDE center
![good](good.jpg)

!SLIDE center
![all](all.jpg)
