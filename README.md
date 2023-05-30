import requests 
import streamlit as st
from streamlit_lottie import st_lottie

st.set_page_config(page_title="Viral Reach",layout="wide")

def load_lottieurl(url):
    r = requests.get(url)
    if r.status_code !=200:
        return None
    return r.json()

#...animation (lottie files)..
lottie_coding = load_lottieurl("https://assets8.lottiefiles.com/private_files/lf30_oOGQFY.json")

#......heading..
with st.container():
    st.header("VIRAL REACH")
    st.subheader("About us")
    
    st.write("we are a Scial Media Marketing Agency aimed at teaching beginners with zero business experience to start &scale their own agencies to profitable levels") 

#website description + lottie animation ..
with st.container():
    st.write("----")
    left_column,right_column = st.columns(2)
    with right_column:
      st.header("Our Mission")
      st.write("We are on a mission to provide the best online business programs.Our courses aim to deliver 10x the impact on your income ")
      st.write("##")
      st.write("Services offered include;")
      st.write(" -we teach customers how to build & sell an incredible team.")
      st.write(" -we teach on how to manage cashflow,understandcopywriting,paid traffic etc.")
      st.write(" -we also teach the community to manage mindset,structure & habits.")
      st.write("The courses offered are designed to build real entreprenuers.")
    with left_column:
        st_lottie(lottie_coding, height=300, key="finance")   

# CONTACTS... (E-mail address)

with st.container():
    st.write("----")
    st.write("Get in touch with our team today to learn more.")
    st.write("contact us via E-mail account: makubojabez@gmail.com")
