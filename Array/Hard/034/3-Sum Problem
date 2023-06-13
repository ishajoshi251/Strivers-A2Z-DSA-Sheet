class Solution:
    def threeSum(self, nums: List[int]) -> List[List[int]]:
        
        nums.sort()  
        if len(nums) < 3:  
            return []
        if nums[0] > 0:  
            return []

        hashMap = {}  
        for i in range(len(nums)):
            hashMap[nums[i]] = i  

        answer = []  
        for i in range(len(nums) - 2):  
            for j in range(i + 1, len(nums) - 1):  
                required = 0-(nums[i]+nums[j])
                if required in hashMap and hashMap[required] > j: 
                    if [nums[i], nums[j], required] not in answer:
                        answer.append([nums[i], nums[j], required])  
        return answer
