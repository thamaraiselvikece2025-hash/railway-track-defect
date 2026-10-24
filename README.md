# railway-track-defect
An AI_based project to detect railway track surface defects using deep learning and computer vision.
import streamlit as st
from PIL import Image

st.title("Intelligent Railway Track Surface Defect Detection")

st.write(
    "Upload a railway track image for defect analysis."
)

uploaded_file = st.file_uploader(
    "Choose a railway track image",
    type=["jpg", "jpeg", "png"]
)

if uploaded_file is not None:
    image = Image.open(uploaded_file)

    st.image(
        image,
        caption="Uploaded Railway Track Image",
        use_container_width=True
    )

    st.info(
        "Image uploaded successfully. "
        "AI model prediction will be added after training."
    )
