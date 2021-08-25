---
description: Il metodo ConnectionMediaType recupera il tipo di supporto per la connessione pin corrente, se presente. Questo metodo implementa il metodo IPin::ConnectionMediaType.
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: Metodo CBasePin.ConnectionMediaType (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cdeed52a212a659ca280163ea9513f0cb4f373ea2686bfde00078ebccb183daa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916751"
---
# <a name="cbasepinconnectionmediatype-method"></a>Metodo CBasePin.ConnectionMediaType

Il **metodo ConnectionMediaType** recupera il tipo di supporto per la connessione pin corrente, se presente. Questo metodo implementa il [**metodo IPin::ConnectionMediaType.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntatore a [**una struttura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) che riceve il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili sono quelli riportati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>                   |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>             | Argomento del puntatore **NULL.**<br/> |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Il pin non è connesso.<br/>      |



 

## <a name="remarks"></a>Commenti

Se il pin è connesso, questo metodo copia il tipo di supporto nella struttura [**AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) specificata da *pmt*. Il chiamante deve liberare il blocco di formato del tipo di supporto. È possibile usare la [**funzione CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) o la funzione helper [**FreeMediaType.**](freemediatype.md)

Se il pin non è connesso, questo metodo azzera il blocco di memoria specificato da *pmt* e restituisce un codice di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

