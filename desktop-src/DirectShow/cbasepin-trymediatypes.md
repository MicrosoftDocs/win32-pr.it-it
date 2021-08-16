---
description: Dato un elenco di tipi di supporti, il metodo TryMediaTypes tenta di completare una connessione usando uno di questi tipi.
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: Metodo CBasePin.TryMediaTypes (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.TryMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a4d4e33ca339c1ade344bb2ca9531bea381d14b4381773673b07e522437e90a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108621"
---
# <a name="cbasepintrymediatypes-method"></a>Metodo CBasePin.TryMediaTypes

Dato un elenco di tipi di supporti, `TryMediaTypes` il metodo tenta di completare una connessione usando uno di questi tipi.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT TryMediaTypes(
         IPin            *pReceivePin,
   const CMediaType      *pmt,
         IEnumMediaTypes *pEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntatore all'interfaccia [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di ricezione.

</dd> <dt>

*Pmt* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che limita i possibili tipi di supporti oppure **NULL.**

</dd> <dt>

*pEnum* 
</dt> <dd>

Puntatore a [**un'interfaccia IEnumMediaTypes,**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) usata per enumerare l'elenco dei tipi di supporti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili sono quelli riportati nella tabella seguente.



| Codice restituito                                                                                                  | Descrizione                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Operazione completata.<br/>                               |
| <dl> <dt>**VFW \_ E NESSUN TIPO \_ \_ \_ ACCETTABILE**</dt> </dl> | Non è stato trovato un tipo di supporto accettabile.<br/> |



 

## <a name="remarks"></a>Commenti

Per ogni tipo di supporto restituito **dall'interfaccia IEnumMediaTypes,** questo metodo tenta una connessione chiamando il [**metodo CBasePin::AttemptConnection.**](cbasepin-attemptconnection.md)

Se il *parametro pmt* è diverso da **NULL,** il pin ignora i tipi di supporti che non corrispondono a questo tipo. Il *parametro pmt* può specificare un tipo di supporto parziale. Un tipo di supporto parziale ha un valore NULL GUID \_ per il tipo principale, il sottotipo o il formato. Il valore \_ NULL GUID corrisponde a qualsiasi tipo, simile a un valore "wildcard".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




