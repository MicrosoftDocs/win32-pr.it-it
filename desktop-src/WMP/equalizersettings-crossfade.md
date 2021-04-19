---
title: EQUALIZERSETTINGS. dissolvenza
description: L'attributo crossfader specifica o recupera un valore che indica se la dissolvenza incrociata è abilitata.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS. dissolvenza Media Player Windows
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333127"
---
# <a name="equalizersettingscrossfade"></a>EQUALIZERSETTINGS. dissolvenza

L'attributo **crossfader** specifica o recupera un valore che indica se la dissolvenza incrociata è abilitata.

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                      |
|-------|----------------------------------|
| true  | La dissolvenza incrociata è abilitata.           |
| false | Valore predefinito. La dissolvenza incrociata è disabilitata. |



 

## <a name="remarks"></a>Commenti

La dissolvenza incrociata è una funzionalità di elaborazione audio che riduce gradualmente il volume di un elemento multimediale vicino alla fine della riproduzione, avviando contemporaneamente la riproduzione del successivo elemento multimediale al volume minimo e aumentando gradualmente il volume al volume normale. La sovrapposizione tra l'inizio del secondo elemento multimediale e la fine del primo elemento multimediale viene specificata dall'attributo **crossFadeWindow** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.crossFadeWindow**](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





