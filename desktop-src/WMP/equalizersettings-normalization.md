---
title: EQUALIZERSETTINGS. normalizzazione
description: L'attributo di normalizzazione specifica o recupera un valore che indica se la normalizzazione è abilitata.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS. normalizzazione di Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326127"
---
# <a name="equalizersettingsnormalization"></a>EQUALIZERSETTINGS. normalizzazione

L'attributo di **normalizzazione** specifica o recupera un valore che indica se la normalizzazione è abilitata.

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                         |
|-------|-------------------------------------|
| true  | La normalizzazione è abilitata.           |
| false | Valore predefinito. La normalizzazione è disabilitata. |



 

## <a name="remarks"></a>Commenti

Quando è abilitata la normalizzazione, il segnale audio per un intero file multimediale digitale viene scalato fino al valore massimo. In questo modo è possibile riprodurre più file approssimativamente nello stesso volume senza che sia necessario apportare modifiche al volume.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationAverage**](equalizersettings-normalizationaverage.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationPeak**](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





