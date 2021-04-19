---
title: Elemento multimediale
description: L'elemento media specifica uno degli elementi multimediali in una playlist.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- Elemento multimediale Media Player Windows
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e693c8b17345d3ba7875d48b83b5e3e90d682dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323911"
---
# <a name="media-element"></a>Elemento multimediale

L'elemento **media** specifica uno degli elementi multimediali in una playlist.

``` syntax
<media
    src = "URL"
    cid = "WPL_GUID"
    tid = "WPL_GUID"
>
</media>
```

## <a name="attributes"></a>Attributi



| Termine                                                                                                                       | Descrizione                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (obbligatorio) <br/> | URL di un elemento multimediale.<br/>                                                              |
| <span id="cid"></span><span id="CID"></span>**CID**<br/>                                                             | ID contenuto univoco per questo elemento multimediale.<br/>                                     |
| <span id="tid"></span><span id="TID"></span>**TID**<br/>                                                             | ID di traccia che può essere utilizzato per tenere traccia dell'oggetto file System per questo elemento multimediale.<br/> |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi               |
|-----------|------------------------|
| Padre    | [Seq](seq-element.md) |
| Figlio     | nessuno                   |



 

## <a name="remarks"></a>Osservazioni

L'attributo **CID** (ID contenuto) viene popolato da Windows Media Player come un modo per identificare in modo univoco una porzione di contenuto multimediale anche se gli attributi dei metadati sono stati modificati. Questo consente la condivisione delle playlist tra i computer, perché il contenuto può essere identificato in un altro computer e il percorso può essere "riparato automaticamente" dalla playlist di Windows Media. L'attributo **TID** (ID di traccia) usa il file System Windows per ripristinare automaticamente il percorso del supporto se il nome o il percorso del file viene modificato.

## <a name="examples"></a>Esempio


```
<media
    src = "laure.wma"
    cid = "ABCDEFGH-abcd-1234-WXYZ-ABCDEF000000"
    tid = "12345678-1234-abcd-ABCD-123456abcDEF"
>
</media>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento seq**](seq-element.md)
</dt> <dt>

[**Riferimento agli elementi della playlist Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





