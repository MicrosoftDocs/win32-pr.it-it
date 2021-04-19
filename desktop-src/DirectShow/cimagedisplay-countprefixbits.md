---
description: Il metodo CountPrefixBits calcola il numero di bit zero all'inizio di un campo di bit specificato.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Metodo CImageDisplay. CountPrefixBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4333e1b0826b4fac7bfff463531b5d2e10704418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330230"
---
# <a name="cimagedisplaycountprefixbits-method"></a>CImageDisplay. CountPrefixBits, metodo

Il `CountPrefixBits` metodo calcola il numero di bit zero all'inizio di un campo di bit specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD CountPrefixBits(
   const DWORD Field
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Campo* 
</dt> <dd>

Specifica un campo di bit come valore **DWORD** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di bit zero che si verificano prima del primo bit o 0x80000000 se tutti i bit sono zero.

## <a name="remarks"></a>Commenti

Questo metodo è utile per lavorare con le maschere dei colori nelle strutture [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




