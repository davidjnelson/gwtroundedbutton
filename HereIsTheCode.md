I'll check this in when I have time.

--

```
package com.YourApp.client;
import org.cobogw.gwt.user.client.ui.RoundedPanel;
import com.google.gwt.user.client.ui.Button;

public class RoundedButton extends Button
{
	RoundedPanel wrapperPanel;
	public RoundedButton(int padding, String color, String text)
	{
		setText(text);
		removeStyleName("gwt-Button");
		setStyleName("roundedButton");
		wrapperPanel = new RoundedPanel(RoundedPanel.ALL, padding);
		wrapperPanel.setCornerColor(color);
		wrapperPanel.add(this);
	}
	public RoundedPanel getRoundedButtonWithWrapperPanel()
	{
		return wrapperPanel;
	}
}
```

--

```
.roundedButton
{
	background-color: #fff8dc;	
	border-style: none;
}
```