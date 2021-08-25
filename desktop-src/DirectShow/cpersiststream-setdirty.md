---
description: Modifica il flag dirty per il flusso corrente.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: Metodo CPersistStream.SetDirty (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a00de873f33cedd1451ebebd0ec21f1dfaa83690923712d867ec4a8d34d502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909301"
---
# <a name="cpersiststreamsetdirty-method"></a>Metodo CPersistStream.SetDirty

Modifica il flag dirty per il flusso corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fDirty* 
</dt> <dd>

Nuovo flag dirty per questo flusso. **TRUE** indica che i dati non sono stati salvati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pstream.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




