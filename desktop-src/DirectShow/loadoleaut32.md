---
description: La funzione LoadOLEAut32 carica la libreria a collegamento dinamico (OleAut32.dll) di automazione.
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: Funzione LoadOLEAut32 (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b23bad7e445eebc78ecf8a849ddde8fc23746131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324784"
---
# <a name="loadoleaut32-function"></a>LoadOLEAut32 (funzione)

La funzione **LoadOLEAut32** carica la libreria a collegamento dinamico (OleAut32.dll) di automazione.

## <a name="syntax"></a>Sintassi


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un handle a un'istanza di DLL di automazione.

## <a name="remarks"></a>Commenti

Quando il distruttore [**CBaseObject**](cbaseobject.md) Elimina l'oggetto che ha caricato OleAut32.dll, la libreria verrà scaricata se ancora caricata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni helper COM**](com-helper-functions.md)
</dt> </dl>

 

 




