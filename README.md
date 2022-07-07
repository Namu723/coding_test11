# 최소 직사각형

def solution(sizes):
    max_x = 0
    max_y = 0

    for i in range(len(sizes)):
        if sizes[i][1] >sizes[i][0]:
            sizes[i][0] ,sizes[i][1] = sizes[i][1] ,sizes[i][0]
    sizes = sorted(sizes, key= lambda x:(x[0],x[1]))
    max_x = list(max(sizes))[0]
    max_y = max(list(zip(*sizes))[1])

    return max_x * max_y

#print(solution([[60, 50], [30, 70], [60, 30], [80, 40]]))
#ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ

def solution(sizes):
    print(max(x) for x in sizes)
    return max(max(x) for x in sizes) * max(min(x) for x in sizes)

