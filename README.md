# Sada

Sada is a Django package designed to handle SadaBiz payment links.

## Installation

To install the package, you can use pip:

```
pip install sada
```

## Usage

After installing the package, you need to add it to your Django project.

In your `settings.py` file, add `sada` to your `INSTALLED_APPS`:

```python
INSTALLED_APPS = [
...
'sada',
...
]
```

Then, include the sada URLconf in your project `urls.py`:

```python
from django.urls import include

urlpatterns = [
...
path('sada/', include('sada.urls')),
...
]
```

Now you can run Django's command to check for any database migrations:

```
python manage.py makemigrations
python manage.py migrate
```

## Models

Sada provides one main model: Product.

- Product represents a product with fields like name, description, active, and metadata.

## Views

Sada provides several views for managing products:

- `ProductListView`: Displays a list of all products.
- `ProductDetailView`: Displays detailed information about a specific product.
- `ProductCreateView`: Allows you to create a new product.
- `ProductUpdateView`: Allows you to update an existing product.
- `ProductDeleteView`: Allows you to delete a product.

These views are accessible via the URLs defined in `sada/urls.py`.

## Templates

Sada provides several templates for displaying products:

- `sada/product_list.html`: Displays a list of all products.
- `sada/product_detail.html`: Displays detailed information about a specific product.
- `sada/product_form.html`: Displays a form for creating or updating a product.
- `sada/product_confirm_delete.html`: Displays a confirmation prompt before deleting a product.

You can customize these templates to suit your needs.

## License

Sada is licensed under the MIT License. For more information, see the [LICENSE](https://github.com/ixarmad/sada/blob/main/LICENSE) file.
