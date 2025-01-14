# Implementasi Teori Graf Menggunakan Python

## Deskripsi
Proyek ini bertujuan untuk membuat sistem berbasis Python untuk mempelajari teori graf menggunakan library **NetworkX**. Program ini berisi kelas `Graf` yang memiliki berbagai metode untuk mempermudah analisis graf, seperti menambah simpul (node), menambah sisi (edge), memeriksa keterhubungan, menghitung jalur terpendek, dan menampilkan visualisasi graf.

## Prasyarat
Pastikan Anda memiliki Python dan library berikut diinstal:
- **NetworkX**
- **Matplotlib**

Untuk menginstalnya, gunakan perintah:
```bash
pip install networkx matplotlib
```

## Fitur Utama
Berikut adalah fitur utama yang diimplementasikan dalam program ini:

### 1. `add_node(node)`
Menambah simpul (node) ke dalam graf.

#### Contoh Penggunaan:
```python
graph.add_node(1)
```

### 2. `add_edge(u, v, weight=1)`
Menambah sisi (edge) antara dua simpul dengan bobot (default = 1).

#### Contoh Penggunaan:
```python
graph.add_edge(1, 2, weight=4.5)
```

### 3. `visualize_graph()`
Menampilkan visualisasi graf beserta bobot tiap sisi.

#### Contoh Penggunaan:
```python
graph.visualize_graph()
```

### 4. `shortest_path(start, end)`
Menghitung jalur terpendek antara dua simpul berdasarkan bobot.

#### Contoh Penggunaan:
```python
print(graph.shortest_path(1, 5))
```

### 5. `visual_shortest_path(start, end)`
Menampilkan visualisasi jalur terpendek antara dua simpul dalam graf.

#### Contoh Penggunaan:
```python
graph.visual_shortest_path(1, 5)
```

### 6. `node_degrees()`
Mengembalikan derajat dari setiap simpul dalam graf.

#### Contoh Penggunaan:
```python
print(graph.node_degrees())
```

### 7. `is_connected()`
Memeriksa apakah graf terhubung (semua simpul dapat dijangkau satu sama lain).

#### Contoh Penggunaan:
```python
print(graph.is_connected())
```

### 8. `is_directed()`
Memeriksa apakah graf bersifat berarah.

#### Contoh Penggunaan:
```python
print(graph.is_directed())
```

### 9. `are_adjacent(u, v)`
Memeriksa apakah dua simpul saling bertetangga langsung.

#### Contoh Penggunaan:
```python
print(graph.are_adjacent(1, 3))
```

### 10. `neighbors(node)`
Menemukan semua simpul yang bertetangga langsung dengan simpul tertentu.

#### Contoh Penggunaan:
```python
print(graph.neighbors(3))
```

## Contoh Implementasi
Berikut adalah contoh penggunaan program:

```python
# Membuat objek graf
graph = Graf()

# Menambah node
graph.add_node(1)
graph.add_node(2)
graph.add_node(3)
graph.add_node(4)
graph.add_node(5)

# Menambah edge
graph.add_edge(1, 2, weight=4.5)
graph.add_edge(1, 3, weight=3.2)
graph.add_edge(2, 4, weight=2.7)
graph.add_edge(3, 4, weight=1.8)
graph.add_edge(1, 4, weight=6.7)
graph.add_edge(3, 5, weight=2.7)

# Visualisasi graf
graph.visualize_graph()

# Menampilkan jalur terpendek
print("Jalur terpendek dari 1 ke 5:", graph.shortest_path(1, 5))

# Visualisasi jalur terpendek
graph.visual_shortest_path(1, 5)

# Informasi tambahan
print("Derajat tiap node:", graph.node_degrees())
print("Apakah graf ini terhubung/connected?", graph.is_connected())
print("Apakah graf ini berarah?", graph.is_directed())
print("Apakah node 1 dan 3 bertetangga langsung?", graph.are_adjacent(1, 3))
print("Tetangga node 3:", graph.neighbors(3))
```

## Hasil Visualisasi
- **Graph Visualization**: Visualisasi graf dengan simpul, sisi, dan bobot.
- **Shortest Path Visualization**: Menampilkan jalur terpendek dengan sisi yang disorot berwarna merah.



