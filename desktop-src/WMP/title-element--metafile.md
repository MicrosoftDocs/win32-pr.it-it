---
title: Elemento TITLE (metafile)
description: L'elemento TITLE definisce una stringa di testo che specifica il titolo per un elemento ASX o ENTRY.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- Elemento TITLE (metafile) Windows Media Player
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 085bec9a9937c8dbd02fad6df785f4bce7afea90a74117e745f09cb5135633d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117721"
---
# <a name="title-element-metafile"></a>Elemento TITLE (metafile)

**L'elemento TITLE** definisce una stringa di testo che specifica il titolo per **un elemento ASX** **o ENTRY.**

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi           |
|-----------------|--------------------|
| Elementi padre | **ASX**, **ENTRY** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento definisce una stringa di testo che specifica il titolo di un **elemento ASX** **o ENTRY.** Il titolo viene visualizzato nel pannello di visualizzazione e nella **finestra di dialogo** Proprietà.

Quando questo elemento viene visualizzato **all'interno di un elemento ASX,** il testo viene visualizzato come **Mostra** informazioni. Quando questo elemento viene visualizzato all'interno di un **elemento ENTRY,** il testo viene visualizzato come **informazioni clip.**

Se un **elemento MOREINFO** viene usato anche con l'elemento (padre) associato, è il testo del titolo su cui l'utente fa clic per accedere all'URL definito nell'elemento **MOREINFO.**

Ogni elemento **ASX e** **ENTRY** padre deve contenere al massimo un elemento **TITLE** figlio. Più **elementi TITLE** dopo il primo verranno ignorati e non verranno visualizzati.

## <a name="examples"></a>Esempio


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------|
| Versione<br/> | Windows Media Player versione 70 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





