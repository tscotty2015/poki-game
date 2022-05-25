# Poki Game

Hi

function singleNumber(nums: number[]) {
    const set = new Set();

    for (let i = 0; i < nums.length; i++) {
        const currentValue = nums[i];

        if (set.has(currentValue)) {
            // Get rid of cuttent value
            set.delete(currentValue);
        } else {
            // store current value
            set.add(currentValue);
        }
    }

    let result;
    set.forEach((n) => { result = n });

    return result;
};