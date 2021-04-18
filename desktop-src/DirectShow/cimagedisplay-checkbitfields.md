---
description: Il metodo CheckBitFields convalida le maschere dei colori in una struttura VIDEOINFO.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Metodo CImageDisplay. CheckBitFields (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade581dad5e53c2454df52e387653e44d6d4ad2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325325"
---
# <a name="cimagedisplaycheckbitfields-method"></a>CImageDisplay. CheckBitFields, metodo

Il `CheckBitFields` metodo convalida le maschere dei colori in una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="syntax"></a>Sintassi


```C++
BOOL CheckBitFields(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInput* 
</dt> <dd>

Puntatore a una struttura **VIDEOINFO** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se le maschere dei colori sono valide o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo verifica che la maschera di colore per ogni componente del colore sia compresa tra uno e otto bit e che ogni maschera di colore sia una sequenza di bit contigua. Chiamare questo metodo solo quando il membro di **biCompression** è impostato su bi \_ campi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




