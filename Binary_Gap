def solution(N):
    # Implement your solution here
    binary_number = bin(N).replace("0b", '')

    if binary_number.count('1') == 1:
        return 0

    if binary_number.count('0') == 0:
        return 0

    # 1100101000000000
    index = 0
    result = []
    while True:
        start = binary_number.find('1', index)
        end = binary_number.find('1', start+1)

        if start == -1 or end == -1:
            break
        
        index = end
        if binary_number[start:end].count('0') > 0:
            result.append(binary_number[start+1:end])

    if not len(result):
        return 0
        
    return len(max(result))
    
assert solution(6) == 0