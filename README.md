# Unicode Shape Preprocessor Library

Using unicode characters as UI elements is fantastic for a few reasons: 

* As vectors they are scalable and are resolution indipendant
* You can colour them or do anything else you can on text with css
* They reduce the number of images you need
* They could eliminate the need for an icon font. Coupled with not needing images this reduces the number of http requests

The problem I've always had with unicode shapes though is that the unicode numbers are impossible to remember, and I'd need to look them up every time I'd want to use them, which can be a deturrant. So, I created this library as a solution. Instead of needing to remember or lookup unicode entity numbers, I've populated variables for some of the most useful shapes for user interfaces. That way, you can refer to them in your stylesheet with a human-friendly variable name.

I've prefixed all of the variables with ushape_ (short for unicode shape) so that they don't cause trouble with your variables. After that, you can use simple names like rectangle, circle, arrow_right, etc, to use these shapes.

## Languages
I've provided libraries for the following preprocessors

* LESS
* SASS (both .scss and .sass)
* Stylus

## Usage

To use a shape, include the library and place the variable in the CSS content attribute. For example:

	@import "unicode_shapes";

	.more_link {
		&:after {
			content: @ushape_arrow_down;
			}
		}