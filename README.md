# bottle_seesion_login_logout_no_cache

Note that every page that uses a session should have the headers set to disable caching

  response.set_header("Cache-Control", "no-cache, no-store, must-revalidate")
  response.add_header("Pragma", "no-cache")
  
  # Delete the cookies from the browser
  response.set_cookie("_", "", expires=0)
