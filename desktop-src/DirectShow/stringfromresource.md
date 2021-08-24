---
description: La funzione StringFromResource carica una stringa da un file di risorse con l'identificatore di risorsa specificato.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: Funzione StringFromResource (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a12bffb3659bd18f630ce3ff06435a701ed77f8fba2af79b20df6d6b2574ad8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329651"
---
# <a name="stringfromresource-function"></a>Funzione StringFromResource

La `StringFromResource` funzione carica una stringa da un file di risorse con l'identificatore di risorsa specificato.

## <a name="syntax"></a>Sintassi


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBuffer* 
</dt> <dd>

Puntatore alla stringa corrispondente a *iResourceID*.

</dd> <dt>

*iResourceID* 
</dt> <dd>

Identificatore di risorsa della stringa da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la stessa stringa di *pBuffer*. Se la funzione non ha esito positivo, restituisce una stringa Null.

## <a name="remarks"></a>Commenti

Il *buffer pBuffer* deve essere almeno STR \_ MAX LENGTH \_ byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper pagina delle proprietà](property-page-helper-functions.md)
</dt> </dl>

 

 




