<template>
	<div class="default">
		<nav class="navbar navbar-expand-lg navbar-light bg-nav2 justify-content-between ">			
			<button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
				<span class="navbar-toggler-icon"></span>
			</button>				
			<div>
				<div class="collapse navbar-collapse" id="navbarNavDropdown">
					<ul class="navbar-nav">
						<li class="nav-item ">
							<a class="nav-link" href="#"><span class="icon-home"></span></a>
						</li>						
						<li class="nav-item">
							<a class="nav-link" href="#"><span class="icon-people"></span></a>
						</li>
						<li class="nav-item">
							<a class="nav-link" href="#"><span class="icon-bell"></span></a>
						</li>
						<li class="nav-item dropdown">
							<a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
								<span class="icon-settings"></span>
							</a>
							<div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
								<router-link to="/Perfil">
								<a class="dropdown-item" href="#"><span class="icon-user"></span> Perfil</a>
								</router-link>
								<a class="dropdown-item" href="#"><span class="icon-wrench"></span> Configuraciones</a>
								<a class="dropdown-item" href="#"><span class="icon-power"></span> Salir</a>
							</div>
						</li>
					</ul>
				</div>
			</div>		 
			<a class="navbar-brand"></a>
			<form class="form-inline">
				<input class="form-control mr-sm-2" type="search" placeholder="Buscar" aria-label="Buscar">
				<button class="btn btn-outline-info2" type="submit"><span class="icon-magnifier"></span></button>
			</form>
		</nav>
		<div class="row">
			<div class="col-9">
				<main class="main-section">
					<slot name="contentColumn1"></slot>									
				</main>
			</div>
			<div class="col-3 bg-conectados mt-2">
				<main class="main-section ">
					<slot name="contentColumn2"></slot>
					<p>aca va la lista de conectados</p>				
				</main>
			</div>
		</div>	
	</div>
</template>

<script >
export default{
	name:'Layout',
	components:{

	}
}

</script>

<style>
.btn-outline-info2 {
	color: #48dbfb;
	background-color: transparent;
	background-image: none;
	border-color: #48dbfb;
}

.btn-outline-info2:hover {
	color: #fff;
	background-color: #48dbfb;
	border-color: #48dbfb;
}

.bg-nav2{
	background: #f7f7f9!important;
	box-shadow: 2px 2px 5px #999;	
}

.btn{
	background: transparent;
}

.row{
	margin-left: 0px;
	margin-right: 0px;
}

.bg-conectados{
	background: #f7f7f9;
	padding: 0px;
}


</style>