When /^I get LoginInfo from API for GMFCA$/ do
    begin
        $log << "Scenario Details...\n #{$scenario_name}"
        if $scenario_name.include?("French")
          $langCode="fr"
        end
        $username=$userId=$gmfca_username
        $orgId=$gmfca_orgId
        $plid=$gmfca_plid
        steps %Q{When I get login info API}
        steps %Q{When Print Log details}
    end
    end
    
