---
description: La funzione GetBitmapSubtype restituisce il GUID del sottotipo di supporto per la bitmap specificata.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: Funzione GetBitmapSubtype (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ba12ffcd1b50b920f28e1969444a2d31a9d073d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328244"
---
# <a name="getbitmapsubtype-function"></a>GetBitmapSubtype (funzione)

La `GetBitmapSubtype` funzione restituisce il **GUID** del sottotipo di supporto per la bitmap specificata.

## <a name="syntax"></a>Sintassi


```C++
const GUID GetBitmapSubtype(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pHeader* 
</dt> <dd>

Puntatore a una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il **GUID** del sottotipo di supporto.

## <a name="remarks"></a>Commenti

Per i tipi RGB non compressi, questa funzione esegue il mapping del campo **biBitCount** al sottotipo. Per i tipi di video compressi, questa funzione usa la classe [**FOURCCMap**](fourccmap.md) per eseguire il mapping del campo di **biCompression** al sottotipo.

Se la funzione non può corrispondere al formato a un sottotipo, il valore restituito è il GUID \_ null.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni video e immagine](video-and-image-functions.md)
</dt> </dl>

 

 




