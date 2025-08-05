array = np.array([[1, -2, 3],[-4, 5, -6]])

# (a)
print("Absolute:\n", np.abs(array))
flat = array.flatten()
print("25th percentile:", np.percentile(flat, 25))
print("50th percentile:", np.percentile(flat, 50))
print("75th percentile:", np.percentile(flat, 75))

print("Row-wise percentile:\n", np.percentile(array, [25, 50, 75], axis=1))
print("Column-wise percentile:\n", np.percentile(array, [25, 50, 75], axis=0))

print("Mean:", flat.mean())
print("Median:", np.median(flat))
print("Std Dev:", np.std(flat))

# (b)
a = np.array([-1.8, -1.6, -0.5, 0.5,1.6, 1.8, 3.0])
print("Floor:", np.floor(a))
print("Ceiling:", np.ceil(a))
print("Trunc:", np.trunc(a))
print("Rounded:", np.round(a))
