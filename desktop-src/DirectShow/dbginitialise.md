---
description: La funzione DbgInitialise Inizializza la libreria di debug. Ignorato nelle compilazioni al dettaglio.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: Funzione DbgInitialise (Wxdebug. h)
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
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327526"
---
# <a name="dbginitialise-function"></a>DbgInitialise (funzione)

La funzione **DbgInitialise** Inizializza la libreria di debug. Ignorato nelle compilazioni al dettaglio.

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

In un eseguibile chiamare questo metodo prima di usare le funzionalità di debug DirectShow. Prima che l'eseguibile venga chiuso, chiamare la funzione [**DbgTerminate**](dbgterminate.md) per pulire la libreria di debug.

In una DLL che si collega alla libreria di classi di base (Strmbase. lib), non è necessario chiamare questa funzione. La funzione viene chiamata automaticamente quando viene caricata la DLL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 




