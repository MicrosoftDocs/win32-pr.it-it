---
description: Il metodo CheckVideoType controlla se un formato VIDEOINFO specificato è compatibile con il formato di visualizzazione.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Metodo CImageDisplay. CheckVideoType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331642"
---
# <a name="cimagedisplaycheckvideotype-method"></a>CImageDisplay. CheckVideoType, metodo

Il `CheckVideoType` metodo controlla se un formato [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) specificato è compatibile con il formato di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckVideoType(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInput* 
</dt> <dd>

Puntatore a una struttura **VIDEOINFO** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se il formato è compatibile o e \_ INVALIDARG in caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo restituisce \_ OK se è possibile visualizzare facilmente il tipo proposto sotto le impostazioni di visualizzazione correnti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




