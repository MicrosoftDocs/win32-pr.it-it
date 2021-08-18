---
description: Il metodo CheckBitFields convalida le maschere di colore in una struttura VIDEOINFO.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Metodo CImageDisplay.CheckBitFields (Winutil.h)
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
ms.openlocfilehash: 44e60b6693dde202cd458cd09495dce9e4bea52ed96a468a8d3dcb6b2370eac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074175"
---
# <a name="cimagedisplaycheckbitfields-method"></a>Metodo CImageDisplay.CheckBitFields

Il `CheckBitFields` metodo convalida le maschere di colore in una struttura [**VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

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

Puntatore a una **struttura VIDEOINFO.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** le maschere di colore sono valide oppure FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

Questo metodo verifica che la maschera colori per ogni componente di colore sia lunga da uno a otto bit e che ogni maschera colori sia una sequenza contigua di bit. Chiamare questo metodo solo quando il **membro biCompression** è impostato su BI \_ BITFIELDS.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




