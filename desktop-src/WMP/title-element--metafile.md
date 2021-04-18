---
title: Elemento TITLE (Metafile)
description: L'elemento TITLE definisce una stringa di testo che specifica il titolo di un elemento ASX o ENTRY.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- Elemento TITLE (Metafile) Windows Media Player
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331365"
---
# <a name="title-element-metafile"></a>Elemento TITLE (Metafile)

L'elemento **title** definisce una stringa di testo che specifica il titolo di un elemento **ASX** o **entry** .

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
| Elementi padre | **ASX**, **voce** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento definisce una stringa di testo che specifica il titolo di un elemento **ASX** o **entry** . Il titolo viene visualizzato nel pannello di visualizzazione e nella finestra di dialogo **Proprietà** .

Quando questo elemento viene visualizzato all'interno di un elemento **ASX** , il testo viene visualizzato come **Mostra** informazioni. Quando questo elemento viene visualizzato all'interno di un elemento **entry** , il testo viene visualizzato come informazioni di **ritaglio** .

Se un elemento **moreinfo** viene usato anche con l'elemento associato (padre), si tratta del testo del titolo che l'utente fa clic per accedere all'URL definito nell'elemento **moreinfo** .

Ogni elemento **ASX** e **entry** padre deve contenere al massimo un elemento **titolo** figlio. Più elementi **title** dopo il primo verranno ignorati e non verranno visualizzati.

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

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





