# UASWEB
~~~
Tugas UAS Loket Studio Foto 
Nama : Endrik
NIM : 311910088
Kelas : TI.19.C.1
~~~~
# Link Video Demonstrasi Aplikasi Loket 
https://www.youtube.com/watch?v=6fKTLX9Zz8o

# Link laporan loket 
https://drive.google.com/file/d/1XBRu9BljVit6yHnWglTpjnMMaKpJ05uB/view?usp=sharing

# Persiapan
Start Xampp klik Apache Start mysql Start dan dilanjut klik admin. 
![1](https://user-images.githubusercontent.com/81820421/126879570-4ea142f4-a539-4c03-9e08-7f46acb0556d.png)

# Masuk ke Localhost 
![2](https://user-images.githubusercontent.com/81820421/126879601-7c7addc9-815a-452b-929f-48bf4f6f9f4b.png)
# Buat Folder baru nama loket
Masukan sourcode loket yang sudah disimpan di xammpp/htdocs/loket/loket.sql
![4](https://user-images.githubusercontent.com/81820421/126879670-26a649e4-df09-46ec-97ea-3553b3bd65a7.png)
# Import loket.sql
Setelah diimport ke folder loket akan muncul seperti ini .
![3](https://user-images.githubusercontent.com/81820421/126879689-05d0cd25-bf63-43b0-9f62-79b9a06ed7c8.png)
# Setelah sudah di import dan berhasil
Cek localhost tersebut . Ketik di link : http://localhost/loket/ 
![image](https://user-images.githubusercontent.com/81820421/126879747-64c1ca5b-b14c-4ef5-bc89-9e1cd3709d0d.png)
# Persiapan cek sourcode loke di Sublime 
## Buka aplikasi Sublime 
Open folder loket yang disimpan di C/xammpp/htdocs/loket/  akan muncul seperti ini .
![image](https://user-images.githubusercontent.com/81820421/126879826-7831355e-3ddf-49d4-aecf-191e0ee9751c.png)
~~~
# Host: localhost  (Version: 5.5.5-10.1.9-MariaDB)
# Date: 2017-11-17 11:21:34
# Generator: MySQL-Front 5.3  (Build 4.187)

/*!40101 SET NAMES latin1 */;

#
# Structure for table "agenda"
#

DROP TABLE IF EXISTS `agenda`;
CREATE TABLE `agenda` (
  `id_agenda` int(11) NOT NULL AUTO_INCREMENT,
  `agenda` varchar(255) CHARACTER SET latin1 DEFAULT NULL,
  `file` varchar(150) CHARACTER SET latin1 DEFAULT NULL,
  PRIMARY KEY (`id_agenda`)
) ENGINE=InnoDB AUTO_INCREMENT=4 DEFAULT CHARSET=latin2;

#
# Data for table "agenda"
#

INSERT INTO `agenda` VALUES (1,'Osis','agenda_1510110916.jpg'),(2,'Ga tau','agenda_1510111008.jpg'),(3,'Ini nama agenda','agenda_1510127207.jpg');

#
# Structure for table "instansi"
#

DROP TABLE IF EXISTS `instansi`;
CREATE TABLE `instansi` (
  `id_instansi` int(2) NOT NULL AUTO_INCREMENT,
  `instansi` varchar(50) DEFAULT NULL,
  `telp` varchar(15) DEFAULT NULL,
  `alamat` varchar(200) DEFAULT NULL,
  `logo` varchar(150) DEFAULT NULL,
  PRIMARY KEY (`id_instansi`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=latin1;

#
# Data for table "instansi"
#

INSERT INTO `instansi` VALUES (1,'SMK Informatika Utama','021-321312','Jl. JCC Komplek PLN P2B TJBB No.61 Krukut Limo Depok','logo_1383876609.png');

#
# Structure for table "karyawan"
#

DROP TABLE IF EXISTS `karyawan`;
CREATE TABLE `karyawan` (
  `username` varchar(40) NOT NULL DEFAULT '',
  `nama` varchar(50) DEFAULT NULL,
  `telp` varchar(15) DEFAULT NULL,
  `alamat` varchar(200) DEFAULT NULL,
  `password` varchar(40) DEFAULT NULL,
  `level` varchar(10) DEFAULT NULL,
  `id_loket` int(3) DEFAULT NULL,
  PRIMARY KEY (`username`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

#
# Data for table "karyawan"
#

INSERT INTO `karyawan` VALUES ('aaa','Aaaa','08967987568','Jl. Hkasdas','3b3690fba8bd08059eae130425396eb05ded1b7d','Penjaga',6),('aku','Aku','08384494040','asdas','3b3690fba8bd08059eae130425396eb05ded1b7d','Admin',NULL),('loket1','Loket 1','08984494040','aaa','3b3690fba8bd08059eae130425396eb05ded1b7d','Penjaga',6),('loket2','Loket 2','083823120','Jl. jalan','3b3690fba8bd08059eae130425396eb05ded1b7d','Penjaga',7),('loket3','Loket 3','08343294','Cinere','3b3690fba8bd08059eae130425396eb05ded1b7d','Penjaga',8),('loket4','Loket 4','083458345','Gandul','3b3690fba8bd08059eae130425396eb05ded1b7d','Penjaga',9);

#
# Structure for table "loket"
#

DROP TABLE IF EXISTS `loket`;
CREATE TABLE `loket` (
  `id_loket` int(3) NOT NULL AUTO_INCREMENT,
  `loket` varchar(40) DEFAULT NULL,
  `suara` varchar(150) DEFAULT NULL,
  `status` tinyint(1) DEFAULT '0',
  PRIMARY KEY (`id_loket`)
) ENGINE=InnoDB AUTO_INCREMENT=12 DEFAULT CHARSET=latin1;

#
# Data for table "loket"
#

INSERT INTO `loket` VALUES (6,'1',NULL,0),(7,'2',NULL,0),(8,'3',NULL,0),(9,'4',NULL,0);

#
# Structure for table "text_jalan"
#

DROP TABLE IF EXISTS `text_jalan`;
CREATE TABLE `text_jalan` (
  `id_text` int(11) NOT NULL AUTO_INCREMENT,
  `text` varchar(150) DEFAULT NULL,
  `img` varchar(150) DEFAULT NULL,
  PRIMARY KEY (`id_text`)
) ENGINE=InnoDB AUTO_INCREMENT=6 DEFAULT CHARSET=latin1;

#
# Data for table "text_jalan"
#

INSERT INTO `text_jalan` VALUES (1,'Nasir sayang saropahahaha','text_1510111034.png'),(2,'Saropah sayang alpi','text_1510111058.jpg'),(3,'alpi sayang maymunah','text_1510111073.jpg'),(4,'Karena kau buktikan untukku satu kisah tentang cinta','text_1510125601.png'),(5,'Ayu si tukang ngupil','text_1510127085.jpg');

#
# Structure for table "transaksi"
#

DROP TABLE IF EXISTS `transaksi`;
CREATE TABLE `transaksi` (
  `id_transaksi` int(11) NOT NULL AUTO_INCREMENT,
  `no_antrian` int(11) DEFAULT NULL,
  `id_loket` int(3) NOT NULL DEFAULT '0',
  `username` varchar(40) DEFAULT NULL,
  `tgl` int(8) unsigned zerofill DEFAULT '00000000',
  PRIMARY KEY (`id_transaksi`)
) ENGINE=InnoDB AUTO_INCREMENT=59 DEFAULT CHARSET=latin1;

#
# Data for table "transaksi"
#

INSERT INTO `transaksi` VALUES (19,1,8,'loket3',12112017),(20,2,6,'loket1',12112017),(21,3,6,'loket1',12112017),(22,4,0,NULL,12112017),(23,5,0,NULL,12112017),(24,6,0,NULL,12112017),(25,1,0,NULL,14112017),(26,2,0,NULL,14112017),(27,1,6,'loket1',16112017),(28,2,6,'loket1',16112017),(29,3,7,'loket2',16112017),(30,1,6,'loket1',17112017),(31,2,7,'loket2',17112017),(32,3,8,'loket3',17112017),(33,4,9,'loket4',17112017),(34,5,0,NULL,17112017),(35,6,0,NULL,17112017),(36,7,0,NULL,17112017),(37,8,0,NULL,17112017),(38,9,0,NULL,17112017),(39,10,0,NULL,17112017),(40,11,0,NULL,17112017),(41,12,0,NULL,17112017),(42,13,0,NULL,17112017),(43,14,0,NULL,17112017),(44,15,0,NULL,17112017),(45,16,0,NULL,17112017),(46,17,0,NULL,17112017),(47,18,0,NULL,17112017),(48,19,0,NULL,17112017),(49,20,0,NULL,17112017),(50,21,0,NULL,17112017),(51,22,0,NULL,17112017),(52,23,0,NULL,17112017),(53,24,0,NULL,17112017),(54,25,0,NULL,17112017),(55,26,0,NULL,17112017),(56,27,0,NULL,17112017),(57,28,0,NULL,17112017),(58,29,0,NULL,17112017);
~~~
# Admin 
~~~
<?php
defined('BASEPATH') OR exit('No direct script access allowed');

class Admin extends CI_Controller {
	public function __construct(){
		parent:: __construct();
		$this->load->model('M_crud');
		$this->load->library('pagination');
		$this->load->library('upload');
		if($this->session->userdata('level') !== 'Admin'){
			redirect('welcome/');
		}
	}
	public function index($id=null)
	{
		$data['instansi'] = $this->M_crud->show('instansi', 'id_instansi DESC')->row();
		//$data['perhari'] = $this->M_crud->get_group_id('transaksi', 'tgl')->result();
		$data['content'] = 'admin/laporan';
		$data['menu'] ="admin/menu";
		$data['text_jalan'] = $this->M_crud->show('text_jalan', 'id_text DESC')->result();
		$config['base_url'] 		= site_url('admin/index');
		$config['total_rows']	 	= $this->M_crud->get_group_id('transaksi', 'tgl')->num_rows();
		$config['per_page']			= '6';
		$config['num_links']		= 5;
		$config['full_tag_open']	= '<ul class="pagination">';
		$config['full_tag_close']	= '</ul>';
		$config['first_link']		= 'First';
		$config['last_link']		= 'Last';
		$config['first_tag_open']	= '<li>';
		$config['first_tag_close']	= '</li>';
		$config['prev_link']		= '&laquo';
		$config['prev_tag_open']	= '<li class="prev">';
		$config['porev_tag_close']	= '</li>';
		$config['next_link']		= '&raquo';
		$config['next_tag_open']	= '<li>';
		$config['next_tag_close']	= '</li>';
		$config['last_tag_open']	= '<li>';
		$config['last_tag_close']	= '</li>';
		$config['cur_tag_open']		= '<li class="active"><a href="">';
		$config['cur_tag_close']	= '</a></li>';
		$config['num_tag_open']		= '<li>';
		$config['num_tag_close']	= '</li>';

		$this->pagination->initialize($config);

		// buat pagination
		$data['halaman'] = $this->pagination->create_links();
		$data['hasil'] = $this->M_crud->fetch_data('transaksi', 'tgl', $config['per_page'], $id);
		$this->load->view('layout', $data);
	}

	public function agenda($id=null)
	{
		$data['instansi'] = $this->M_crud->show('instansi', 'id_instansi DESC')->row();
		//$data['perhari'] = $this->M_crud->get_group_id('transaksi', 'tgl')->result();
		$data['content'] = 'admin/agenda';
		$data['menu'] ="admin/menu";
		$data['text_jalan'] = $this->M_crud->show('text_jalan', 'id_text DESC')->result();
		$config['base_url'] 		= site_url('admin/agenda/');
		$config['total_rows']	 	= $this->M_crud->get_group_id('agenda', 'id_agenda')->num_rows();
		$config['per_page']			= '7';
		$config['num_links']		= 5;
		$config['full_tag_open']	= '<ul class="pagination">';
		$config['full_tag_close']	= '</ul>';
		$config['first_link']		= 'First';
		$config['last_link']		= 'Last';
		$config['first_tag_open']	= '<li>';
		$config['first_tag_close']	= '</li>';
		$config['prev_link']		= '&laquo';
		$config['prev_tag_open']	= '<li class="prev">';
		$config['porev_tag_close']	= '</li>';
		$config['next_link']		= '&raquo';
		$config['next_tag_open']	= '<li>';
		$config['next_tag_close']	= '</li>';
		$config['last_tag_open']	= '<li>';
		$config['last_tag_close']	= '</li>';
		$config['cur_tag_open']		= '<li class="active"><a href="">';
		$config['cur_tag_close']	= '</a></li>';
		$config['num_tag_open']		= '<li>';
		$config['num_tag_close']	= '</li>';

		$this->pagination->initialize($config);

		// buat pagination
		$data['halaman'] = $this->pagination->create_links();
		$data['hasil'] = $this->M_crud->fetch_data('agenda', 'id_agenda', $config['per_page'], $id);

		$this->load->view('layout', $data);
	}

	public function karyawan($id=null)
	{
		$data['instansi'] = $this->M_crud->show('instansi', 'id_instansi DESC')->row();
		$data['loket'] = $this->M_crud->show('loket', 'loket ASC');
		//$data['perhari'] = $this->M_crud->get_group_id('transaksi', 'tgl')->result();
		$data['content'] = 'admin/karyawan';
		$data['menu'] ="admin/menu";
		$data['text_jalan'] = $this->M_crud->show('text_jalan', 'id_text DESC')->result();
		$config['base_url'] 		= site_url('admin/karyawan');;
		$config['total_rows']	 	= $this->M_crud->get_group_id('karyawan', 'username')->num_rows();
		$config['per_page']			= '7';
		$config['num_links']		= 5;
		$config['full_tag_open']	= '<ul class="pagination">';
		$config['full_tag_close']	= '</ul>';
		$config['first_link']		= 'First';
		$config['last_link']		= 'Last';
		$config['first_tag_open']	= '<li>';
		$config['first_tag_close']	= '</li>';
		$config['prev_link']		= '&laquo';
		$config['prev_tag_open']	= '<li class="prev">';
		$config['porev_tag_close']	= '</li>';
		$config['next_link']		= '&raquo';
		$config['next_tag_open']	= '<li>';
		$config['next_tag_close']	= '</li>';
		$config['last_tag_open']	= '<li>';
		$config['last_tag_close']	= '</li>';
		$config['cur_tag_open']		= '<li class="active"><a href="">';
		$config['cur_tag_close']	= '</a></li>';
		$config['num_tag_open']		= '<li>';
		$config['num_tag_close']	= '</li>';

		$this->pagination->initialize($config);

		// buat pagination
		$data['halaman'] = $this->pagination->create_links();
		$data['hasil'] = $this->M_crud->fetch_data('karyawan', 'username', $config['per_page'], $id);

		$this->load->view('layout', $data);
	}

	public function loket($id=null)
	{
		$data['instansi'] = $this->M_crud->show('instansi', 'id_instansi DESC')->row();
		//$data['perhari'] = $this->M_crud->get_group_id('transaksi', 'tgl')->result();
		$data['content'] = 'admin/loket';
		$data['menu'] ="admin/menu";
		$data['text_jalan'] = $this->M_crud->show('text_jalan', 'id_text DESC')->result();
		$config['base_url'] 		= site_url('admin/loket/');;
		$config['total_rows']	 	= $this->M_crud->get_group_id('loket', 'id_loket')->num_rows();
		$config['per_page']			= '7';
		$config['num_links']		= 5;
		$config['full_tag_open']	= '<ul class="pagination">';
		$config['full_tag_close']	= '</ul>';
		$config['first_link']		= 'First';
		$config['last_link']		= 'Last';
		$config['first_tag_open']	= '<li>';
		$config['first_tag_close']	= '</li>';
		$config['prev_link']		= '&laquo';
		$config['prev_tag_open']	= '<li class="prev">';
		$config['porev_tag_close']	= '</li>';
		$config['next_link']		= '&raquo';
		$config['next_tag_open']	= '<li>';
		$config['next_tag_close']	= '</li>';
		$config['last_tag_open']	= '<li>';
		$config['last_tag_close']	= '</li>';
		$config['cur_tag_open']		= '<li class="active"><a href="">';
		$config['cur_tag_close']	= '</a></li>';
		$config['num_tag_open']		= '<li>';
		$config['num_tag_close']	= '</li>';

		$this->pagination->initialize($config);

		// buat pagination
		$data['halaman'] = $this->pagination->create_links();
		$data['hasil'] = $this->M_crud->fetch_data('loket', 'id_loket', $config['per_page'], $id);

		$this->load->view('layout', $data);
	}

	public function instansi($id=null)
	{
		$data['instansi'] = $this->M_crud->show('instansi', 'id_instansi DESC')->row();
		//$data['perhari'] = $this->M_crud->get_group_id('transaksi', 'tgl')->result();
		$data['content'] = 'admin/instansi';
		$data['menu'] ="admin/menu";
		$data['text_jalan'] = $this->M_crud->show('text_jalan', 'id_text DESC')->result();
		$data['hasil'] = $this->M_crud->show('instansi', 'id_instansi DESC')->result();

		$this->load->view('layout', $data);
	}

	public function text_jalan($id=null)
	{
		$data['instansi'] = $this->M_crud->show('instansi', 'id_instansi DESC')->row();
		//$data['perhari'] = $this->M_crud->get_group_id('transaksi', 'tgl')->result();
		$data['content'] = 'admin/text_jalan';
		$data['menu'] ="admin/menu";
		$data['text_jalan'] = $this->M_crud->show('text_jalan', 'id_text DESC')->result();
		$config['base_url'] 		= site_url('admin/text_jalan/');
		$config['total_rows']	 	= $this->M_crud->show('text_jalan', 'id_text DESC')->num_rows();
		$config['per_page']			= '7';
		$config['num_links']		= 5;
		$config['full_tag_open']	= '<ul class="pagination">';
		$config['full_tag_close']	= '</ul>';
		$config['first_link']		= 'First';
		$config['last_link']		= 'Last';
		$config['first_tag_open']	= '<li>';
		$config['first_tag_close']	= '</li>';
		$config['prev_link']		= '&laquo';
		$config['prev_tag_open']	= '<li class="prev">';
		$config['porev_tag_close']	= '</li>';
		$config['next_link']		= '&raquo';
		$config['next_tag_open']	= '<li>';
		$config['next_tag_close']	= '</li>';
		$config['last_tag_open']	= '<li>';
		$config['last_tag_close']	= '</li>';
		$config['cur_tag_open']		= '<li class="active"><a href="">';
		$config['cur_tag_close']	= '</a></li>';
		$config['num_tag_open']		= '<li>';
		$config['num_tag_close']	= '</li>';

		$this->pagination->initialize($config);

		// buat pagination
		$data['halaman'] = $this->pagination->create_links();
		$data['hasil'] = $this->M_crud->fetch_data('text_jalan', 'id_text', $config['per_page'], $id);

		$this->load->view('layout', $data);
	}

	public function add_loket(){
		$loket=htmlspecialchars($this->input->post('loket'));
		$status=htmlspecialchars($this->input->post('status'));
		$cek=$this->M_crud->get_id('loket', array('loket' => $loket))->num_rows();
		if($cek > 0){
			echo "<script>alert('Nama Loket Sudah Ada'); location='".site_url('admin/loket/')."' </script>";
		}
		else{
			$this->M_crud->add('loket',  array('loket' => $loket, 'status' => $status));
			redirect('admin/loket/');
		}
	}
	public function edit_loket($id){
		$loket=htmlspecialchars($this->input->post('loket'));
		$status=htmlspecialchars($this->input->post('status'));
		$where=array('id_loket' => $id);
		$this->M_crud->edit('loket', array('loket' => $loket, 'status' => $status), $where);
		redirect('admin/loket');
	}
	public function del_loket($id){
		$where=array('id_loket' => $id);
		$this->M_crud->del('loket', $where);
		redirect('admin/loket/');
	}
	public function edit_instansi($id){
		$instansi=htmlspecialchars($this->input->post('instansi'));
		$telp=htmlspecialchars($this->input->post('telp'));
		$alamat=htmlspecialchars($this->input->post('alamat'));
		$logo = $_FILES['logo']['name'];
		$where=array('id_instansi' => $id);
		if ($logo!='') {
			$cek = $this->M_crud->get_id('instansi', $where);
			list($txt,$ext) = explode(".", $logo);
			$logo_baru	= "logo_".time().".".$ext;
			$path			= "./media/";

			$config['file_name'] = $logo_baru;
			$config['upload_path'] = $path;
			$config['allowed_types'] = 'gif|jpg|png|bmp|jpeg';
			$config['max_size'] = '1050';
			$config['max_width'] = '1024';
			$config['max_height'] = '800';
			$this->upload->initialize($config);
			if (! $this->upload->do_upload('logo')) {
				// pesan error
				echo $path;
				echo $this->upload->display_errors();
				exit;
			}
			else if(file_exists('./media/'.$cek->row('logo'))){
					unlink('./media/'.$cek->row('logo'));
				}
		}
		else{
			$logo_baru	= $this->input->post('logo_lama');
		}
		$data=array('instansi' => $instansi, 'telp' => $telp, 'alamat' => $alamat, 'logo' => $logo_baru);
		$this->M_crud->edit('instansi', $data, $where);
		redirect('admin/instansi');
	}
	public function add_karyawan(){
		$username=$this->input->post('username');
		$nama=$this->input->post('nama');
		$telp=$this->input->post('telp');
		$alamat=$this->input->post('alamat');
		$pass=sha1(md5($this->input->post('password')));
		$level=$this->input->post('level');
		$id_loket =$this->input->post('id_loket');

		$cek=$this->M_crud->get_id('karyawan', array('username' => $username))->num_rows();
		if($cek > 0){
			$this->session->set_flashdata("pesan", "<br><div class='alert alert-danger'>
              		 <p class='text-danger'><center>Username Sudah Ada</center></p></div>");
			redirect('admin/karyawan/');
		}
		else{
			$data=array('username' => $username, 'nama' => $nama, 'telp' => $telp, 'alamat' => $alamat, 'password' => $pass, 'level' => $level, 'id_loket' => $id_loket);
			$this->M_crud->add('karyawan',  $data);
			$this->session->set_flashdata("pesan", "<br><div class='alert alert-success'>
              		 <p class='text-danger'><center>Karyawan berhasil ditambah</center></p></div>");
			redirect('admin/karyawan/');
		}
	}
	public function edit_karyawan(){
		if($this->input->post('password') == ''){
			$pass = $this->input->post('password_lama');
		}
		else{
			$pass = sha1(md5($this->input->post('password')));
		}
		$username = $this->input->post('username');
		$nama = $this->input->post('nama');
		$telp = $this->input->post('telp');
		$alamat = $this->input->post('alamat');
		$level = $this->input->post('level');

		$data = array('nama' => $nama, 'telp' => $telp, 'alamat' => $alamat, 'password' => $pass, 'level' => $level);
		$where = array('username' => $username);
		$this->M_crud->edit('karyawan', $data, $where);

		$this->session->set_flashdata("pesan", "<br><div class='alert alert-success'><center>Data berhasil diupdate</center></div>");
		redirect('admin/karyawan/');
	}
	public function del_karyawan($id){
		$where=array('username' => $id);
		$this->M_crud->del('karyawan', $where);
		$this->session->set_flashdata("pesan", "<br><div class='alert alert-success'><center>Data berhasil dihapus</center></div>");
		redirect('admin/karyawan/');
	}
	public function add_agenda(){
		$media=$_FILES['media']['name'];
		if ($media!='') {
			list($txt,$ext) = explode(".", $media);
			$media_baru	= "agenda_".time().".".$ext;
			$path			= "./media/agenda/";

			$config['file_name'] = $media_baru;
			$config['upload_path'] = $path;
			$config['allowed_types'] = 'gif|jpg|png|bmp|jpeg';
			$config['max_size'] = '10050';
			$this->upload->initialize($config);
			if (! $this->upload->do_upload('media')) {
				// pesan error
				echo $path;
				echo $this->upload->display_errors();
				exit;
			}
		}
		else{
			$media_baru	= "404.png";
		}
		$agenda = $this->input->post('agenda');

		$data = array('agenda' => $agenda, 'file' => $media_baru);
		$this->M_crud->add('agenda', $data);

		$this->session->set_flashdata("pesan", "<br><div class='alert alert-success'><center>Data berhasil ditambah</center></div>");
		redirect('admin/agenda/');
	}

	public function edit_agenda(){
		$id = $this->input->post('id_agenda');
		$where=array('id_agenda' => $id);
		$media=$_FILES['media']['name'];
		if ($media!='') {
			list($txt,$ext) = explode(".", $media);
			$media_baru	= "agenda_".time().".".$ext;
			$path			= "./media/agenda/";

			$config['file_name'] = $media_baru;
			$config['upload_path'] = $path;
			$config['allowed_types'] = 'gif|jpg|png|bmp|jpeg';
			$config['max_size'] = '10050';
			$this->upload->initialize($config);
			if (! $this->upload->do_upload('media')) {
				// pesan error
				echo $path;
				echo $this->upload->display_errors();
				exit;
			}
			$cek = $this->M_crud->get_id('agenda', $where);
			if($cek->row('file') != '404.png'){
				if(file_exists('./media/agenda/'.$cek->row('file'))){
					unlink('./media/agenda/'.$cek->row('file'));
				}
			}
		}
		else{
			$media_baru	= $this->input->post('media_lama');
		}
		$agenda = $this->input->post('agenda');
		
		$data = array('agenda' => $agenda, 'file' => $media_baru);
		$this->M_crud->edit('agenda', $data, $where);

		$this->session->set_flashdata("pesan", "<br><div class='alert alert-success'><center>Data berhasil diupdate</center></div>");
		redirect('admin/agenda/');
	}

	public function del_agenda($id){
		$where=array('id_agenda' => $id);
		$cek = $this->M_crud->get_id('agenda', $where);
		if(file_exists('./media/agenda/'.$cek->row('file'))){
			unlink('./media/agenda/'.$cek->row('file'));
		}
		$this->M_crud->del('agenda', $where);
		$this->session->set_flashdata("pesan", "<br><div class='alert alert-success'><center>Data berhasil dihapus</center></div>");
		redirect('admin/agenda/');
	}

	public function add_text(){
		$media=$_FILES['img']['name'];
		if ($media!='') {
			list($txt,$ext) = explode(".", $media);
			$media_baru	= "text_".time().".".$ext;
			$path			= "./media/agenda/";

			$config['file_name'] = $media_baru;
			$config['upload_path'] = $path;
			$config['allowed_types'] = 'gif|jpg|png|bmp|jpeg';
			$config['max_size'] = '10050';
			$this->upload->initialize($config);
			if (! $this->upload->do_upload('img')) {
				// pesan error
				echo $path;
				echo $this->upload->display_errors();
				exit;
			}
		}
		else{
			$media_baru	= "404.png";
		}
		$text = $this->input->post('text');

		$data = array('text' => $text, 'img' => $media_baru);
		$this->M_crud->add('text_jalan', $data);

		$this->session->set_flashdata("pesan", "<br><div class='alert alert-success'><center>Data berhasil ditambah</center></div>");
		redirect('admin/text_jalan/');
	}

	public function edit_text(){
		$id = $this->input->post('id_text');
		$where=array('id_text' => $id);
		$media=$_FILES['img']['name'];
		if ($media!='') {
			list($txt,$ext) = explode(".", $media);
			$media_baru	= "text_".time().".".$ext;
			$path			= "./media/agenda/";

			$config['file_name'] = $media_baru;
			$config['upload_path'] = $path;
			$config['allowed_types'] = 'gif|jpg|png|bmp|jpeg';
			$config['max_size'] = '10050';
			$this->upload->initialize($config);
			if (! $this->upload->do_upload('img')) {
				// pesan error
				echo $path;
				echo $this->upload->display_errors();
				exit;
			}
			$cek = $this->M_crud->get_id('text_jalan', $where);
			if($cek->row('img') != '404.png'){
				if(file_exists('./media/agenda/'.$cek->row('img'))){
					unlink('./media/agenda/'.$cek->row('img'));
				}
			}
		}
		else{
			$media_baru	= $this->input->post('img_lama');
		}
		$text = $this->input->post('text');
		
		$data = array('text' => $text, 'img' => $media_baru);
		$this->M_crud->edit('text_jalan', $data, $where);

		$this->session->set_flashdata("pesan", "<br><div class='alert alert-success'><center>Data berhasil diupdate</center></div>");
		redirect('admin/text_jalan/');
	}

	public function del_text($id){
		$where=array('id_text' => $id);
		$cek = $this->M_crud->get_id('text_jalan', $where);
		if(file_exists('./media/agenda/'.$cek->row('img'))){
			unlink('./media/agenda/'.$cek->row('img'));
		}
		$this->M_crud->del('text_jalan', $where);
		$this->session->set_flashdata("pesan", "<br><div class='alert alert-success'><center>Data berhasil dihapus</center></div>");
		redirect('admin/text_jalan/');
	}
}

~~~
![image](https://user-images.githubusercontent.com/81820421/126879876-29d5ab01-a45b-42ed-a59e-028a7e865b4c.png)

# Code Penjaga 
~~~
<?php
defined('BASEPATH') OR exit('No direct script access allowed');

class Penjaga extends CI_Controller {
	public function __construct(){
		parent:: __construct();
		$this->load->model('M_crud');
		if($this->session->userdata('level') !== 'Penjaga'){
			redirect('welcome/');
		}
	}
	public function index()
	{
		// $data['instansi'] = $this->M_crud->show('instansi', 'id_instansi DESC')->row();
		// $data['loket'] = $this->M_crud->show('loket', 'loket ASC')->result();
		// $data['content'] = 'pilih_loket';
		// $data['menu'] = 'menu';
		// $data['text_jalan'] = $this->M_crud->show('text_jalan', 'id_text DESC')->result();
		// $this->load->view('layout', $data);
		redirect('penjaga/loket/');
	}
	public function loket()
	{
		$id = $this->session->userdata('loket');
		$data['instansi'] = $this->M_crud->show('instansi', 'id_instansi DESC')->row();
		$data['agenda'] = $this->M_crud->show('agenda', 'id_agenda DESC')->row();
		$data['loket'] = $this->M_crud->get_id('loket', array('id_loket' => $id))->row();
		
		$data['antrian'] = $this->M_crud->get_max_id('transaksi', 'no_antrian', array('id_loket' => $id, 'username' => $this->session->userdata('username'), 'tgl' => date('dmY')))->row();
		$where =array('id_loket <' => 1, 'tgl' => date('dmY'));
		$data['cek'] = $this->M_crud->get_id('transaksi', $where)->result();
		$data['content'] = 'penjaga';
		$data['menu'] = 'menu';
		$data['text_jalan'] = $this->M_crud->show('text_jalan', 'id_text DESC')->result();
		$this->load->view('layout', $data);
	}
	public function antrian_selanjutnya(){
		$tgl = date('dmY');
		$where =array('id_loket <' => 1, 'tgl' => $tgl);
		$antrian = $this->M_crud->get_id('transaksi', $where, 'no_antrian DESC');;
		$data=array('no_antrian' => $antrian->row('no_antrian'), 'id_loket' => $this->session->userdata('loket'), 'username' => $this->session->userdata('username'), 'tgl' => $tgl);
		//$this->M_crud->del('transaksi', array('no_antrian' => $antrian));
		$w=array('id_transaksi' => $antrian->row('id_transaksi'));
		$this->M_crud->edit('transaksi', $data, $w);
		redirect('penjaga/loket/');
	}
}
~~~
![image](https://user-images.githubusercontent.com/81820421/126879916-5275a5be-9902-4f7b-8b0c-63da25c9ee1b.png)

# Sourcode bagian Welcome 
~~~
<?php
defined('BASEPATH') OR exit('No direct script access allowed');

class Penjaga extends CI_Controller {
	public function __construct(){
		parent:: __construct();
		$this->load->model('M_crud');
		if($this->session->userdata('level') !== 'Penjaga'){
			redirect('welcome/');
		}
	}
	public function index()
	{
		// $data['instansi'] = $this->M_crud->show('instansi', 'id_instansi DESC')->row();
		// $data['loket'] = $this->M_crud->show('loket', 'loket ASC')->result();
		// $data['content'] = 'pilih_loket';
		// $data['menu'] = 'menu';
		// $data['text_jalan'] = $this->M_crud->show('text_jalan', 'id_text DESC')->result();
		// $this->load->view('layout', $data);
		redirect('penjaga/loket/');
	}
	public function loket()
	{
		$id = $this->session->userdata('loket');
		$data['instansi'] = $this->M_crud->show('instansi', 'id_instansi DESC')->row();
		$data['agenda'] = $this->M_crud->show('agenda', 'id_agenda DESC')->row();
		$data['loket'] = $this->M_crud->get_id('loket', array('id_loket' => $id))->row();
		
		$data['antrian'] = $this->M_crud->get_max_id('transaksi', 'no_antrian', array('id_loket' => $id, 'username' => $this->session->userdata('username'), 'tgl' => date('dmY')))->row();
		$where =array('id_loket <' => 1, 'tgl' => date('dmY'));
		$data['cek'] = $this->M_crud->get_id('transaksi', $where)->result();
		$data['content'] = 'penjaga';
		$data['menu'] = 'menu';
		$data['text_jalan'] = $this->M_crud->show('text_jalan', 'id_text DESC')->result();
		$this->load->view('layout', $data);
	}
	public function antrian_selanjutnya(){
		$tgl = date('dmY');
		$where =array('id_loket <' => 1, 'tgl' => $tgl);
		$antrian = $this->M_crud->get_id('transaksi', $where, 'no_antrian DESC');;
		$data=array('no_antrian' => $antrian->row('no_antrian'), 'id_loket' => $this->session->userdata('loket'), 'username' => $this->session->userdata('username'), 'tgl' => $tgl);
		//$this->M_crud->del('transaksi', array('no_antrian' => $antrian));
		$w=array('id_transaksi' => $antrian->row('id_transaksi'));
		$this->M_crud->edit('transaksi', $data, $w);
		redirect('penjaga/loket/');
	}
}
~~~
![image](https://user-images.githubusercontent.com/81820421/126879927-36c8263c-8e76-49ff-8389-8dff4178db42.png)
  # Setelah codingan benar dan berhasil . cek untuk aplikasinya apakah berjalan atau tidak .
  ![image](https://user-images.githubusercontent.com/81820421/126879957-3347d415-c808-484e-944a-5e4f99e3e131.png)

# Aplikasi Berhasil


