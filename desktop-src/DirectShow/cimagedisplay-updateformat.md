---
description: Il metodo UpdateFormat compila alcuni membri facoltativi della struttura VIDEOINFO.
ms.assetid: 5ca34fa0-eef4-44f5-bbcc-e686e5181d86
title: Metodo CImageDisplay. UpdateFormat (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.UpdateFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6966da171e37e1cc285afc1872d221ca7aad99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328350"
---
# <a name="cimagedisplayupdateformat-method"></a>CImageDisplay. UpdateFormat, metodo

Il `UpdateFormat` metodo compila alcuni membri facoltativi della struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdateFormat(
   VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Puntatore a una struttura **VIDEOINFO** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo imposta i membri **biClrUsed**, **biClrImportant** e **biSizeImage** sui valori corretti e cancella i rettangoli di origine e di destinazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




