Gold Ring Product Page Documentation
This HTML page displays a gold ring product with dynamic pricing based on metal quality selection. Here's how the data flow works:

Data Structure
The pricing data is stored in a JavaScript object (variantData) within the script tag.Each metal quality (14k, 18k, 22k) has its own pricing configuration including:

Gold price per gram

Gold weight (fixed at 1.5g)

Diamond price (fixed at ₹41,850)

Making charges (fixed amount for each variant)

Data Flow Initialization:
When the page loads (DOMContentLoaded event), the script initializes with 14k gold as default updatePriceBreakup() is called with the 14k variant data

User Interaction:

When user selects a different metal quality from the dropdown, the change event triggers The selected variant's data is retrieved from variantData updatePriceBreakup() is called with the new variant's data

Price Calculation:

Gold price is calculated as price per gram * weight Making charges are applied as fixed amounts (though the code supports percentage-based charges) Total price sums gold value, diamond price, and making charges

Display Update:

All calculated values are formatted with Indian rupee symbols Numbers are formatted with thousand separators using toLocaleString() Values are injected into the price breakdown table cells
