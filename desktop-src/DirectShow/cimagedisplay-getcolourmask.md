---
description: Il metodo GetColourMask recupera le maschere dei colori per il formato di visualizzazione corrente.
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: Metodo CImageDisplay. GetColourMask (Winutil. h)
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
ms.openlocfilehash: 499b3677cd68444b58514d692d87cd4f631350b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333074"
---
# <a name="cimagedisplaygetcolourmask-method"></a>CImageDisplay. GetColourMask, metodo

Il `GetColourMask` metodo recupera le maschere dei colori per il formato di visualizzazione corrente.

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

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




