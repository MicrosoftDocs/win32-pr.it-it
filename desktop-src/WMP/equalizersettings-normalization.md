---
title: EQUALIZERSETTINGS.normalization
description: L'attributo di normalizzazione specifica o recupera un valore che indica se la normalizzazione è abilitata.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS.normalization Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f2befdd62f0508822d5547cb3b894b93ea095f52db4cf9bbdb4a444d99251c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578168"
---
# <a name="equalizersettingsnormalization"></a>EQUALIZERSETTINGS.normalization

**L'attributo di** normalizzazione specifica o recupera un valore che indica se la normalizzazione è abilitata.

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                         |
|-------|-------------------------------------|
| true  | La normalizzazione è abilitata.           |
| false | Valore predefinito. La normalizzazione è disabilitata. |



 

## <a name="remarks"></a>Commenti

Quando la normalizzazione è abilitata, il segnale audio per un intero file multimediale digitale viene ridimensionato fino al valore massimo. In questo modo è possibile riprodurre più file approssimativamente allo stesso volume senza richiedere modifiche al volume.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationAverage**](equalizersettings-normalizationaverage.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationPeak**](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





