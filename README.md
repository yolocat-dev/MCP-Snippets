# MCP-Snippets
Snippets for MCP 1.8.8 (Minecraft Coder Pack)

## Utility Snippets
### [GuiUtils](GuiUtils)
#### Available Features:
Draw Scaled Strings. There are a version which includes shadows. Usage:
```java
void drawScaledString(FontRenderer fr, String str, int x, int y, float scale, int color);
void drawScaledStringWithShadow(FontRenderer fr, String str, int x, int y, float scale, int color);
```
Drawing Hollow Rects, with specified thickness. Usage:
```java
void drawHollowRect(int x, int y, int width, int height, int thickness, int color);
```
Drawing Rounded Rects, available as smooth. Usage:
```java
void drawRoundedRect(int x, int y, int width, int height, float radius, int color);
void drawSmoothRoundedRect(int x, int y, int width, int height, float radius, int color);
```
Draw ChatComponents. Usage:
```java
void drawChatComponent(FontRenderer fr, int x, int y, IChatComponent chatComponent);
void drawChatComponents(FontRenderer fr, int x, int y, IChatComponent[] chatComponents);
```
### [ColorUtils](ColorUtils)
#### Available Features:
Get Chroma Color, with optional speed. Usage:
```java
Color getChromaColor();
Color getChromaColor(long speedMultiplier);
```
Convert Float to Color (0.0f -> 1.0f). Alpha defaults to 1f. Usage:
```java
Color floatToColor(float r, float g, float b);
Color floatToColor(float r, float g, float b, float a);
```
Convert Int to Color (0 -> 255). Alpha defaults to 255. Usage:
```java
Color intToColor(int r, int g, int b);
Color intToColor(int r, int g, int b, int a);
```
### [DesktopUtils](DesktopUtils)
#### Available Features:
Set Borderless Window. Usage:
```java
void setBorderlessWindow(boolean borderless);
```
Get Borderless Window. Usage:
```java
boolean getBorderlessWindow();
```
Set Window Icon. Usage:
```java
void setWindowIcon(ResourceLocation icon16, ResourceLocation icon32);
```
Set Window Title. Usage:
```java
void setWindowTitle(String title);
```
### [SessionChanger](SessionChanger)
You need to change Minecraft.java#session to public and remove the final modifier for this to work.
#### Available Features:
Login with Mojang. Returns the session if needed. Credits to Eric Golde for this. Parameter "changeSession" defaults to true if not specified. Usage:
```java
Session loginMojang(String email, String password);
Session loginMojang(String email, String password, boolean changeSession);
```
Login with Microsoft. This needs a FX version of JDK to work. Zulu JDKFX is recommended. Credits to OpenAuth for the Microsoft Authentication. Parameter "changeSession" defaults to true if not specified. Usage:
```java
Session loginMicrosoft();
Session loginMicrosoft(boolean changeSession);
```
