---
title: Elemento Tab
description: Rappresenta una scheda di base o contestuale.
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- Elemento Tab Windows barra multifunzione
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 349004f65713160acc75bdb6f77765ad9f0c3034
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625957"
---
# <a name="tab-element"></a>Elemento Tab

Rappresenta una scheda [di base](windowsribbon-controls-tab.md) [o contestuale.](windowsribbon-controls-tabgroup.md)

## <a name="usage"></a>Utilizzo

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
```

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Type</th>
<th>Obbligatoria</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Valido solo se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> è l'elemento padre.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Stringa contenente un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.<br/> Gli spazi vuoti sono validi e ignorati.<br/> Lunghezza massima: 250 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                         | Descrizione                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [**Gruppo**](windowsribbon-element-group.md)<br/>                         | Può verificarsi una o più volte<br/> <br/> |
| [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> | Può verificarsi al massimo una volta<br/> <br/>      |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                             |
|---------------------------------------------------------------------|
| [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md)<br/> |
| [**TabGroup**](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a>Commenti

Obbligatorio.

Deve verificarsi almeno una volta per [**ogni elemento Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md) [**o TabGroup.**](windowsribbon-element-tabgroup.md)

**Tab** supporta le [modalità dell'applicazione](ribbon-applicationmodes.md).

Se [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) è presente per l'elemento **Tab,** è necessaria una voce per ogni elemento [**Group**](windowsribbon-element-group.md) e le relative dimensioni ideali in **ScalingPolicy.IdealSizes.**

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup di base per **l'elemento Tab.**

Questa sezione di codice illustra le **dichiarazioni di comando** tab per una **scheda** Home.


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



Questa sezione di codice illustra le dichiarazioni del controllo **Tab.**


```XML
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```



## <a name="element-information"></a>Informazioni sull'elemento

- **Sistema minimo supportato:** Windows 7 
- **Può essere vuoto:** No



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Tab](windowsribbon-controls-tab.md)
</dt> <dt>

[Controllo Gruppo di schede](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

