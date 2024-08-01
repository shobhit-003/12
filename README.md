# Button

## Description

The `Button` component provides a versatile way to create different button types for various actions. It supports the following:

*   Standard HTML `<button>` elements
*   Anchor tag links (`<a>`)
*   React Router links (`<Link>`)

You can include icons, control loading states, customize the appearance, and manage click events. 

## Props

| Prop Name     | Type       | Description                                                                                                                | Default Value | Required |
| ------------- | -----------| -------------------------------------------------------------------------------------------------------------------------- | ------------- | -------- |
| `alt`         | String     | Alternative text for the button (useful for accessibility).                                                              | None          | No       |
| `children`    | String     | The text or content to be displayed within the button.                                                                 | None          | No       |
| `className`   | String     | Additional CSS classes to be applied to the button for custom styling.                                                     | None          | No       |
| `disabled`    | Boolean    | Disables the button if set to `true`.                                                                                  | `false`       | No       |
| `href`        | String     | URL for the link, used when `type` is set to 'link'.                                                                 | None          | No       |
| `iconBefore`  | String     | Name of a MingCute icon to display before the button text  (see https://www.mingcute.com/) .                                       | None          | No       |
| `iconAfter`   | String     | Name of a MingCute icon to display after the button text   (see https://www.mingcute.com/) .                                        | None          | No       |
| `loading`     | Boolean    | Indicates if the button is in a loading state. Displays a loading indicator if `true`.                                   | `false`       | No       |
| `onClick`     | Function   | Callback function to be executed when the button is clicked.                                                            | None          | No       |
| `size`        | 'normal'   | Determines the size of the button. Accepted values: 'normal' (default), 'large'.                                          | 'normal'      | No       |
| `to`          | String     | Path for React Router links, used when `type` is set to 'router-link'.                                             | None          | No       |
| `type`        | String     | Specifies the button type. Accepted values: 'button' (default), 'link', 'router-link'.                                   | 'button'      | No       |
| `variant`     | 'primary'  | Sets the button's visual style. Accepted values: 'primary' (default), 'secondary', 'tertiary', 'outline', 'danger', 'ghost'| 'primary'     | No       |

## Examples

```jsx
// Basic button
<Button onClick={() => alert('Clicked!')}>Submit</Button>

// Large primary button with icon and loading state
<Button size="large" variant="primary" loading iconAfter="arrow_right_line">
  Next
</Button>

// Link button (styled as standard link)
<Button type="link" href="[https://www.example.com](https://www.example.com)">Visit Example</Button>

// React Router link button
<Button type="router-link" to="/profile" variant="secondary">
  My Profile
</Button>
