---
title: Proprietà Command. LabelDescription
description: Rappresenta una descrizione dell'etichetta.
ms.assetid: 6c683e9e-0742-466e-9fdd-3d29f8ccb9ff
keywords:
- Barra multifunzione di Windows Command. LabelDescription
topic_type:
- apiref
api_name:
- Command.LabelDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f748425b4c8363feee737d18c750b3a1d91121b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964769"
---
# <a name="commandlabeldescription-property"></a>Proprietà Command. LabelDescription

Rappresenta una descrizione dell'etichetta.

## <a name="usage"></a>Utilizzo

``` syntax
<Command.LabelDescription>
  child elements
</Command.LabelDescription>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                   | Descrizione                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**Stringa**](windowsribbon-element-string.md)<br/> | Può verificarsi al massimo una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Comando**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).

**Command. LabelDescription** può contenere un valore di *tipo xs: String* vincolato a qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.

> [!Note]  
> Usare il riferimento al carattere XML UCS (Universal Character Set) `&#xA;` per specificare un'interruzioni di riga.

 

La lunghezza massima è unbounded.

Se non viene specificato alcun valore per **Command. LabelDescription**, l'elemento figlio [**stringa**](windowsribbon-element-string.md) è obbligatorio.

> [!Note]  
> Se **Command. LabelDescription** contiene sia un elemento Value che un elemento figlio [**String**](windowsribbon-element-string.md) , la **stringa** avrà la precedenza.

 

**Command. LabelDescription** supporta solo l'allineamento a sinistra.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato un manifesto di comandi degli Appunti con diverse dichiarazioni **Command. LabelDescription** .


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfaccia utente \_ pkey \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 





