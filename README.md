import itertools


def is_prime(num):

    if num < 2:
    
        return False
    
    for i in range(2, int(num**0.5) + 1):
    
        if num % i == 0:
        
            return False
   
    return True



def solution(nums):

    # 가능한 모든 조합 생성
    
    combinations = itertools.combinations(nums, 3)
    
    # 소수인 경우의 개수 카운트
    
    count = 0
    
    for combo in combinations:
    
        if is_prime(sum(combo)):
        
            
            count += 1

    
    
    return count


# 예시 입력

nums = [1, 2, 4, 6, 7]
