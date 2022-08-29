# custom-forms
custom forms removing default appearance, using "focus, placeholder-shown, checked + label and ::after


# Removing default appearance and replace with custom iamge

select {
  -moz-appearance: none;
  -webkit-appearance: none;
  appearance: none;
  background-image: url('../images/arrow.png');
  background-repeat: no-repeat;
  background-position: right;
  background-size: contain;
}


# Using :focus 

/* The right-side border changes when the element is clicked on or tabbed into */
.text-input:focus {
  border-right-width: 5px;
}

# Using placeholder-shown

/* The border becomes dashed when the element's placeholder text is visible */
.text-input:placeholder-shown {
  border-style: dashed;
}

# Using checked + label

/* The font style of the adjacent element changes when the given element is checked */
.checkbox:checked + label {
  color: #999999;
  font-style: italic;
}


# Using ::after

/* When checked, the adjacent element has text insert at the end */
.checkbox:checked + label::after {
  margin-left: 10px;
  font-size: 90%;
  content: '(thanks!)';
}
