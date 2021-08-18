---
title: TEXT.fontStyle
description: L'attributo fontStyle specifica o recupera lo stile del carattere per il controllo Text.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- Text.fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fbdbe021890b3a76fbae3838cbebe958956af82ff468f990fe6fd9e91345a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762901"
---
# <a name="textfontstyle"></a>TEXT.fontStyle

**L'attributo fontStyle** specifica o recupera lo stile del carattere per il controllo Text.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** contenente uno o più dei valori seguenti.



| Valore     | Descrizione                 |
|-----------|-----------------------------|
| Bold      | Stile carattere grassetto.            |
| Corsivo    | Stile del carattere corsivo.          |
| Sottolineato | Stile del carattere di sottolineatura.       |
| Barrato | Stile del carattere barrato.       |
| Normale    | Valore predefinito. Stile del carattere normale. |



 

## <a name="remarks"></a>Commenti

È possibile usare qualsiasi combinazione di valori, separati da spazi. Lo stile Normale ha la priorità su tutti gli altri valori e tutti gli altri specificati insieme a Normal verranno ignorati.

Vedere [l'attributo value](text-value.md) per un esempio che illustra come vengono usati gli attributi dell'elemento **TEXT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> </dl>

 

 





