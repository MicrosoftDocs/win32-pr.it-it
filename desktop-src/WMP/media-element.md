---
title: Elemento media
description: L'elemento multimediale specifica uno degli elementi multimediali in una playlist.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- Elemento media Windows Media Player
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c67f4321d85ec52babbc6f24c2cd9e3512f7c970eb3360ba2ddfd7ba53f82152
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996321"
---
# <a name="media-element"></a>Elemento media

**L'elemento** multimediale specifica uno degli elementi multimediali in una playlist.

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
| <span id="cid"></span><span id="CID"></span>**Cid**<br/>                                                             | ID contenuto univoco per questo elemento multimediale.<br/>                                     |
| <span id="tid"></span><span id="TID"></span>**Tid**<br/>                                                             | ID di rilevamento che può essere utilizzato per tenere traccia dell'oggetto file system per questo elemento multimediale.<br/> |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi               |
|-----------|------------------------|
| Padre    | [Seq](seq-element.md) |
| Figlio     | nessuno                   |



 

## <a name="remarks"></a>Osservazioni

**L'attributo cid** (ID contenuto) viene popolato dal Windows Media Player per identificare in modo univoco una parte di contenuto multimediale anche se i relativi attributi dei metadati sono stati modificati. Ciò consente la condivisione delle playlist tra computer, perché il contenuto può essere identificato in un altro computer e il percorso può essere "riparato automaticamente" dalla playlist di Windows Media. **L'attributo tid** (ID rilevamento) usa il Windows file system per ripristinare automaticamente il percorso del supporto se il nome o il percorso del file viene modificato.

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
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento seq**](seq-element.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi della playlist multimediale**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





