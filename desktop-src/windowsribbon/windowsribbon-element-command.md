---
title: Elemento Command
description: Rappresenta una definizione di comando.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Elemento Command Della barra multifunzione di Windows
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e1df5b62c7b2d7c55345ba8d6da366d04697054
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443482"
---
# <a name="command-element"></a>Elemento Command

Rappresenta una definizione di comando.

## <a name="usage"></a>Utilizzo

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
```

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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
<td><strong>Commento</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Usato per annotare l'elemento di comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Stringa composta da qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.<br/> Lunghezza massima: 250 caratteri.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>xs:positiveInteger union xs:string<br/></td>
<td>No<br/></td>
<td>ID risorsa univoco. <br/> <br/>
<dt><span></span><span></span><strong></strong> (Unione di xs:positiveInteger e xs:string)<br/> </dt> <dd> Valore intero compreso tra 2 e 59999, inclusi o 0x2 e 0xea5f in formato esadecimale, inclusivo. <br/> La lunghezza massima è di 10 caratteri, inclusi gli zeri iniziali facoltativi. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Keytip</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Stringa che rappresenta il tasto di scelta rapida di un elemento di comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Stringa composta da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>LabelDescription</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Stringa che rappresenta il testo visualizzato in un elemento di comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Stringa composta da qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>EtichettaTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Stringa che rappresenta il testo visualizzato in un elemento di comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Stringa composta da qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Nome</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Stringa costituita da una lettera o un carattere di sottolineatura seguito da qualsiasi sequenza di cifre, lettere o caratteri di sottolineatura.<br/> Lunghezza massima: 100 caratteri.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Simbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Stringa costituita da una lettera o un carattere di sottolineatura seguito da qualsiasi sequenza di cifre, lettere o caratteri di sottolineatura.<br/> Lunghezza massima: 100 caratteri.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Descrizione comando</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Stringa che rappresenta il testo visualizzato in un elemento di comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Stringa composta da qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>TooltipTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Stringa che rappresenta il testo visualizzato in un elemento di comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Stringa composta da qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                     | Descrizione                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Command.Comment**](windowsribbon-element-command-comment.md)<br/>                                 | Può verificarsi al massimo una volta<br/> <br/> |
| [**Command.Id**](windowsribbon-element-command-id.md)<br/>                                           | Può verificarsi al massimo una volta<br/> <br/> |
| [**Command.Keytip**](windowsribbon-element-command-keytip.md)<br/>                                   | Può verificarsi al massimo una volta<br/> <br/> |
| [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>               | Può verificarsi al massimo una volta<br/> <br/> |
| [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                           | Può verificarsi al massimo una volta<br/> <br/> |
| [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> | Può verificarsi al massimo una volta<br/> <br/> |
| [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         | Può verificarsi al massimo una volta<br/> <br/> |
| [**Command.Name**](windowsribbon-element-command-name.md)<br/>                                       | Può verificarsi al massimo una volta<br/> <br/> |
| [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | Può verificarsi al massimo una volta<br/> <br/> |
| [**Command.SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         | Può verificarsi al massimo una volta<br/> <br/> |
| [**Command.Symbol**](windowsribbon-element-command-symbol.md)<br/>                                   | Può verificarsi al massimo una volta<br/> <br/> |
| [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/>           | Può verificarsi al massimo una volta<br/> <br/> |
| [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>                       | Può verificarsi al massimo una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                               |
|---------------------------------------------------------------------------------------|
| [**Application.Commands**](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

Può verificarsi una o più volte per ogni [**elemento Application.Commands.**](windowsribbon-element-application-commands.md)

Gli elementi figlio **dell'elemento Command** possono essere presenti in qualsiasi ordine.

In genere, le risorse command vengono dichiarate nel markup della barra multifunzione, ma possono anche essere impostate in fase di esecuzione con una chiamata a [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). Ad esempio, è possibile impostare la proprietà [ \_ PKEY \_ Keytip](windowsribbon-reference-properties-uipkey-keytip.md) dell'interfaccia utente per un oggetto Command anziché dichiarare un valore nel markup con [**l'elemento Command.Keytip.**](windowsribbon-element-command-keytip.md)

Nei casi in cui le proprietà Command, ad esempio etichette e immagini, non possono essere impostate con [**SetUICommandProperty,**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) possono essere invalidate con una chiamata a [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand). Dopo l'invalidazione, il framework esegue una query sull'applicazione host per i dettagli della risorsa.

> [!Note]  
> Una risorsa non può essere ripristinata dalla tabella delle risorse di markup dopo che è stata invalidata.

 

Al file di intestazione di markup della barra multifunzione viene aggiunta una definizione command per **ogni comando** dichiarato nel markup.

Il valore di *Suggerimento tasto* di scelta rapida funge da tasto di scelta rapida per un comando a meno che tale comando non venga esposto tramite una voce di menu. In questo caso, il framework ignora il valore *keytip* e usa invece un carattere preceduto da una e commerciale come specificato da *LabelTitle* o [UI \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md). Se non viene specificata alcuna e commerciale da *LabelTitle* o UI PKEY Label, non viene esposta alcuna descrizione comando o \_ tasto di scelta \_ rapida.

## <a name="examples"></a>Esempio

L'esempio seguente illustra un manifesto degli **elementi Command** per una **scheda** Home.


```XML
<Application.Commands>
```




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




```XML
</Application.Commands>
```



## <a name="element-information"></a>Informazioni sull'elemento

* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** No



 

