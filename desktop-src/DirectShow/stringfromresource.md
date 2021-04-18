---
description: La funzione StringFromResource carica una stringa da un file di risorse con l'identificatore di risorsa specificato.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: Funzione StringFromResource (Wxutil. h)
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
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331917"
---
# <a name="stringfromresource-function"></a>StringFromResource (funzione)

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

Restituisce la stessa stringa di *pbuffer*. Se la funzione ha esito negativo, restituisce una stringa null.

## <a name="remarks"></a>Commenti

Il buffer *pbuffer* deve essere almeno di \_ lunghezza massima di Str \_ byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di supporto della pagina delle proprietà](property-page-helper-functions.md)
</dt> </dl>

 

 




