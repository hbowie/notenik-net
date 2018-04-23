<?output "Notenik ToC.md" ?>
## Table of Contents

<?nextrec?>
<?definegroup 1 =$type$= ?>
<?ifendgroup 1 ?>
<?endif?>
<?ifnewgroup 1 ?>
* =$type$=
<?endif?>
	- [=$title$=](#=$seq$=-=$type&f$=-=$title&f$=)
<?loop?>



