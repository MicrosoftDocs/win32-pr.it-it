---
description: La funzione LoadOLEAut32 carica la libreria a collegamento dinamico di Automazione (OleAut32.dll).
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: Funzione LoadOLEAut32 (Combase.h)
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
ms.openlocfilehash: 0ca5832246e90e1df207754dc33380547b8193829394d81e6b2b757fccf79a91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502311"
---
# <a name="loadoleaut32-function"></a>Funzione LoadOLEAut32

La **funzione LoadOLEAut32** carica la libreria a collegamento dinamico di Automazione (OleAut32.dll).

## <a name="syntax"></a>Sintassi


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un handle a un'istanza della DLL di automazione.

## <a name="remarks"></a>Commenti

Quando il [**distruttore CBaseObject**](cbaseobject.md) elimina l'oggetto caricato OleAut32.dll, scarica la libreria se è ancora caricata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni helper COM**](com-helper-functions.md)
</dt> </dl>

 

 




