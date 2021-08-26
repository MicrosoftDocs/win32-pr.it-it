---
description: Il metodo FindPin recupera il pin con l'identificatore specificato.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: Metodo CBaseRenderer.FindPin (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f639e5d68b11b6a7a65ccfe0d0c6465f822d591b0c4dfd0f4916072fde40856
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043771"
---
# <a name="cbaserendererfindpin-method"></a>Metodo CBaseRenderer.FindPin

Il `FindPin` metodo recupera il pin con l'identificatore specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Id* 
</dt> <dd>

Puntatore a una stringa di caratteri wide con terminazione Null costante che identifica il pin. Deve essere L"In".

</dd> <dt>

*ppPin* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin. Se il metodo ha esito negativo, *\* ppPin* è impostato su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                       | Descrizione                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Operazione completata.<br/>                   |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>         | Argomento del puntatore **NULL.**<br/> |
| <dl> <dt>**VFW \_ E \_ NON \_ TROVATO**</dt> </dl> | Non trovato.<br/>                 |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBaseFilter::FindPin.**](cbasefilter-findpin.md) L'unico pin del filtro (il pin di input) è denominato "In".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




