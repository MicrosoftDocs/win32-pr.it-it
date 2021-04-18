---
description: Quando si crea un processo con la funzione CreateProcess, è possibile specificare che il processo erediti gli handle per gli oggetti mutex, Event, Semaphore o timer usando la \_ struttura degli attributi di sicurezza.
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Ereditarietà degli oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6087ae3699e7628ab97871ede41cc2e406e40157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314645"
---
# <a name="object-inheritance"></a>Ereditarietà degli oggetti

Quando si crea un processo con la funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) , è possibile specificare che il processo erediti gli handle per gli oggetti mutex, Event, Semaphore o timer usando la struttura degli [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . L'handle ereditato dal processo ha lo stesso accesso all'oggetto come handle originale. L'handle ereditato viene visualizzato nella tabella di handle del processo creato, ma è necessario comunicare il valore dell'handle al processo creato. È possibile eseguire questa operazione specificando il valore come argomento della riga di comando quando si chiama **CreateProcess**. Il processo creato usa quindi la funzione [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) per recuperare la stringa della riga di comando e convertire l'argomento handle in un handle utilizzabile. Per altre informazioni, vedere [Ereditarietà](../procthread/inheritance.md).

 

 
