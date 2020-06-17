# placeholder-asterisk-color-Red
placeholder asterisk color Red
~~~
<style type="text/css">
.form-palceholder {
  position: relative;
}
.form-palceholder .palceholder {
  position: absolute;
  top: 7px;
  left: 8px;
  color: #b1b1b1;
  display: none;
}
.form-palceholder label {
  font-wight: normal;
  color: #b1b1b1;
}
.form-palceholder .asterisk {
  color: red;
}

</style>
####################################################
<div class="form-group form-palceholder">
  <div class="palceholder">
          <label for="name">Clinic Name</label>
        <span class="asterisk">*</span>
      </div>
  <input 
    required 
    type="text" 
    class="form-control form-palceholder-control" 
    id="clinic_name" name="name" 
    placeholder="" 
    value="<?php echo set_value('name',isset($user['record']['name'])?$user['record']['name']:''); ?>" 
  />
</div>
####################################################
<script>
	/* placeholder asterisk color Red */
	$('.palceholder').click(function() {
	  $(this).siblings('input').focus();
	});

	$('.form-palceholder-control').focus(function() {
	  $(this).siblings('.palceholder').hide();
	});

	$('.form-palceholder-control').blur(function() {
	  var $this = $(this);
	  if ($this.val().length == 0)
	    $(this).siblings('.palceholder').show();
	});

	$('.form-palceholder-control').blur();
</script>
~~~
