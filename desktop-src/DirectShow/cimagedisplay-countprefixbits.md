---
description: Il metodo CountPrefixBits calcola il numero di bit zero all'inizio di un campo di bit specificato.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Metodo CImageDisplay.CountPrefixBits (Winutil.h)
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
ms.openlocfilehash: 510ac01baab55fbf45e3441296018426335a8f50061f06400872fd7275d3e273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108481"
---
# <a name="cimagedisplaycountprefixbits-method"></a>Metodo CImageDisplay.CountPrefixBits

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

Specifica un campo di bit come **valore DWORD.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di bit zero che si verificano prima del primo 1 bit o 0x80000000 se tutti i bit sono pari a zero.

## <a name="remarks"></a>Commenti

Questo metodo è utile per l'uso di maschere di colore nelle [**strutture VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




