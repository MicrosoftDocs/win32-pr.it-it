---
description: La funzione DbgInitialise inizializza la libreria di debug. Ignorato nelle build per la vendita al dettaglio.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: Funzione DbgInitialise (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13aad8d0214c65c01237c8e74548c3915af9287c935b53e33c6d229b2da5b12e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654216"
---
# <a name="dbginitialise-function"></a>Funzione DbgInitialise

La **funzione DbgInitialise** inizializza la libreria di debug. Ignorato nelle build per la vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hInst* 
</dt> <dd>

Handle per l'istanza del modulo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

In un eseguibile chiamare questo metodo prima di usare le DirectShow di debug. Prima della chiusura del file eseguibile, chiamare [**la funzione DbgTerminate**](dbgterminate.md) per pulire la libreria di debug.

In una DLL collegata alla libreria di classi base (Strmbase.lib), non è necessario chiamare questa funzione. La funzione viene chiamata automaticamente quando viene caricata la DLL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 




