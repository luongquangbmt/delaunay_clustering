First open the 2D
Second click on Frame -->New Frame; then select Tile Frame below ( also in the Frame Tab)
two frames will appear together
Click on the empty frame, click File --> Open, open the 3D cube
You should see two frames like this.
![image](https://user-images.githubusercontent.com/58369576/191304535-4a199108-8e4a-44b1-b362-b43699249fd5.png)



Click on Frame --> Match --> Frame > WCS (always do this to get the two images in the same coordinates). Do it all the time so you get the right coordinate system.

click on Frame, a panel show up. Match is somewhere in the middle
![image](https://user-images.githubusercontent.com/58369576/191303911-2b0914a8-81a0-4f1f-8acb-ef84d9e707d3.png)
![Uploading image.png…]()



If you click on the 3D frame, you can slide the Cube window, it will tell you which slice you are in

Click on color: choose the color pallet that you like
Click on scale, choose Zscale (or play around with it to sshow the signal better
Then click on scale parameters, set low to 0 (always); you can vary max value



casa
importfits?
im = importfits(fitsimage='.fits', imagename='ashes_cube')
imrebin(outfile='ashes_cube_rebin', imagename='ashes_cube',factor=[2,2])
exportfits(fitsimage='.fits', imagename='ashes_cube_rebin',velocity=True, dropstokes=True)
