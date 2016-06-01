---
title: Change port
ms.custom: na
ms.prod: windows-server-2012
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3d772c90-e849-4e74-b9ec-b6cae1159336
author: Lizap
---
# Change port
Lists or changes the COM port mappings to be compatible with MS\-DOS applications.

For examples of how to use this command, see [Examples](#BKMK_examples).

> [!NOTE]
> [!INCLUDE[rd_note-cmd-line-ref](includes/rd_note-cmd-line-ref_md.md)]

## Syntax

```
change port [<PortX>=<PortY> | /d <PortX> | /query]
```

## Parameters

|Parameter|Description|
|-------------|---------------|
|<PortX>\=<PortY>|Maps COM <*PortX*> to <*PortY*>.|
|\/d <PortX>|Deletes the mapping for COM <*PortX*>.|
|\/query|Displays the current port mappings.|
|\/?|Displays help at the command prompt.|

## Remarks

-   Most MS\-DOS applications support only COM1 through COM4 serial ports. The **change port** command maps a serial port to a different port number, allowing applications that do not support high\-numbered COM ports to access the serial port. Remapping works only for the current session and is not retained if you log off from a session and then log on again.

-   Use **change port** without any parameters to display the available COM ports and their current mappings.

## <a name="BKMK_examples"></a>Examples

-   To map COM12 to COM1 for use by an MS\-DOS\-based application, type:

    ```
    change port com12=com1
    ```

-   To display the current port mappings, type:

    ```
    change port /query
    ```

#### Additional references
[Command-Line Syntax Key](Command-Line-Syntax-Key.md)

[Change](Change.md)

[Remote Desktop Services &#40;Terminal Services&#41; Command Reference](Remote-Desktop-Services--Terminal-Services--Command-Reference.md)

