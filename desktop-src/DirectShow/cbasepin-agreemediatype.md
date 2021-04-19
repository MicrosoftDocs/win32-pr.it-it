---
description: Il metodo AgreeMediaType Cerca un tipo di supporto per creare una connessione pin.
ms.assetid: 545186d2-b5e8-4833-b0ff-11160c1dd53b
title: Metodo CBasePin. AgreeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AgreeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e5cdea12cb8bca3319f908fe697251a3d4699d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332783"
---
# <a name="cbasepinagreemediatype-method"></a>CBasePin. AgreeMediaType, metodo

Il `AgreeMediaType` metodo cerca un tipo di supporto per creare una connessione pin.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT AgreeMediaType(
         IPin       *pReceivePin,
   const CMediaType *pmt
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

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica un tipo di supporto o **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                                  | Descrizione                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Esito positivo.<br/>                            |
| <dl> <dt>**VFW \_ E \_ nessun \_ \_ tipo accettabile**</dt> </dl> | Non è stato trovato alcun tipo di supporto accettabile.<br/> |



 

## <a name="remarks"></a>Commenti

Se il parametro *PMT* è non **null** e specifica completamente un tipo di supporto, questo metodo tenta una connessione usando tale tipo di supporto. Se il tentativo ha esito negativo, il metodo restituisce un errore.

Se il parametro *PMT* è **null** o specifica un tipo di supporto parziale, questo metodo tenta i tipi di supporto nell'ordine seguente:

1.  Tipi di supporto preferiti del PIN di destinazione.
2.  Tipi di supporti preferiti del PIN.

I tipi di supporto Preferiti vengono enumerati con il metodo [**CBasePin:: EnumMediaTypes**](cbasepin-enummediatypes.md) e l'enumeratore risultante viene passato al metodo [**CBasePin:: TryMediaTypes**](cbasepin-trymediatypes.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




