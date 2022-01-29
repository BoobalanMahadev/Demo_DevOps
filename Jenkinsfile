@Library('DevOps_Library@master') _
node
{

	stage('Source CheckOut')
    	{
		SourceCheckout("https://github.com/mahendran-indiabees/Demo_DevOps.git","master","GitToken")
	}
	stage('Maven Build')
	{
		BuildMaven("clean install")
	}
	Stage('Upload Artifact')
	{
		UploadArtifacts("war","Demo.war","demo","com.mydemo","nexus_cred","Build-Snapshots")
	}
	
}
