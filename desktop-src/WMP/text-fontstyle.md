---
title: TEXT. fontStyle
description: L'attributo fontStyle specifica o recupera lo stile del carattere per il controllo di testo.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- Media Player di Windows TEXT. fontStyle
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab6ddfb3ff31cba50027c010ed10c2129d45134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325117"
---
# <a name="textfontstyle"></a>TEXT. fontStyle

L'attributo **FontStyle** specifica o recupera lo stile del carattere per il controllo di testo.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente uno o più dei valori seguenti.



| Valore     | Descrizione                 |
|-----------|-----------------------------|
| Grassetto      | Stile del carattere in grassetto.            |
| Corsivo    | Stile del carattere corsivo.          |
| Sottolineato | Stile del carattere sottolineato.       |
| Barrato | Stile del carattere di attacco.       |
| Normale    | Valore predefinito. Stile del carattere normale. |



 

## <a name="remarks"></a>Commenti

È possibile utilizzare qualsiasi combinazione di valori, separati da spazi. Lo stile normale ha la priorità su tutti gli altri valori, mentre quelli specificati insieme al normale verranno ignorati.

Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> </dl>

 

 





