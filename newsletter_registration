#====== Newsletter Registartion ==========
import streamlit as st

st.set_page_config(page_title="Example 2 HCI",
                   layout="wide")

st.title("Example 2")
st.header("Party Registration")
st.subheader("Register for out newsletter")

page_color = """
<style>
 [data-testid="stAppViewContainer"] > .main {{
 background-color: #F1FFFB;}}
 [data-testid="stSidebar"] > div:first-child {{
 background-color: #74DCBE;}}
 [data-testid="stHeader"] {{
 background: rgba(0,0,0,0);
 }}
 </style>
"""

st.sidebar.title("Contact info")
st.sidebar.selectbox("Preferred Contact",options=
                     ["Email", "Phone"])

with st.form("Registration",clear_on_submit=True):
    name = st.text_input("Whats your name: ")
    age = st.text_input("Whats your age: ")
    major = st.selectbox("What is your major: ",
                         options=[
                             "CS", "Law", "Philosophy", "Geology", "Biology"
                         ])
    level = st.radio("What is your level?",
                     options=[
                         "Undergrad", "Grad", "PHD"
                     ])

    subscribed = st.checkbox("Do you wanna know about future events? ")
    submit = st.form_submit_button("Submit")
    if submit and subscribed:
        st.success(f"{name}, {age} old {level} in {major} is now subscribed" )
    elif submit:
        st.warning(f"{name}, {age} old {level} in {major} "
                   f"is still  subscribed to our newsletter!")
    else:
        st.info("Please fill out the form")
