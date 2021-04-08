---
description: Network Monitor utilizza la funzione di esportazione DllMain per identificare l'esistenza del parser e rilasciare le risorse utilizzate da Network Monitor per archiviare le informazioni sul parser.
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: Implementazione del parser DllMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55dd1ab7432920ac7496643c7c6f9aa0692daf56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750050"
---
# <a name="implementing-dllmain-parser"></a>Implementazione del parser DllMain

Network Monitor utilizza la funzione di esportazione **DllMain** per identificare l'esistenza del parser e rilasciare le risorse utilizzate da Network Monitor per archiviare le informazioni sul parser.

Quando Network Monitor chiama **DllMain** per la prima volta, la dll del parser chiama [**CreateProtocol**](createprotocol.md) per eseguire le operazioni seguenti:

-   Specificare il protocollo rilevato dal parser.
-   Fornire punti di ingresso per le funzioni di esportazione del parser rimanenti che Network Monitor chiamate.

Quando Network Monitor chiama **DllMain** per l'ultima volta, **DllMain** chiama [**DestroyProtocol**](destroyprotocol.md) per rilasciare tutte le risorse utilizzate da Network Monitor per archiviare le informazioni sul parser.

Nella procedura seguente vengono identificati i passaggi necessari per implementare **DllMain**.

**Per implementare DllMain**

1.  Specificare la struttura [**ENTRYPOINTS**](entrypoints.md) per la funzione [**CreateProtocol**](createprotocol.md) e la variabile di connessione globale. La variabile di associazione viene utilizzata per tenere traccia del numero di istanze di protocollo in esecuzione.
2.  Esaminare il valore del parametro del *comando* impostato dal sistema operativo.

    Se il parametro del *comando* è impostato su dll \_ processo \_ Connetti e Connetti è 0, chiamare [**CreateProtocol**](createprotocol.md) per fornire il nome del protocollo e i punti di ingresso per le funzioni di esportazione seguenti.

    -   **Registra**
    -   **Annullamento registrazione**
    -   **RecognizeFrame**
    -   **AttachProperties**
    -   **FormatProperties** (obbligatorio solo se Network Monitor visualizzerà le proprietà del protocollo).

    Se il parametro del *comando* è impostato su dll \_ processo di \_ scollegamento e il collegamento è 0, chiamare [**DestroyProtocol**](destroyprotocol.md) usando l'handle dell'istanza restituito da [**CreateProtocol**](createprotocol.md) .

3.  Restituisce **true** perché la funzione del parser **DllMain** deve restituire sempre **true**.

Di seguito è riportata un'implementazione di base di **DllMain**. Nell'esempio di codice viene utilizzata un'istruzione case per intercettare i valori del parametro *Command* per determinare se è necessario chiamare [**CreateProtocol**](createprotocol.md) o [**DestroyProtocol**](destroyprotocol.md) .

``` syntax
#include <windows.h>

// Entry point structure for parser export functions and global
// Attach variable.
ENTRYPOINTS EntryPoints =
{
  Register,
  Deregister,
  RecognizeFrame,
  AttachProperties,
  FormatProperties
};

DWORD Attached = 0; 

BOOL WINAPI DllMain(HANDLE hInstance, ULONG Command, LPVOID Reserved)
{
  switch(Command)
  {
  // Call CreateProtocol.
  case DLL_PROCESS_ATTACH:
       // Loading parser DLL.
       if(Attached == 0)
       {
         hProtocol = CreateProtocol( "ProtocolName",
                                     &EntryPoints,
                                     ENTRYPOINTS_SIZE);
       }
       Attached++;
       break;
  // Call DestroyProtocol.
  case DLL_PROCESS_DETACH:
       // Unloading parser DLL.
       Attached--;
       if(Attached == 0)
       {
         DestroyProtocol( hProtocol);
       }
       break;
  }
  return TRUE;
}
```

 

 



