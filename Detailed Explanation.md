# ⭐ STAR SCHEMA

This project follows a **Star Schema** data model design.

### Fact Table
- **Donations**

### Dimension Tables
- **Donors**
- **Campaigns**
- **Calendar**

The `Donations` fact table stores transactional donation data, while the dimension tables provide descriptive information for donor analysis, campaign tracking, and time-based reporting.

## Donations Table

The `Donations` fact table contains transactional donation records and key information such as:

- `donation_id`
- `donor_id`
- `amount`
- `gift_aid_claimed`

### Additional Calculated Columns

Two additional calculated columns were created:

1. **Gift_Aid_Amount**  
   Calculates an additional 25% of the donation amount when `gift_aid_claimed` is marked as `"Yes"`.

2. **Total_Value**  
   Calculates the total donation value by adding:

   amount + gift_aid_amount

This helps provide a more accurate representation of the total contribution value received from each donation.
