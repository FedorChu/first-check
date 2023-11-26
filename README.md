# first-check
matrix = [
     [' ' , 1, 2, 3]
    ,[1, '-', '-', '-']
    ,[2, '-', '-', '-']
    ,[3, '-', '-', '-']
 ]
matrix1 = [
     [' ' , 1, 2, 3]
    ,[1, '-', '-', '-']
    ,[2, '-', '-', '-']
    ,[3, '-', '-', '-']
 ]

i = 0
k = 1
while 1 > i:
    k = k + 1
    if k % 2 == 0:
        print("ход 1-го игрока ")
        L = int(input('введите номер столбца от 1 до 3: '))
        M = int(input('введите номер строки от 1 до 3: '))

        real_var = input('введите  X')
        matrix[L][M] = real_var

        if matrix[L][M] == matrix1[L][M] or matrix1[L][M] == 'X' or matrix1[L][M] == '0':
            print("Первый игрок в НЕ правильно выбрал ячейку, необходимо заново вести")
            k = k - 1



        else:
            matrix1[L][M] = matrix[L][M]
            #print(matrix)
            x1 = [x[0] for x in matrix]
            x2 = [x[1] for x in matrix]
            x3 = [x[2] for x in matrix]
            x4 = [x[3] for x in matrix]
            print(x1)
            print(x2)
            print(x3)
            print(x4)
            # столбцы
            if matrix[L][M] == matrix[1][1] and matrix[L][M] == matrix[1][2] and matrix[L][M] == matrix[1][3]:
                print("победа 1-го игрока")
                i = i + 2

            if matrix[L][M] == matrix[2][1] and matrix[L][M] == matrix[2][2] and matrix[L][M] == matrix[2][3]:
                print("победа 1-го игрока")
                i = i + 2

            if matrix[L][M] == matrix[3][1] and matrix[L][M] == matrix[3][2] and matrix[L][M] == matrix[3][3]:
                print("победа 1-го игрока")
                i = i + 2

            # сроки
            if matrix[L][M] == matrix[1][1] and matrix[L][M] == matrix[2][1] and matrix[L][M] == matrix[3][1]:
                print("победа 1-го игрока")
                i = i + 2

            if matrix[L][M] == matrix[2][1] and matrix[L][M] == matrix[2][2] and matrix[L][M] == matrix[2][3]:
                print("победа 1-го игрока")
                i = i + 2

            if matrix[L][M] == matrix[3][1] and matrix[L][M] == matrix[3][2] and matrix[L][M] == matrix[3][3]:
                print("победа 1-го игрока")
                i = i + 2


            # диогонали
            if matrix[L][M] == matrix[1][1] and matrix[L][M] == matrix[2][2] and matrix[L][M] == matrix[3][3]:
                print("победа 1-го игрока")
                i = i + 2

            if matrix[L][M] == matrix[3][1] and matrix[L][M] == matrix[2][2] and matrix[L][M] == matrix[3][1]:
                print("победа 1-го игрока")
                i = i + 1



    else:
        print("ход 2-го игрока ")
        L = int(input('введите номер столбца от 1 до 3: '))
        M = int(input('введите номер строки от 1 до 3: '))

        real_var = input('введите  0 ')
        matrix[L][M] = real_var

        if matrix[L][M] == matrix1[L][M] or matrix1[L][M] == 'X' or matrix1[L][M] == '0':
            print("Второй игрок в НЕ правильно выбрал ячейку, необходимо заново вести")
            k = k - 1
            matrix[L][M] = '-'
        else:
            matrix1[L][M] = matrix[L][M]
            x1 = [x[0] for x in matrix]
            x2 = [x[1] for x in matrix]
            x3 = [x[2] for x in matrix]
            x4 = [x[3] for x in matrix]
            print(x1)
            print(x2)
            print(x3)
            print(x4)

            # столбцы
            if matrix[L][M] == matrix[1][1] and matrix[L][M] == matrix[1][2] and matrix[L][M] == matrix[1][3]:
                print("победа 2-го игрока")

                i = i + 1

            if matrix[L][M] == matrix[2][1] and matrix[L][M] == matrix[2][2] and matrix[L][M] == matrix[2][3]:
                print("победа 2-го игрока")
                i = i + 1

            if matrix[L][M] == matrix[3][1] and matrix[L][M] == matrix[3][2] and matrix[L][M] == matrix[3][3]:
                print("победа 2-го игрока")
                i = i + 1

            # сроки
            if matrix[L][M] == matrix[1][1] and matrix[L][M] == matrix[2][1] and matrix[L][M] == matrix[3][1]:
                print("победа 2-го игрока")
                i = i + 1

            if matrix[L][M] == matrix[2][1] and matrix[L][M] == matrix[2][2] and matrix[L][M] == matrix[2][3]:
                print("победа 2-го игрока")
                i = i + 1

            if matrix[L][M] == matrix[3][1] and matrix[L][M] == matrix[3][2] and matrix[L][M] == matrix[3][3]:
                print("победа 2-го игрока")
                i = i + 1


            # диогонали
            if matrix[L][M] == matrix[1][1] and matrix[L][M] == matrix[2][2] and matrix[L][M] == matrix[3][3]:
                print("победа 2-го игрока")
                i = i + 1

            if matrix[L][M] == matrix[3][1] and matrix[L][M] == matrix[2][2] and matrix[L][M] == matrix[3][1]:
                print("победа 2-го игрока")
                i = i + 1
