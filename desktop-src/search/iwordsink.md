---
description: Gestisce le parole identificate dalle interruzioni di parola sia durante l'ora dell'indice che durante la query.
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: Interfaccia IWordSink (Search.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 109a852f37f3118cd1012c7385a4f9071fdd2f8867f57036e7607c20fd2dadbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822311"
---
# <a name="iwordsink-interface"></a>Interfaccia IWordSink

Gestisce le parole identificate dalle interruzioni di parola sia durante l'ora dell'indice che durante la query.

## <a name="members"></a>Membri

**L'interfaccia IWordSink** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWordSink** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWordSink** include questi metodi.



| Metodo                                             | Descrizione                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**EndAltPhrase**](iwordsink-endaltphrase.md)     | Indica la fine della frase finale in una sequenza di frasi alternative generate da un word breaker durante l'indice.<br/>  |
| [**PutAltWord**](iwordsink-putaltword.md)         | Inserisce una parola alternativa e la relativa posizione **nell'oggetto IWordSink.**<br/>                                                       |
| [**PutBreak**](iwordsink-putbreak.md)             | Inserisce un'interruzione dopo la parola precedente.<br/>                                                                                       |
| [**PutWord**](iwordsink-putword.md)               | Inserisce una parola e la relativa posizione **nell'oggetto IWordSink.**<br/>                                                                    |
| [**StartAltPhrase**](iwordsink-startaltphrase.md) | Indica il limite tra le frasi in una sequenza di frasi alternative generate da un word breaker durante il tempo di indicizzazione.<br/> |



 

## <a name="remarks"></a>Commenti

Windows Search crea e inizializza istanze **dell'oggetto IWordSink.** **L'oggetto IWordSink** riceve il parametro *fQuery* durante l'inizializzazione e usa questo parametro per determinare il contesto di word breaking in cui viene usato l'oggetto.

[**Le implementazioni di IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) ricevono un puntatore **all'oggetto IWordSink** nel [**metodo IWordBreaker::BreakText.**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Search.h</dt> </dl> |



 

 
