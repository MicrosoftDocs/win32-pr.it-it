---
description: Gestisce le parole identificate da interruzioni di parola durante il tempo di indicizzazione e di query.
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: Interfaccia IWordSink (search. h)
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
ms.openlocfilehash: 2eab8eee4f7b07b0f712e68d7ad05b970506b00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306094"
---
# <a name="iwordsink-interface"></a>Interfaccia IWordSink

Gestisce le parole identificate da interruzioni di parola durante il tempo di indicizzazione e di query.

## <a name="members"></a>Membri

L'interfaccia **IWordSink** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWordSink** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWordSink** dispone di questi metodi.



| Metodo                                             | Descrizione                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**EndAltPhrase**](iwordsink-endaltphrase.md)     | Indica la fine della frase finale in una sequenza di frasi alternative generate da un Word breaker in fase di indicizzazione.<br/>  |
| [**PutAltWord**](iwordsink-putaltword.md)         | Inserisce una parola alternativa e la relativa posizione nell'oggetto **IWordSink** .<br/>                                                       |
| [**PutBreak**](iwordsink-putbreak.md)             | Inserisce un'interruzioni dopo la parola precedente.<br/>                                                                                       |
| [**PutWord**](iwordsink-putword.md)               | Inserisce una parola e la relativa posizione nell'oggetto **IWordSink** .<br/>                                                                    |
| [**StartAltPhrase**](iwordsink-startaltphrase.md) | Indica il limite tra le frasi in una sequenza di frasi alternative generate da un Word breaker durante l'esecuzione dell'indice.<br/> |



 

## <a name="remarks"></a>Commenti

Windows Search crea e inizializza le istanze dell'oggetto **IWordSink** . L'oggetto **IWordSink** riceve il parametro *fQuery* durante l'inizializzazione e usa questo parametro per determinare il contesto di suddivisione delle parole in cui viene usato l'oggetto.

Le implementazioni [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) ricevono un puntatore all'oggetto **IWordSink** nel metodo [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Search. h</dt> </dl> |



 

 
