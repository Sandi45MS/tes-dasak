import streamlit as st
# Load CSS
with open("style.css") as css:
    st.markdown(f"<style>{css.read()}</style>", unsafe_allow_html=True)


st.title("Kalkulator Pertambahan Sederhana")

st.write("Masukkan dua angka untuk dijumlahkan:")

# Input angka
angka1 = st.number_input("Angka pertama", value=0)
angka2 = st.number_input("Angka kedua", value=0)

# Tombol hitung
if st.button("Hitung"):
    hasil = angka1 + angka2
    st.success(f"Hasil pertambahan: {hasil}")
