---
description: Il metodo GetDisplayFormat recupera un formato video che descrive la modalità di visualizzazione corrente.
ms.assetid: 98134704-0453-4090-94de-d92cdf324538
title: Metodo CImageDisplay.GetDisplayFormat (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetDisplayFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8841e95f4097d043e7ef01abdb067c248f43b9295a8c8466ba50f07d23bd7dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074145"
---
# <a name="cimagedisplaygetdisplayformat-method"></a>Metodo CImageDisplay.GetDisplayFormat

Il `GetDisplayFormat` metodo recupera un formato video che descrive la modalità di visualizzazione corrente.

## <a name="syntax"></a>Sintassi


```C++
const VIDEOINFO* GetDisplayFormat();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a una [**struttura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




