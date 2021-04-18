---
description: La funzione DbgDumpObjectRegister Visualizza informazioni sugli oggetti attivi. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: Funzione DbgDumpObjectRegister (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgDumpObjectRegister
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727d9c00ebbe3d48bb46797a1e27b9dd27c7b2c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327528"
---
# <a name="dbgdumpobjectregister-function"></a>DbgDumpObjectRegister (funzione)

La `DbgDumpObjectRegister` funzione Visualizza informazioni sugli oggetti attivi. Ignorato nelle compilazioni al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Nelle build di debug la libreria di debug gestisce un elenco di oggetti attivi. L'elenco include tutti gli oggetti che derivano da [**CBaseObject**](cbaseobject.md), che sono stati creati dal modulo corrente e che non sono stati eliminati definitivamente. I metodi del costruttore e del distruttore **CBaseObject** aggiornano l'elenco.

Questa funzione genera diversi messaggi di memoria del LOG \_ . Al livello di registrazione 1, la funzione Visualizza solo il numero totale di oggetti. Al livello di registrazione 2 o superiore, viene visualizzato un elenco degli oggetti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 




