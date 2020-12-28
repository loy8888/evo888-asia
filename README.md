<html>
 <head> 
  <meta charset="utf-8"> 
  <meta http-equiv="X-UA-Compatible" content="IE=edge"> 
  <title>Management Center</title> 
  <!-- Tell the browser to be responsive to screen width --> 
  <meta content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no" name="viewport"> 
  <!-- Bootstrap 3.3.6 --> 
  <link rel="stylesheet" href="/Content/bootstrap/css/bootstrap.min.css"> 
  <!-- Font Awesome --> 
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.5.0/css/font-awesome.min.css"> 
  <!-- Ionicons --> 
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/ionicons/2.0.1/css/ionicons.min.css"> 
  <!-- jvectormap --> 
  <link rel="stylesheet" href="/Content/plugins/jvectormap/jquery-jvectormap-1.2.2.css"> 
  <!-- Theme style --> 
  <link rel="stylesheet" href="/Content/dist/css/AdminLTE.min.css"> 
  <link rel="stylesheet" href="/Content/page.css"> 
  <!-- AdminLTE Skins. Choose a skin from the css/skins
         folder instead of downloading all of them to reduce the load. --> 
  <link rel="stylesheet" href="/Content/dist/css/skins/_all-skins.min.css"> 
  <link rel="stylesheet" href="/Content/jquery.dataTables.min.css"> 
  <link rel="stylesheet" href="/Content/plugins/timepicker/bootstrap-timepicker.min.css"> 
  <link rel="stylesheet" href="/Content/plugins/datepicker/datepicker3.css"> 
  <link rel="stylesheet" href="/Content/plugins/select2/select2.min.css"> 
  <link rel="stylesheet" href="/Content/plugins/timepicker/bootstrap-timepicker.min.css"> 
  <link rel="stylesheet" href="/Content/WdatePicker.css"> 
  <link rel="stylesheet" href="/Content/sweetalert.css"> 
  <link rel="stylesheet" href="/Content/black.css"> 
  <link rel="stylesheet" href="/Content/laypage.css"> 
  <!-- HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries --> 
  <!-- WARNING: Respond.js doesn't work if you view the page via file:// --> 
  <!--[if lt IE 9]>
     
     
    <![endif]--> 
  <link href="/Content/skin/My97DatePicker/skin/WdatePicker.css" rel="stylesheet" type="text/css"> 
  <!-- jQuery 2.2.3 --> 
  <!-- Bootstrap 3.3.6 --> 
  <!-- FastClick --> 
  <!-- AdminLTE App --> 
  <!-- Sparkline --> 
  <!-- jvectormap --> 
  <!-- SlimScroll 1.3.0 --> 
  <!-- ChartJS 1.0.1 --> 
  <!-- AdminLTE dashboard demo (This is only for demo purposes) --> 
  <!-- AdminLTE for demo purposes --> 
  <script>
        Alert = {
            show: function ($div, msg) {
                $div.find('.alert-msg').text(msg);
                if ($div.css('display') === 'none') {
                    // fadein, fadeout.
                    $div.fadeIn(1000).delay(2000).fadeOut(0);
                }
            },
            info: function (msg) {
                this.show($('#alert-info'), msg);
            },
            warn: function (msg) {
                this.show($('#alert-warn'), msg);
            }
        }
        $('body').on('click', '.alert-close', function () {
            $(this).parents('.alert').hide();
        });
        $('#info').click(function () {
            Alert.info('This is infomation alert.')
        });
        $('#warn').click(function () {
            Alert.warn('This is warning alert.')
        });
    </script> 
  <style type="text/css">.jqstooltip { position: absolute;left: 0px;top: 0px;visibility: hidden;background: rgb(0, 0, 0) transparent;background-color: rgba(0,0,0,0.6);filter:progid:DXImageTransform.Microsoft.gradient(startColorstr=#99000000, endColorstr=#99000000);-ms-filter: "progid:DXImageTransform.Microsoft.gradient(startColorstr=#99000000, endColorstr=#99000000)";color: white;font: 10px arial, san serif;text-align: left;white-space: nowrap;padding: 5px;border: 1px solid white;z-index: 10000;}.jqsfield { color: white;font: 10px arial, san serif;text-align: left;}</style>
 </head> 
 <body class="skin-purple sidebar-mini"> 
  <div class="wrapper"> 
   <header class="main-header"> 
    <!-- Logo --> 
    <a href="/" class="logo hidden-xs"> 
     <!-- mini logo for sidebar mini 50x50 pixels --> <span class="logo-mini"><b></b></span> 
     <!-- logo for regular state and mobile devices --> <span class="logo-lg"><b></b></span> </a> 
    <!-- Header Navbar: style can be found in header.less --> 
    <nav class="navbar navbar-static-top"> 
     <!-- Sidebar toggle button--> 
     <a href="#" class="sidebar-toggle" data-toggle="offcanvas" role="button"> <span class="sr-only">Toggle navigation</span> </a> 
     <div style="padding:15px;color:White;"> 
      <span style="margin-right:10px;"><i class="fa fa-user"></i><span class="m_uid" id="m_uid_name">&nbsp;&nbsp;&nbsp;Bazuka01</span></span> 
      <span class="badge bg-gray span_d" id="n1" style="display: none;"></span> 
      <span class="badge bg-orange span_d" id="n2" style="display: none;"></span> 
      <span class="badge bg-aqua span_d" id="n3" title="my current score" style="vertical-align:baseline">My Score: 1000.00</span> 
      <span class="hidden-xs" style="margin-left:10px"><i class="fa fa-calendar-times-o"></i>&nbsp;&nbsp;&nbsp;<span id="localtime" style="color:White;"><font color="#ffffff">2020-12-28 01:31:38 </font></span></span> 
      <!-- Navbar Right Menu --> 
     </div> 
    </nav> 
   </header> 
   <!-- Left side column. contains the logo and sidebar --> 
   <aside class="main-sidebar"> 
    <!-- sidebar: style can be found in sidebar.less --> 
    <section class="sidebar" style="height: auto;"> 
     <!-- Sidebar user panel --> 
     <!-- search form --> 
     <form action="/Search/Index" method="get" class="sidebar-form"> 
      <div class="input-group"> 
       <input type="text" name="username" class="form-control" placeholder="Search…"> 
       <input type="hidden" name="type" value="1"> 
       <span class="input-group-btn"> <button type="submit" name="search" id="search-btn" class="btn btn-flat"> <i class="fa fa-search"></i> </button> </span> 
      </div> 
     </form> 
     <!-- /.search form --> 
     <!-- sidebar menu: : style can be found in sidebar.less --> 
     <form action="/Account/LogOff" class="navbar-right" id="logoutForm" method="post">
      <input name="__RequestVerificationToken" type="hidden" value="gyuDlPPf-ONWa4kV2H7Ge3eRcMQqfK7pzLe1cUi0Cx7kSowHzzHcOJr9n8wbfV6qQlJYr3ajxHD1AKbc4Co0SSPsvu5BfBLAdWQ8-zO2hD41">
     </form> 
     <ul class="sidebar-menu"> 
      <li> <a href="/Account/Manage?action=1"> <i class="fa fa-lock text-gray"></i> <span class="text-bold">Change Password</span> </a> </li> 
      <li> <a href="/Manage/Management?parentId=10242"> <i class="fa  fa-users text-gray"></i> <span class="text-bold">User Management</span> </a> </li> 
      <li> <a href="/Search/Index"> <i class="fa fa-search text-gray"></i> <span class="text-bold">Search User</span> </a> </li> 
      <li> <a href="/ScoreLog/SearchScoreLog"> <i class="fa fa-history text-aqua"></i> <span class="text-bold">Player Score Log</span> </a> </li> 
      <li> <a href="/GameLog/SearchGameLog"> <i class="fa fa-history text-blue"></i> <span class="text-bold">Player Game Log</span> </a> </li> 
      <li> <a href="/BonusLog/SearchBonusLog"> <i class="fa fa-history text-red"></i> <span class="text-bold">Player Bonus Log</span> </a> </li> 
      <li> <a href="/LuckyWheelLog/SearchLuckyWheelLog"> <i class="fa fa-history text-red"></i> <span class="text-bold">Player LuckyWheelLog</span> </a> </li> 
      <li> <a href="/LoginLog/SearchLoginLog"> <i class="fa fa-history text-gray"></i> <span class="text-bold">Player Login Log</span> </a> </li> 
      <li> <a href="/OperationLog/ViewLog"> <i class="fa fa-dot-circle-o text-gray"></i> <span class="text-bold">Operation Log</span> </a> </li> 
      <li> <a href="/Suggestion/Create"> <i class="fa fa-info-circle text-gray"></i> <span class="text-bold">Suggestion</span> </a> </li> 
      <li> <a href="/Agent/SetAgentLoginIP?agentid=10242"> <i class="fa fa-info-circle text-gray"></i> <span class="text-bold">Set Agent Login IP</span> </a> </li> 
      <li> <a style="cursor:pointer" id="signout"> <i class="fa fa-sign-out text-green fa-lg"></i> <span class="text-bold text-orange">Sign Out</span> </a> </li> 
     </ul> 
     <script>
    $('#signout').click(function () {
        swal({
            title: "Are you sure sign out?",
            type: "warning",
            showCancelButton: true,
            confirmButtonColor: '#00A65A',
            confirmButtonText: 'OK',
            cancelButtonText: "Cancel",
            closeOnConfirm: false,
            closeOnCancel: true
        },
 function (isConfirm) {

     if (isConfirm) {
         document.getElementById('logoutForm').submit()
     }
 });
    })
</script> 
    </section> 
    <!-- /.sidebar --> 
   </aside> 
   <!-- Content Wrapper. Contains page content --> 
   <div class="content-wrapper" style="min-height: 592.001px;"> 
    <!-- Content Header (Page header) --> 
    <!-- Main content --> 
    <section class="content"> 
     <div id="alert-info" class="alert alert-info alert-top" role="alert"> 
      <button type="button" class="close alert-close" aria-label="Close"><span aria-hidden="true">×</span></button> 
      <span class="alert-msg"></span> 
     </div> 
     <div id="alert-warn" class="alert alert-warning alert-top" role="alert"> 
      <button type="button" class="close alert-close" aria-label="Close"><span aria-hidden="true">×</span></button> 
      <span class="alert-msg"></span> 
     </div> 
     <!-- Info boxes --> 
     <section class="content-header"> 
      <h1 class="hidden-xs"> Search User<small><a href="javascript:window.history.back()" target="_self" onclick="javascript:window.history.back();"><i class="fa fa-arrow-left"></i> Back</a></small> </h1> 
      <ol class="breadcrumb hidden-md hidden-lg hidden-sm"> 
       <li>Search User&nbsp;&nbsp;&nbsp;<a href="javascript:window.history.back()" target="_self" onclick="javascript:window.history.back();"><i class="fa fa-arrow-left"></i> Back</a></li> 
      </ol> 
     </section> 
     <section class="content"> 
      <div class="box box-default"> 
       <div class="box-body"> 
        <div class="input-group input-group-lg"> 
         <input type="text" id="txt_UserName" maxlength="17" class="form-control text-bold text-blue ui-autocomplete-input" autocomplete="off"> 
         <span class="input-group-btn"> <button type="button" id="Button_OK" class="btn btn-info btn-flat">Go</button> </span> 
        </div> 
       </div> 
       <div class="box box-primary" id="tb_list_0" style="display:none;"> 
        <div class="box-header with-border"> 
         <h3 class="box-title text-bold" id="d_tip_0"></h3>
         <i class="fa fa-angle-decimal-right"></i> 
         <div class="box-tools pull-right"> 
          <button data-widget="collapse" class="btn btn-box-tool" type="button"><i class="fa fa-minus"></i></button> 
         </div> 
        </div> 
        <div class="box-body" style="display: block;"> 
         <div class="table-responsive"> 
          <table class="table table-hover table-bordered"> 
           <thead> 
            <tr> 
             <th> Username </th> 
             <th> Score </th> 
             <th> Name </th> 
             <th> Agent </th> 
             <th> Tel </th> 
             <th> Description </th> 
             <th> Operation </th> 
            </tr> 
           </thead> 
           <tbody id="tblData_0"></tbody> 
          </table> 
         </div> 
        </div> 
       </div> 
       <input type="hidden" value="0" id="type"> 
       <div class="box-body" id="tb_list_1" style="display: none"> 
        <div class="table-responsive"> 
         <table class="table table-bordered"> 
          <thead> 
           <tr> 
            <th id="th_infoID" style="display:none;"> UID </th> 
            <th> Username </th> 
            <th> Online </th> 
            <th> PlayerStatus </th> 
            <th> Agent </th> 
            <th> Balance </th> 
            <th> Name </th> 
            <th> Tel </th> 
            <th> Description </th> 
            <th> Operation </th> 
           </tr> 
          </thead> 
          <tbody id="tblData_1"></tbody> 
         </table> 
        </div> 
       </div> 
       <input type="hidden" value="1" id="reportLevel"> 
       <input type="hidden" value="1" id="setScoreLevel"> 
       <input type="hidden" value="1" id="addUserLevel"> 
       <input type="hidden" value="1" id="enableUserLevel"> 
       <input type="hidden" value="1" id="editUserLevel"> 
       <div class="box box-primary" id="tb_list_2" style="display:none;"> 
        <div class="box-header with-border"> 
         <h3 class="box-title text-bold" id="d_tip_1"></h3>
         <i class="fa fa-angle-decimal-right"></i> 
         <div class="box-tools pull-right"> 
          <button data-widget="collapse" class="btn btn-box-tool" type="button"><i class="fa fa-minus"></i></button> 
         </div> 
        </div> 
        <div class="box-body" style="display: block;"> 
         <div class="table-responsive"> 
          <table class="table table-hover table-bordered"> 
           <thead> 
            <tr> 
             <th> Username </th> 
             <th> Balance </th> 
             <th> Name </th> 
             <th> User agent </th> 
             <th> Tel </th> 
             <th> Description </th> 
             <th> Operation </th> 
            </tr> 
           </thead> 
           <tbody id="tblData_2"></tbody> 
          </table> 
         </div> 
        </div> 
       </div> 
      </div> 
     </section> 
     <!-- /.row --> 
    </section> 
    <!-- /.content --> 
   </div> 
   <!-- /.content-wrapper --> 
   <div class="main-footer hidden-xs bg-gray-light" style=""> 
    <span class="text-danger">
     <marquee behavior="scroll" scrollamount="2" direction="left" onmouseover="this.stop()" onmouseout="this.start()"></marquee></span> 
   </div> 
   <!-- <footer class="main-footer">
            <div class="pull-right hidden-xs">

            </div>

        </footer> --> 
   <!-- Add the sidebar's background. This div must be placed
             immediately after the control sidebar --> 
   <div class="control-sidebar-bg" style="position: fixed; height: auto;"></div> 
   <div class="modal hide" id="pleaseWaitDialog" data-backdrop="static" data-keyboard="false"> 
    <div class="modal-header"> 
     <h1>Processing...</h1> 
    </div> 
    <div class="modal-body"> 
     <div class="progress progress-striped active"> 
      <div class="bar" style="width: 100%;"></div> 
     </div> 
    </div> 
   </div> 
  </div> 
  <!-- ./wrapper --> 
  <script>
        var reportLevel = document.getElementById('reportLevel').value;
        var setScoreLevel = document.getElementById('setScoreLevel').value;
        var addUserLevel = document.getElementById('addUserLevel').value;
        var enableUserLevel = document.getElementById('enableUserLevel').value;
        var editUserLevel = document.getElementById('editUserLevel').value;
    $(document).ready(function () {
        var type = parseInt($('#type').val());
        if (type == 1) {
            AppendTable();
        }
    })
    $('#txt_UserName').keypress(function (e) {
        var key = e.which;
        if (key == 13) {
            e.preventDefault();
            $.LoadingOverlay("show");
            AppendTable();
            $.LoadingOverlay("hide");

        }
    });

    $('#Button_OK').click(function (e) {
        e.preventDefault();
        $.LoadingOverlay("show");
        AppendTable();
        $.LoadingOverlay("hide");
    })
    function AppendTable() {
        var data = {
            username: $('#txt_UserName').val()
        };

        $.ajax({
            type: "POST",
            url: "/Search/Search",
            content: "application/json; charset=utf-8",
            data: data,
            success: function (d) {
                $('#tblData_0').text("");
                $('#tblData_1').text("");
                $('#tblData_2').text("");

                var jsondata = $.parseJSON(d);
                if (jsondata == null) {
                    swal({ title: "no this account.", confirmButtonText: 'OK' });
                    return;
                }

                if (jsondata["error"] != "") {
                    swal({ title: jsondata["error"], confirmButtonText: 'OK' });
                    return;
                }
                if (jsondata["pathdata"] == null) {
                    swal({ title: "no this account.", confirmButtonText: 'OK' });
                    return;
                }
                if (jsondata["pathdata"] != null && jsondata["pathdata"].length > 0) {
                    for (var i = 0; i < jsondata["pathdata"].length; i++) {
                        var row = jsondata["pathdata"][i];
                        var tags = '';
                        tags += '<td id="op2_0" class="text-left">';
                        if (setScoreLevel == 1) {
                            tags += '<button type="button" class="btn btn-info btn-xs" title="" onfocus="this.blur();" onclick="document.location=' + "'/Agent/EditScore?id=" + row.id + "'" + '"' + '>set score</button>';
                        }

                        tags += '<button type="button" class="btn btn-info btn-xs" title="" onfocus="this.blur();" onclick="document.location=' + "'/ScoreLog/SearchScoreLog?sid=" + row.id + "'" + '"' + '">score log</button>';
                        if (editUserLevel == 1) {
                            tags += '<button type="button" class="btn btn-info btn-xs" title="" onfocus="this.blur();" onclick="document.location=' + "'/Agent/Edit?id=" + row.id + "'" + '">edit</button>';
                        }
                        if (reportLevel == 1) {
                            tags += '<button type="button" class="btn btn-info btn-xs" title="" onfocus="this.blur();" onclick="document.location=' + "'/Report/Search?sid=" + row.id + "'" + '">report</button>';
                            tags += '<button type="button" class="btn btn-info btn-xs" title="" onfocus="this.blur();" onclick="document.location=' + "'/Report/Chart?sid=" + row.id + "'" + '">chart</button>';
                        }
                        if (enableUserLevel) {
                            tags += '<button type="button" class="btn btn-info btn-xs" title="" onfocus="this.blur();" onclick="">Total</button>';
                            if (row.state == 1) {
                                tags += '<button type="button" name="agentable" title="' + row.username + '" rel="disable" player="' + row.id + '" class="btn btn-info btn-xs" onfocus="this.blur();" onclick="">disable</button>';
                            }
                            else {
                                tags += '<button type="button" name="agentable" title="' + row.username + '" rel="enable" player="' + row.id + '" class="btn btn-danger btn-xs" onfocus="this.blur();" onclick="">enable</button>';
                            }
                        }
                        tags += '</td>';


                        $("#tb_list_0").attr("style", "display: block");
                        $("#d_tip_0").text("Higher Level AgentList");

                        var tblContent = '<tr class="tr_h"><td><a href="/Manage/Management?parentId=' + row.id + '">' + row.username + "</td><td>" + row.score.toFixed(2) + "</td><td>" + row.name + "</td><td>" + row.agent + "</td><td>" + row.tel + "</td><td>" + row.description + "</td>" + tags + "</tr>";
                        $('#tblData_0').append(tblContent.replace(/null/gi, "").replace(/undefined/gi, ""));
                    }
                }

                var row = jsondata["data"];

                if (jsondata["type"] == 1) {
                    var tags = '<td id="op1_0" class="text-left">';
                    if(setScoreLevel == 1){
                        tags += '<button class="btn btn-info btn-xs"  onfocus="this.blur();" onclick="document.location=' + "'/Player/EditScore?id=" + row.id + "'" + '">set score</button>';
                    }
                    tags += '<button class="btn btn-info btn-xs"  onfocus="this.blur();" onclick="document.location=' + "'/ScoreLog/SearchScoreLog?id=" + row.id + "'" + '">score log</button>';
                    if (editUserLevel == 1) {
                        tags += '<button class="btn btn-info btn-xs"  onfocus="this.blur();" onclick="document.location=' + "'/Player/Edit?id=" + row.id + "'" + '">edit</button>';
                    }
                    if (reportLevel == 1) {
                        tags += '<button class="btn btn-info btn-xs"  onfocus="this.blur();" onclick="document.location=' + "'/Report/Search?id=" + row.id + "'" + '">report</button>';
                    }
                    tags += '<button class="btn btn-info btn-xs"  onfocus="this.blur();" onclick="document.location=' + "'/GameLog/SearchGameLog?id=" + row.id + "'" + '">game log</button>';
                    if (enableUserLevel == 1) {
                        tags += '<button class="btn btn-info btn-xs"  name="forcequite" title="' + row.username + '" player="' + row.id + '" onfocus="this.blur();" onclick="">quit game</button>';
                        if (row.state == 1) {
                            tags += '<button type="button" name="able" title="' + row.username + '" rel="disable" player="' + row.id + '" class="btn btn-info btn-xs" onfocus="this.blur();" onclick="">disable</button>';
                        }
                        else {
                            tags += '<button type="button" name="able" title="' + row.username + '" rel ="enable" player="' + row.id + '" class="btn btn-danger btn-xs" onfocus="this.blur();" onclick="">enable</button>';
                        }
                    }
                    tags += '<button class="btn btn-info btn-xs"  onfocus="this.blur();" onclick="document.location=' + "'/BonusLog/SearchBonusLog?id=" + row.id + "'" + '">bonus log</button>';

                    tags += '</td>';

                    $("#tb_list_1").attr("style", "display: block");
                    $("#tb_list_2").attr("style", "display: none");
                    var onlineString = '<span class="badge bg-gray">Disconnected</span>';
                    if (row.isonline == 1)
                        onlineString = '<span class="badge bg-blue-gradient">In Lobby</span>';
                    else if (row.isonline == 2)
                        onlineString = '<span class="badge bg-red">Playing Game</span>';
                    var tblContent = '<tr class="tr_h"><td><b>' + row.username + "</b></td><td>" + row.online + "</td><td>" + onlineString + "</td><td>" + row.agent + "</td><td>" + row.balance.toFixed(2) + "</td><td>" + row.name + "</td><td>" + row.tel + "</td><td>" + row.description + "</td>" + tags + "</tr>";
                    $('#tblData_1').append(tblContent.replace(/null/gi, ""));
                }
                else {
                    var tags = '';
                    if (setScoreLevel == 1) {
                        tags += '<td id="op2_0" class="text-left"><button type="button" class="btn btn-info btn-xs" title="" onfocus="this.blur();" onclick="document.location=' + "'/Agent/EditScore?id=" + row.id + "'" + '"' + '>set score</button>';
                    }
                    tags += '<button type="button" class="btn btn-info btn-xs" title="" onfocus="this.blur();" onclick="document.location=' + "'/ScoreLog/SearchScoreLog?sid=" + row.id + "'" + '"' + '">score log</button>';
                    if (editUserLevel == 1) {
                        tags += '<button type="button" class="btn btn-info btn-xs" title="" onfocus="this.blur();" onclick="document.location=' + "'/Agent/Edit?id=" + row.id + "'" + '">edit</button>';
                    }
                    if (reportLevel == 1) {
                        tags += '<button type="button" class="btn btn-info btn-xs" title="" onfocus="this.blur();" onclick="document.location=' + "'/Report/Search?sid=" + row.id + "'" + '">report</button>';
                        tags += '<button type="button" class="btn btn-info btn-xs" title="" onfocus="this.blur();" onclick="document.location=' + "'/Report/Chart?sid=" + row.id + "'" + '">chart</button>';
                    }
                    if (enableUserLevel == 1) {
                        tags += '<button type="button" name="total" class="btn btn-info btn-xs" title="" onfocus="this.blur();" onclick="">total</button>';
                        if (row.state == 1) {
                            tags += '<button type="button" name="agentable" title="' + row.username + '" rel="disable" player="' + row.id + '" class="btn btn-info btn-xs" onfocus="this.blur();" onclick="">disable</button>';
                        }
                        else {
                            tags += '<button type="button" name="agentable" title="' + row.username + '" rel="enable" player="' + row.id + '" class="btn btn-danger btn-xs" onfocus="this.blur();" onclick="">enable</button>';
                        }
                    }
                    tags += '</td>';

                    $("#tb_list_1").attr("style", "display: none");
                    $("#tb_list_2").attr("style", "display: block");
                    $("#d_tip_1").text(row.username + " " + 'agent list');

                    var tblContent = '<tr class="tr_h"><td><a href="/Manage/Management?parentId=' + row.id + '"><b>' + row.username + "</b></a></td><td>" + row.score.toFixed(2) + "</td><td>" + row.name + "</td><td>" + row.agent + "</td><td>" + row.tel + "</td><td>" + row.description + "</td>" + tags + "</tr>";
                    $('#tblData_2').append(tblContent.replace(/null/gi, "").replace(/undefined/gi, ""));
                }
                $.LoadingOverlay("hide");
            },
            error: function (xhr) {
                if (xhr.status === 401) {
                    window.location.href = "/Account/Login";
                    return;
                }
            },
        });
    }
    $('body').on("click", "button[name='able']", function () {
        var username = $(this).attr("title");
        var state = $(this).attr("rel");
        var alertstr = state + " " + username;
        var data = { id: parseInt($(this).attr("player")) };
        swal({
            title: "Are you sure?",
            text: alertstr,
            type: "info",
            showCancelButton: true,
            closeOnConfirm: false,
            showLoaderOnConfirm: true,
            confirmButtonText: 'OK',
            cancelButtonText: 'Cancel'
        }, function () {
            setTimeout(function () {
                $.ajax({
                    type: "POST",
                    url: "/Player/State",
                    content: "application/json; charset=utf-8",
                    data: data,
                    success: function (d) {
                        document.location.reload();
                    },
                    error: function (xhr) {
                        if (xhr.status === 401) {
                            window.location.href = "/Account/Login";
                            return;
                        }
                    },
                });
                swal({ title: "successfull operation.", confirmButtonText: 'OK' });
            }, 2500);
        });
    });
        $('body').on("click", "button[name='agentable']", function () {
        var username = $(this).attr("title");
        var state = $(this).attr("rel");
        var alertstr = state + " " + username;
        var data = { id: parseInt($(this).attr("player")) };
        swal({
            title: "Are you sure?",
            text: alertstr,
            type: "info",
            showCancelButton: true,
            closeOnConfirm: false,
            showLoaderOnConfirm: true,
            confirmButtonText: 'OK',
            cancelButtonText: 'Cancel'
        }, function () {
            setTimeout(function () {
                $.ajax({
                    type: "POST",
                    url: "/Agent/State",
                    content: "application/json; charset=utf-8",
                    data: data,
                    success: function (d) {
                        document.location.reload();
                    },
                    error: function (xhr) {
                        if (xhr.status === 401) {
                            window.location.href = "/Account/Login";
                            return;
                        }
                    },
                });
                swal({ title: "successfull operation.", confirmButtonText: 'OK' });
            }, 2500);
        });
    });
    $('body').on("click", "button[name='forcequite']", function () {
        var username = $(this).attr("title");
        var alertstr = "Force quite player " + username + "?";
        var data = { id: parseInt($(this).attr("player")) };
        var target = $(this);

        swal({
            title: "Are you sure?",
            text: alertstr,
            type: "warning",
            showCancelButton: true,
            closeOnConfirm: false,
            confirmButtonText: 'OK',
            cancelButtonText: 'Cancel'
        }, function () {
            $.ajax({
                type: "POST",
                url: "/Player/ForceQuite",
                content: "application/json; charset=utf-8",
                data: data,
                success: function (d) {
                    if (d == 1) {
                        swal({ title: "successfull operation.", confirmButtonText: "OK" });
                    }
                    else if (d == -1) {
                        swal({ title: "Player is not online now", confirmButtonText: "OK" });
                    }
                    else {
                        swal({ title: "failed operation.", confirmButtonText: "OK" });
                    }
                },
                error: function (xhr) {
                    if (xhr.status === 401) {
                        window.location.href = "/Account/Login";
                        return;
                    }
                },
            });
        });
    });
    </script> 
  <script type="text/javascript">

    function VaildPassword() {
        var not = checkPassWord($('#password').val())
        if (!not) {
            TipPassword();
        }

        else {
            $('#ppassword').parent().removeClass("has-warning");
            $('#ppassword').parent().addClass("has-success");
            return true;
        }
    }

    function VaildPassword2() {
        var not = checkPassWord($('#password').val())
        if (!not && $('#password').val() != '') {
            TipPassword();
        }

        else {
            $('#ppassword').parent().removeClass("has-warning");
            $('#ppassword').parent().addClass("has-success");
            return true;
        }
    }

    function TipPassword() {
        $('#ppassword').text("Password with minimum 6 characters, must with combination of numbers and alphabets. At least a capital letter and a small letter.");
        $('#ppassword').parent().addClass("has-warning");
        return false;

    }
    function TodayDate() {
        var date = new Date();
        var d = new Date(date),
            month = '' + (d.getMonth() + 1),
            day = '' + d.getDate(),
            year = d.getFullYear();

        if (month.length < 2) month = '0' + month;
        if (day.length < 2) day = '0' + day;

        return [year, month, day].join('-');
    }
    function ValidSetScore() {
        val = $('#setscore').val();

        if (!isFloat(val) && !isInt(val)) {
            $('#pscore').text("eg.: 100 or 10.50")
            scorewarning();
            return false;
        }
        if (val == null || val == "") {
            $('#pscore').text("eg.: 100 or 10.50")
            scorewarning()
            return false;
        }

        if (parseFloat($('#setscore').val()) > parseFloat($('#maxscore').val())) {

            $('#pscore').text("Max value: " + $('#maxscore').val());
            scorewarning();
            return false;

        }

        if (parseFloat($('#setscore').val()) < 0 && Math.abs(parseFloat($('#setscore').val())) > parseFloat($('#curNum').text()))
        {
            $('#pscore').text("Max value: " + $('#curNum').val())
            scorewarning();
            return false;
        }

        else {
            $('#pscore').parent().removeClass('has-warning');
            $('#pscore').parent().addClass('has-success');
            return true;

        }

    }
    function ValidSetScoreCreate() {
        val = $('#setscore').val();

        if (!isFloat(val) && !isInt(val)) {
            $('#pscore').text("eg.: 100 or 10.50")
            scorewarning();
            return false;
        }
        if (val == null || val == "") {
            $('#pscore').text("eg.: 100 or 10.50")
            scorewarning()
            return false;
        }

        if (parseFloat($('#setscore').val()) > parseFloat($('#maxscore').val())) {
            $('#pscore').text("Max value: " + $('#maxscore').val());
            scorewarning();
            return false;

        }

        if (parseFloat($("#setscore").val()) < 0 && $("#isonline").val() == 2) {
            swal({ title: "Player is in game. Cannot withdraw money!", confirmButtonText: 'OK' });
            scorewarning();
            return false;
        }

        if (parseFloat($('#setscore').val()) < 0) {
            $('#pscore').text("Max value: " + $('#maxscore').val())
            scorewarning();
            return false;
        }

        else {
            $('#pscore').parent().removeClass('has-warning');
            $('#pscore').parent().addClass('has-success');
            return true;

        }

    }
    function scorewarning() {
        $('#pscore').text();
        $('#setscore').parent().addClass("has-warning")
        $('#setscore').val("");
    }
    function checkUserName(n) { return /^([a-zA-Z0-9]{1}[a-zA-Z0-9_-]{6,16})+$/.test(n) };
    function checkPassWord(n){return/^(?=.*?[0-9])(?=.*?[A-Z])(?=.*?[a-z])[0-9A-Za-z!)-_]{6,15}$/.test(n)}
    function VaildAgentName() {
        if (!checkUserName($('#username').val()))
        {
            AgentNameWarning();
            return false;
        }
        var url = "/Agent/CheckAgentName"; // the script where you handle the form input.
        var username = $('#username').val();
        $.ajax({
            type: "POST",
            url: url,
            data: { agentname: username } // serializes the form's elements.
        }).done(function (data) {
            if (data == 0) {
                $('#pusername').text("this account exists.");
                $('#pusername').parent().removeClass("has-success");
                $('#pusername').parent().addClass("has-warning");
            }
            if (data == 1) {
                $('#pusername').parent().removeClass("has-warning");
                $('#pusername').parent().addClass("has-success");
                $('#pusername').text("byte length: 7-16 byte.");
            }
        }).fail(function () {
            $('#pusername').text("this account exists.");
            $('#pusername').parent().removeClass("has-success");
            $('#pusername').parent().addClass("has-warning");
        });

        return true;

    }
    function AgentNameWarning() {
        $('#pusername').text("byte length: 7-16 byte.");
        $('#pusername').parent().addClass("has-warning");
        return false;
    }

    function isFloat(val) {
        var floatRegex = /^-?\d+(?:[.,]\d*?)?$/;
        if (!floatRegex.test(val))
            return false;

        val = parseFloat(val);
        if (isNaN(val))
            return false;
        return true;
    }

    /*function CheckPassword(val) {
        var pwd_regex = /(^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)[a-zA-Z\d!@#$%^&*()_-]{6,}$)/;
        if (!pwd_regex.test(val))
            return false;
        return true;
    }*/

    function isInt(val) {
        var intRegex = /^-?\d+$/;
        if (!intRegex.test(val))
            return false;

        var intVal = parseInt(val, 10);
        return parseFloat(val) == intVal && !isNaN(intVal);
    }

    function startInterval() {
        setInterval("startTime();", 1000);
    }

    function startTime() {
        document.getElementById('localtime').innerHTML = getTime();
    }

    function convertUTCDateToLocalDate(dateString) {
        if (dateString == null)
            return "N/A";
        dateString = dateString.replace('T', ' ');
        var day = dateString.split(" ")[0].split("-");
        var time = dateString.split(" ")[1].split(":");
        var date = new Date(day[0], day[1] - 1, day[2], time[0], time[1], time[2]);
        date.setHours(date.getHours() + 8);
        return date.toString("MM/dd/yyyy HH:mm:ss tt");
    }
    function getLocalDateFromUTCTime(dateString) {
        if (dateString == null)
            return "N/A";
        var day = dateString.split(" ")[0].split("-");
        var time = dateString.split(" ")[1].split(":");
        var date = new Date(day[0], day[1] - 1, day[2], time[0], time[1], time[2]);
        date.setHours(date.getHours() + 8);
        return date.toString("yyyy-MM-dd");
    }
    function convertLocalDateToUTCDate(dateString, format) {
        var day = dateString.split(" ")[0].split("-");
        var time = dateString.split(" ")[1].split(":");
        var date = new Date(day[0], day[1] - 1, day[2], time[0], time[1], time[2]);
        //var newDate = new Date(date.getUTCFullYear(), date.getUTCMonth(), date.getUTCDate(), date.getUTCHours(), date.getUTCMinutes(), date.getUTCSeconds());
        if (format == "date")
            return date.toString("yyyy-MM-dd HH:mm:ss");
        else if (format == "time")
            return date.toString("HH:mm:ss");
        else
            return date.toString("yyyy-MM-dd HH:mm:ss");
    }

    //$('#txtName').on('keydown', function (e) {
    //    if ($('#txtName').val().length >= 20)
    //        e.preventDefault();
    //});

    //$('#txtTel').on('keydown', function (e) {
    //    if ($('#txtTel').val().length >= 20)
    //        e.preventDefault();
    //});

    //$('#txtDesc').on('keydown', function (e) {
    //    if ($('#txtDesc').val().length >= 255)
    //        e.preventDefault();
    //});
    function getBonusType(type) {
        switch (type) {
            case 0:
                return "Random";
            case 1:
                return "Minor";
            case 2:
                return "Major";
            default:
                return "Undefined";
        }
    }
    function getLuckyType(type) {
        switch (type) {
            case 0:
                return "Axia";
            case 1:
                return "Oppo A15";
            case 2:
                return "iPhone";
            case 3:
                return "Hongbao-118";
            case 4:
                return "Vivo";
            case 5:
                return "Hongbao-288";
            case 6:
                return "AndroidPhone";
            case 7:
                return "Hongbao-138";
            case 8:
                return "Motorcycle";
            case 9:
                return "Hongbao-88";
            case 10:
                return "Hongbao-8.8";
            default:
                return "Undefined";
        }
    }
    function getProcessed(value) {
        if (value == 0)
            return "Not Processed";
        else
            return "Processed";
    }
    function refreshCountry() {

        var countryDB = document.getElementById("countryDefault").value;
        if (countryDB == null || countryDB == "")
            countryDB = "ANY";

        var optcnt = document.fm.select.options.length;
        for (i = 0 ; i < optcnt; i++) {
            if (document.fm.select.options[i].value == countryDB) {
                document.fm.select.options[i].selected = true;
                break;
            }
        }
    }

    function getSelectedCountry() {
        var optcnt = document.fm.select.options.length;
        for (i = 0 ; i < optcnt; i++) {
            if (document.fm.select.options[i].selected == true) {
                var selectedValue = document.fm.select.options[i].value;
                return selectedValue;
            }
        }

        return "ANY";
    }

    $(document).ready(function () {
        setInterval(function () {
            var time = new Date().toString("yyyy-MM-dd HH:mm:ss");
            $("#localtime").text(time);
        }, 1000);
    });
    $("#time_start").timepicker({
        showInputs: false,
        showSeconds: true,
        showMeridian: false,
        defaultValue: '00:00:00'
    });
    $("#time_start").timepicker("setTime", "00:00:00")
    $("#time_end").timepicker({
        showInputs: false,
        showSeconds: true,
        showMeridian: false,
        defaultValue: '23:59:59'
    });
    $("#time_end").timepicker("setTime", "59:59:59")

</script> 
  <div style="display: none; position: fixed; left: 0px; top: 0px; width: 100%; height: 100%; cursor: move; opacity: 0; background: rgb(255, 255, 255);"></div>
 </body>
</html>
