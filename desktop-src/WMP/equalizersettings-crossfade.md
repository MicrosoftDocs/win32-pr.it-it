---
title: EQUALIZERSETTINGS.crossFade
description: L'attributo crossFade specifica o recupera un valore che indica se la dissolvenza incrociata è abilitata.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS.crossFade Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff38ee7634f31da7717bfca015ebaacd88796d9c8186faef155704a449bbb07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838626"
---
# <a name="equalizersettingscrossfade"></a>EQUALIZERSETTINGS.crossFade

**L'attributo crossFade** specifica o recupera un valore che indica se la dissolvenza incrociata è abilitata.

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                      |
|-------|----------------------------------|
| true  | La dissolvenza incrociata è abilitata.           |
| false | Valore predefinito. La dissolvenza incrociata è disabilitata. |



 

## <a name="remarks"></a>Commenti

La dissolvenza incrociata è una funzionalità di elaborazione audio che riduce gradualmente il volume di un elemento multimediale verso la fine della riproduzione, avviando contemporaneamente la riproduzione dell'elemento multimediale successivo al volume minimo e aumentandolo gradualmente al volume normale. La sovrapposizione tra l'inizio del secondo elemento multimediale e la fine del primo elemento multimediale viene specificata **dall'attributo crossFadeWindow.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.crossFadeWindow**](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





