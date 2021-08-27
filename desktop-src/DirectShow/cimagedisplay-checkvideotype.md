---
description: Il metodo CheckVideoType controlla se un formato VIDEOINFO specificato è compatibile con il formato di visualizzazione.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Metodo CImageDisplay.CheckVideoType (Winutil.h)
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
ms.openlocfilehash: de6389e22868fe529b5038fe6be1403748dd5a01d22a242c41f9e6c6b8f86808
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108491"
---
# <a name="cimagedisplaycheckvideotype-method"></a>Metodo CImageDisplay.CheckVideoType

Il `CheckVideoType` metodo verifica se un formato [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) specificato è compatibile con il formato di visualizzazione.

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

Puntatore a una **struttura VIDEOINFO.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il formato è compatibile oppure E \_ INVALIDARG in caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo restituisce S \_ OK se il tipo proposto può essere visualizzato facilmente nelle impostazioni di visualizzazione correnti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




