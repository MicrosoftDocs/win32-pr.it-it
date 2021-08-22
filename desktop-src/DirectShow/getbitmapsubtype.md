---
description: La funzione GetBitmapSubtype restituisce il GUID del sottotipo multimediale per la bitmap specificata.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: Funzione GetBitmapSubtype (Wxutil.h)
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
ms.openlocfilehash: 8903e4a404367327b677a239b8ab28e3cb47e5679203857154f453a5cc01e25e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536681"
---
# <a name="getbitmapsubtype-function"></a>Funzione GetBitmapSubtype

La `GetBitmapSubtype` funzione restituisce il GUID del sottotipo **multimediale** per la bitmap specificata.

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

Puntatore a [**una struttura BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il GUID del sottotipo **multimediale**.

## <a name="remarks"></a>Commenti

Per i tipi RGB non compressi, questa funzione esegue il mapping **del campo biBitCount** al sottotipo. Per i tipi di video compressi, questa funzione usa la [**classe FOURCCMap**](fourccmap.md) per eseguire il mapping **del campo biCompression** al sottotipo.

Se la funzione non può corrispondere al formato di un sottotipo, il valore restituito è NULL \_ GUID.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per video e immagini](video-and-image-functions.md)
</dt> </dl>

 

 




