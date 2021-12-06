arr = ["nap", "teachers", "cheaters", "PAN", "ear", "era", "hectares"]

function aclean(arr) {
  const map = new Map(),
        set = new Set()
  
  arr.forEach(item => {
    map.set(item, item.split('').sort().join(''))
  })
  for(const p of map.values()) set.add(p)
  return set
}

aclean(arr)