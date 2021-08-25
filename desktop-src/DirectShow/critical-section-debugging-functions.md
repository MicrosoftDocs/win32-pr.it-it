---
description: Funzioni di debug delle sezioni critiche
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Funzioni di debug delle sezioni critiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65834d84900ad3ac893cb75493a59902629fec15523cfaca8974a6684ba9c409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908071"
---
# <a name="critical-section-debugging-functions"></a>Funzioni di debug delle sezioni critiche

Queste funzioni consentono di eseguire il debug di sezioni critiche nel codice, semplificando l'individuazione della causa di un deadlock. Queste funzioni usano la classe helper [**CCritSec.**](ccritsec.md)



| Funzione                             | Descrizione                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [**CritCheckIn**](critcheckin.md)   | Restituisce **TRUE** se il thread corrente è proprietario della sezione critica specificata.  |
| [**CritCheckOut**](critcheckout.md) | Restituisce **FALSE** se il thread corrente è proprietario della sezione critica specificata. |
| [**DbgLockTrace**](dbglocktrace.md) | Abilita o disabilita la registrazione di debug per una determinata sezione critica.              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di debug](debugging-utilities.md)
</dt> </dl>

 

 



