---
description: Un processo figlio può ereditare handle dal processo padre. Un handle ereditato è valido solo nel contesto del processo figlio. Per consentire a un processo figlio di ereditare gli handle aperti dal processo padre, attenersi alla procedura riportata di seguito.
ms.assetid: 957cd369-bebf-4e04-9f7e-a936e2e97887
title: Gestisci ereditarietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd684308503a8747f6730e9d0daf4aa3de760186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317661"
---
# <a name="handle-inheritance"></a>Gestisci ereditarietà

Un processo figlio può ereditare handle dal processo padre. Un handle ereditato è valido solo nel contesto del processo figlio. Per consentire a un processo figlio di ereditare gli handle aperti dal processo padre, attenersi alla procedura riportata di seguito.

1.  Creare l'handle con il membro **bInheritHandle** della struttura [**degli \_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) impostata su **true**.
2.  Creare il processo figlio utilizzando la funzione [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) , con il parametro *BInheritHandles* impostato su **true**.

La funzione [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) duplica un handle da usare nel processo corrente o in un altro processo. Se un'applicazione Duplica uno dei relativi handle per un altro processo, l'handle duplicato è valido solo nel contesto dell'altro processo.

Un handle duplicato o ereditato è un valore univoco, ma fa riferimento allo stesso oggetto dell'handle originale. I processi possono ereditare o duplicare gli handle per i tipi di oggetti seguenti:

-   Token di accesso
-   Dispositivo di comunicazione
-   Input console
-   Buffer dello schermo della console
-   Desktop
-   Directory
-   Evento
-   File
-   Mapping dei file
-   Processo
-   Inserimento/espulsione
-   Mutex
-   Pipe
-   Processo
-   Chiave del Registro di sistema
-   Semaphore
-   Presa elettrica
-   Thread
-   Timer
-   Stazione finestra

Tutti gli altri oggetti sono privati del processo che li ha creati; i rispettivi handle di oggetto non possono essere duplicati o ereditati.

Per altre informazioni, vedere [Ereditarietà](/windows/desktop/ProcThread/inheritance).

 

 
