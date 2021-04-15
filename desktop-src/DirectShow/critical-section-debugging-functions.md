---
description: Funzioni di debug della sezione critica
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Funzioni di debug della sezione critica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520993"
---
# <a name="critical-section-debugging-functions"></a>Funzioni di debug della sezione critica

Queste funzioni consentono di eseguire il debug di sezioni critiche nel codice, semplificando la ricerca della cause di un deadlock. Queste funzioni usano la classe helper [**CCritSec**](ccritsec.md) .



| Funzione                             | Descrizione                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [**CritCheckIn**](critcheckin.md)   | Restituisce **true** se il thread corrente è proprietario della sezione critica specificata.  |
| [**CritCheckOut**](critcheckout.md) | Restituisce **false** se il thread corrente è proprietario della sezione critica specificata. |
| [**DbgLockTrace**](dbglocktrace.md) | Abilita o Disabilita la registrazione di debug per una sezione critica specificata.              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di debug](debugging-utilities.md)
</dt> </dl>

 

 



