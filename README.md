# exemple
print('Ассоциативность дизьюнкции')
print("x y z|x or y|(x or y) or z|y or z|x or(y or z)|")
for x in range(2):
    for y in range(2):
        for z in range(2):
           print(x, y, z, '  ', x or y, '     ',(x or y) or z, '         ', y or z, '      ',x or(y or z))
