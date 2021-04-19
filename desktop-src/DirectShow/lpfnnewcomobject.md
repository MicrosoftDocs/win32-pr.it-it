---
description: Puntatore a una funzione che crea un'istanza dell'oggetto.
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Puntatore alla funzione LPFNNewCOMObject (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 07c0f8ab961c872c9dc0f92d2fff519b94cd049e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330383"
---
# <a name="lpfnnewcomobject-function-pointer"></a>Puntatore alla funzione LPFNNewCOMObject

Puntatore a una funzione che crea un'istanza dell'oggetto.

## <a name="syntax"></a>Sintassi


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pUnkOuter* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown** dell'oggetto che aggrega il nuovo oggetto, se presente. Questo puntatore può essere **null**.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a un valore **HRESULT** . Se il costruttore ha esito negativo, questo parametro riceve un codice di errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a una nuova istanza dell'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




