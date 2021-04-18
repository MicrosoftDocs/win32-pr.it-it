---
description: Dato un elenco di tipi di supporto, il metodo TryMediaTypes tenta di completare una connessione usando uno di questi tipi.
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: Metodo CBasePin. TryMediaTypes (Amfilter. h)
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
ms.openlocfilehash: 19b8da39d07b8aae9401bdc6ccf2eecb5d3a1e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327345"
---
# <a name="cbasepintrymediatypes-method"></a>CBasePin. TryMediaTypes, metodo

Dato un elenco di tipi di supporto, il `TryMediaTypes` Metodo prova a completare una connessione usando uno di questi tipi.

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

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di ricezione.

</dd> <dt>

*PMT* 
</dt> <dd>

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che limita i tipi di supporti possibili o **null**.

</dd> <dt>

*pEnum* 
</dt> <dd>

Puntatore a un'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) , usata per enumerare l'elenco dei tipi di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                                  | Descrizione                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Esito positivo.<br/>                               |
| <dl> <dt>**VFW \_ E \_ nessun \_ \_ tipo accettabile**</dt> </dl> | Non è stato trovato alcun tipo di supporto accettabile.<br/> |



 

## <a name="remarks"></a>Commenti

Per ogni tipo di supporto restituito dall'interfaccia **IEnumMediaTypes** , questo metodo tenta una connessione chiamando il metodo [**CBasePin:: AttemptConnection**](cbasepin-attemptconnection.md) .

Se il parametro *PMT* è diverso da **null**, il pin ignora i tipi di supporto che non corrispondono a questo tipo. Il parametro *PMT* può specificare un tipo di supporto parziale. Un tipo di supporto parziale ha un valore GUID \_ null per il tipo principale, il sottotipo o il formato. Il \_ valore null del GUID corrisponde a qualsiasi tipo, simile a un valore "jolly".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




