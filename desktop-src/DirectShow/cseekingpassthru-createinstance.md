---
description: Il metodo CreateInstance crea un'istanza dell'oggetto . Questo metodo supporta la creazione dell'oggetto tramite un class factory. Per altre informazioni, vedere CFactoryTemplate.
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: Metodo CSeekingPassThru.CreateInstance (Seekpt.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5060e2e9842022d89c49e01b56967a92b71c5752e01239fd970c881ccb509cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908061"
---
# <a name="cseekingpassthrucreateinstance-method"></a>Metodo CSeekingPassThru.CreateInstance

Il `CreateInstance` metodo crea un'istanza dell'oggetto . Questo metodo supporta la creazione dell'oggetto tramite un class factory. Per altre informazioni, vedere [**CFactoryTemplate**](cfactorytemplate.md).

## <a name="syntax"></a>Sintassi


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** di aggregazione. In caso contrario, impostare questo parametro su **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **valore HRESULT.** Ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a un nuovo **oggetto CSeekingPassThru.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Seekpt.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSeekingPassThru**](cseekingpassthru.md)
</dt> </dl>

 

 




