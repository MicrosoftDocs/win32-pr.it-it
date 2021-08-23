---
description: Quando si crea un processo con la funzione CreateProcess, è possibile specificare che il processo erediti gli handle per gli oggetti mutex, event, semaphore o timer usando la struttura SECURITY \_ ATTRIBUTES.
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Ereditarietà degli oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab6d2380ac0012e0f1005df2dfc4b820bee82a7974f3ca03d856c7df9fb8446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661381"
---
# <a name="object-inheritance"></a>Ereditarietà degli oggetti

Quando si crea un processo con la [**funzione CreateProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) è possibile specificare che il processo erediti gli handle per gli oggetti mutex, event, semaphore o timer usando la struttura [**SECURITY \_ ATTRIBUTES.**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) L'handle ereditato dal processo ha lo stesso accesso all'oggetto dell'handle originale. L'handle ereditato viene visualizzato nella tabella degli handle del processo creato, ma è necessario comunicare il valore dell'handle al processo creato. A tale scopo, specificare il valore come argomento della riga di comando quando si chiama **CreateProcess**. Il processo creato usa quindi la [**funzione GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) per recuperare la stringa della riga di comando e convertire l'argomento handle in un handle utilizzabile. Per altre informazioni, vedere [Ereditarietà](../procthread/inheritance.md).

 

 
