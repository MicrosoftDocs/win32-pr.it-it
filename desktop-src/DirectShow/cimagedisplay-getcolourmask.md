---
description: Il metodo GetColourMask recupera le maschere di colore per il formato di visualizzazione corrente.
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: Metodo CImageDisplay.GetColourMask (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetColourMask
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 018bdaf96e5b6508e13893290449d77041c453b3b28bb4c4d794cc5cc85fb945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655942"
---
# <a name="cimagedisplaygetcolourmask-method"></a>Metodo CImageDisplay.GetColourMask

Il `GetColourMask` metodo recupera le maschere di colore per il formato di visualizzazione corrente.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetColourMask(
   DWORD *pMaskRed,
   DWORD *pMaskGreen,
   DWORD *pMaskBlue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMaskRed* 
</dt> <dd>

Puntatore a una variabile che riceve la maschera del componente rosso.

</dd> <dt>

*pMaskGreen* 
</dt> <dd>

Puntatore a una variabile che riceve la maschera del componente verde.

</dd> <dt>

*pMaskBlue* 
</dt> <dd>

Puntatore a una variabile che riceve la maschera del componente blu.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




