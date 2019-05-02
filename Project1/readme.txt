What are Channels and Kernels (according to EVA)?

Channels are the features of an image.Its what the image consists of.
Eg: if an image contains Red Green and Blue colors and has just horizontal lines, Red, Green, Blue and Horizontal lines become separate channels
Red - Channel 1, Green - Channel 2, Blue - Channel 3, Horizontal Lines - Channel 4

Kernel
	* Kernel is a matrix which filters out a specific channel in an image.
	* It passes over all the pixels in an image, takes the dot product of the kernel and the image pixels and gives an output which would just have the channel the kernel was supposed to filter.
	* A kernel can filter out just one channel.

Eg: When a Kernel which filters out vertical edges passes over all the pixels in an image(containing vertical (Channel 1) and horizontal edges(Channel 2), the output image will just have vertical edges. 
=================================================================================================================================
Why should we only (well mostly) use 3x3 Kernels?
	* With 3x3 kernels we can get the same result as any higher kernel, (with more number of convolution)

Eg: We can get the same output as Convolving an image with 5x5kernel by Convolving the image with 3x3 kernel twice
	* With smaller kernel size, the network can learn more number of features.
	* 3x3 kernel uses lesser parameters than 5x5 kernel or more to get the same effect

		* When convolution is done on image matrix of 5x5 with kernal of 5x5 we get output of matrix 1x1. The parameters used in this scenario is 5x5=25
		* When convolution is done on image matrix of 5x5 with kernal of 3x3 we get output of matrix 3x3. To get 1x1 the convolution has to be done on the 3x3 matrix again. The number of parameters used in this scenario is (3x3)+(3x3)=18
=================================================================================================================================

How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)We need to perform 3x3 convolution operation  99
	1. 199 x 199 image with 3x3 kernel - After convolution image matrix will be 197 x 197
	2. 197 x 197 image with 3x3 kernel - After convolution image matrix will be 195 x 195
	3. 195 x 195 image with 3x3 kernel - After convolution image matrix will be 193 x 193
	4. 193 x 193 image with 3x3 kernel - After convolution image matrix will be 191 x 191
	5. 191 x 191 image with 3x3 kernel - After convolution image matrix will be 189 x 189
	6. 189 x 189 image with 3x3 kernel - After convolution image matrix will be 187 x 187
	7. 187 x 187 image with 3x3 kernel - After convolution image matrix will be 185 x 185
	8. 185 x 185 image with 3x3 kernel - After convolution image matrix will be 183 x 183
	9. 183 x 183 image with 3x3 kernel - After convolution image matrix will be 181 x 181
	10. 181 x 181 image with 3x3 kernel - After convolution image matrix will be 179 x 179
	11. 179 x 179 image with 3x3 kernel - After convolution image matrix will be 177 x 177
	12. 177 x 177 image with 3x3 kernel - After convolution image matrix will be 175 x 175
	13. 175 x 175 image with 3x3 kernel - After convolution image matrix will be 173 x 173
	14. 173 x 173 image with 3x3 kernel - After convolution image matrix will be 171 x 171
	15. 171 x 171 image with 3x3 kernel - After convolution image matrix will be 169 x 169
	16. 169 x 169 image with 3x3 kernel - After convolution image matrix will be 167 x 167
	17. 167 x 167 image with 3x3 kernel - After convolution image matrix will be 165 x 165
	18. 165 x 165 image with 3x3 kernel - After convolution image matrix will be 163 x 163
	19. 163 x 163 image with 3x3 kernel - After convolution image matrix will be 161 x 161
	20. 161 x 161 image with 3x3 kernel - After convolution image matrix will be 159 x 159
	21. 159 x 159 image with 3x3 kernel - After convolution image matrix will be 157 x 157
	22. 157 x 157 image with 3x3 kernel - After convolution image matrix will be 155 x 155
	23. 155 x 155 image with 3x3 kernel - After convolution image matrix will be 153 x 153
	24. 153 x 153 image with 3x3 kernel - After convolution image matrix will be 151 x 151
	25. 151 x 151 image with 3x3 kernel - After convolution image matrix will be 149 x 149
	26. 149 x 149 image with 3x3 kernel - After convolution image matrix will be 147 x 147
	27. 147 x 147 image with 3x3 kernel - After convolution image matrix will be 145 x 145
	28. 145 x 145 image with 3x3 kernel - After convolution image matrix will be 143 x 143
	29. 143 x 143 image with 3x3 kernel - After convolution image matrix will be 141 x 141
	30. 141 x 141 image with 3x3 kernel - After convolution image matrix will be 139 x 139
	31. 139 x 139 image with 3x3 kernel - After convolution image matrix will be 137 x 137
	32. 137 x 137 image with 3x3 kernel - After convolution image matrix will be 135 x 135
	33. 135 x 135 image with 3x3 kernel - After convolution image matrix will be 133 x 133
	34. 133 x 133 image with 3x3 kernel - After convolution image matrix will be 131 x 131
	35. 131 x 131 image with 3x3 kernel - After convolution image matrix will be 129 x 129
	36. 129 x 129 image with 3x3 kernel - After convolution image matrix will be 127 x 127
	37. 127 x 127 image with 3x3 kernel - After convolution image matrix will be 125 x 125
	38. 125 x 125 image with 3x3 kernel - After convolution image matrix will be 123 x 123
	39. 123 x 123 image with 3x3 kernel - After convolution image matrix will be 121 x 121
	40. 121 x 121 image with 3x3 kernel - After convolution image matrix will be 119 x 119
	41. 119 x 119 image with 3x3 kernel - After convolution image matrix will be 117 x 117
	42. 117 x 117 image with 3x3 kernel - After convolution image matrix will be 115 x 115
	43. 115 x 115 image with 3x3 kernel - After convolution image matrix will be 113 x 113
	44. 113 x 113 image with 3x3 kernel - After convolution image matrix will be 111 x 111
	45. 111 x 111 image with 3x3 kernel - After convolution image matrix will be 109 x 109
	46. 109 x 109 image with 3x3 kernel - After convolution image matrix will be 107 x 107
	47. 107 x 107 image with 3x3 kernel - After convolution image matrix will be 105 x 105
	48. 105 x 105 image with 3x3 kernel - After convolution image matrix will be 103 x 103
	49. 103 x 103 image with 3x3 kernel - After convolution image matrix will be 101 x 101
	50. 101 x 101 image with 3x3 kernel - After convolution image matrix will be 99 x 99
	51. 99 x 99 image with 3x3 kernel - After convolution image matrix will be 97 x 97
	52. 97 x 97 image with 3x3 kernel - After convolution image matrix will be 95 x 95
	53. 95 x 95 image with 3x3 kernel - After convolution image matrix will be 93 x 93
	54. 93 x 93 image with 3x3 kernel - After convolution image matrix will be 91 x 91
	55. 91 x 91 image with 3x3 kernel - After convolution image matrix will be 89 x 89
	56. 89 x 89 image with 3x3 kernel - After convolution image matrix will be 87 x 87
	57. 87 x 87 image with 3x3 kernel - After convolution image matrix will be 85 x 85
	58. 85 x 85 image with 3x3 kernel - After convolution image matrix will be 83 x 83
	59. 83 x 83 image with 3x3 kernel - After convolution image matrix will be 81 x 81
	60. 81 x 81 image with 3x3 kernel - After convolution image matrix will be 79 x 79
	61. 79 x 79 image with 3x3 kernel - After convolution image matrix will be 77 x 77
	62. 77 x 77 image with 3x3 kernel - After convolution image matrix will be 75 x 75
	63. 75 x 75 image with 3x3 kernel - After convolution image matrix will be 73 x 73
	64. 73 x 73 image with 3x3 kernel - After convolution image matrix will be 71 x 71
	65. 71 x 71 image with 3x3 kernel - After convolution image matrix will be 69 x 69
	66. 69 x 69 image with 3x3 kernel - After convolution image matrix will be 67 x 67
	67. 67 x 67 image with 3x3 kernel - After convolution image matrix will be 65 x 65
	68. 65 x 65 image with 3x3 kernel - After convolution image matrix will be 63 x 63
	69. 63 x 63 image with 3x3 kernel - After convolution image matrix will be 61 x 61
	70. 61 x 61 image with 3x3 kernel - After convolution image matrix will be 59 x 59
	71. 59 x 59 image with 3x3 kernel - After convolution image matrix will be 57 x 57
	72. 57 x 57 image with 3x3 kernel - After convolution image matrix will be 55 x 55
	73. 55 x 55 image with 3x3 kernel - After convolution image matrix will be 53 x 53
	74. 53 x 53 image with 3x3 kernel - After convolution image matrix will be 51 x 51
	75. 51 x 51 image with 3x3 kernel - After convolution image matrix will be 49 x 49
	76. 49 x 49 image with 3x3 kernel - After convolution image matrix will be 47 x 47
	77. 47 x 47 image with 3x3 kernel - After convolution image matrix will be 45 x 45
	78. 45 x 45 image with 3x3 kernel - After convolution image matrix will be 43 x 43
	79. 43 x 43 image with 3x3 kernel - After convolution image matrix will be 41 x 41
	80. 41 x 41 image with 3x3 kernel - After convolution image matrix will be 39 x 39
	81. 39 x 39 image with 3x3 kernel - After convolution image matrix will be 37 x 37
	82. 37 x 37 image with 3x3 kernel - After convolution image matrix will be 35 x 35
	83. 35 x 35 image with 3x3 kernel - After convolution image matrix will be 33 x 33
	84. 33 x 33 image with 3x3 kernel - After convolution image matrix will be 31 x 31
	85. 31 x 31 image with 3x3 kernel - After convolution image matrix will be 29 x 29
	86. 29 x 29 image with 3x3 kernel - After convolution image matrix will be 27 x 27
	87. 27 x 27 image with 3x3 kernel - After convolution image matrix will be 25 x 25
	88. 25 x 25 image with 3x3 kernel - After convolution image matrix will be 23 x 23
	89. 23 x 23 image with 3x3 kernel - After convolution image matrix will be 21 x 21
	90. 21 x 21 image with 3x3 kernel - After convolution image matrix will be 19 x 19
	91. 19 x 19 image with 3x3 kernel - After convolution image matrix will be 17 x 17
	92. 17 x 17 image with 3x3 kernel - After convolution image matrix will be 15 x 15
	93. 15 x 15 image with 3x3 kernel - After convolution image matrix will be 13 x 13
	94. 13 x 13 image with 3x3 kernel - After convolution image matrix will be 11 x 11
	95. 11 x 11 image with 3x3 kernel - After convolution image matrix will be 9 x 9
	96. 9 x 9 image with 3x3 kernel - After convolution image matrix will be 7 x 7
	97. 7 x 7 image with 3x3 kernel - After convolution image matrix will be 5 x 5
	98. 5 x 5 image with 3x3 kernel - After convolution image matrix will be 3 x 3
	99. 3 x 3 with 3x3 kernal - After convolution image matrix will be 1 x 1


