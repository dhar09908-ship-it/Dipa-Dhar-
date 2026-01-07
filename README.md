def normalize_company_name(company_name):
    """
    Accepts a company name string and returns standardized name:
    'CAF SoftSol India Pvt Ltd.'
    """

    if not company_name or not isinstance(company_name, str):
        return "CAF SoftSol India Pvt Ltd."

    # Convert to lowercase for comparison
    name = company_name.lower()

    # Base standardized name
    standardized_name = "CAF SoftSol India Pvt Ltd."

    # Check if CAF exists in any format
    if "caf" in name:
        return standardized_name

    # If missing CAF but other parts exist
    if "softsol" in name or "solution" in name:
        return standardized_name

    # Default fallback
    return standardized_name
