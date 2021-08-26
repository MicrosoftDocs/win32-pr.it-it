---
description: Il metodo SetDrawContext imposta i contesti di dispositivo usati per il disegno.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Metodo CDrawImage.SetDrawContext (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58a10c9f1a485058ed460f4cd30cd4d3894b471415f131d7d4aa59ee757b87d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055971"
---
# <a name="cdrawimagesetdrawcontext-method"></a>Metodo CDrawImage.SetDrawContext

Il `SetDrawContext` metodo imposta i contesti di dispositivo usati per il disegno.

## <a name="syntax"></a>Sintassi


```C++
void SetDrawContext();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo recupera i contesti di dispositivo della finestra e della memoria dall'oggetto [**CBaseWindow**](cbasewindow.md) proprietario. Chiamare questo metodo dopo l'inizializzazione della finestra, ma prima di iniziare a disegnare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




