---
description: La funzione DbgDumpObjectRegister visualizza informazioni sugli oggetti attivi. Ignorato nelle build per la vendita al dettaglio.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: Funzione DbgDumpObjectRegister (Wxdebug.h)
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
ms.openlocfilehash: d82d7b419949210e19460880126a07ad52f63ae59f6055e5a2b968a2dd5c7beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821578"
---
# <a name="dbgdumpobjectregister-function"></a>Funzione DbgDumpObjectRegister

La `DbgDumpObjectRegister` funzione visualizza informazioni sugli oggetti attivi. Ignorato nelle build per la vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Nelle build di debug, la libreria di debug gestisce un elenco di oggetti attivi. L'elenco include tutti gli oggetti che derivano da [**CBaseObject**](cbaseobject.md), sono stati creati dal modulo corrente e non sono stati distrutti. I metodi del costruttore e del distruttore **CBaseObject** aggiornano l'elenco.

Questa funzione genera diversi messaggi LOG \_ MEMORY. Al livello di registrazione 1, la funzione visualizza solo il numero totale di oggetti. Al livello di registrazione 2 o superiore, viene visualizzato un elenco degli oggetti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 




