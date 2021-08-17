---
description: Network Monitor usa la funzione di esportazione DllMain per identificare l'esistenza del parser e rilasciare le risorse utilizzate Network Monitor per archiviare le informazioni sul parser.
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: Implementazione del parser DllMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb79ab862c64d8d99359965fec6c0d1ca8bf3cf9e35fdf58f1cbc063d5c3e6c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132940"
---
# <a name="implementing-dllmain-parser"></a>Implementazione del parser DllMain

Network Monitor usa la funzione di esportazione **DllMain** per identificare l'esistenza del parser e rilasciare le risorse che Network Monitor per archiviare le informazioni sul parser.

Quando Network Monitor chiama **DllMain** per la prima volta, la DLL del parser chiama [**CreateProtocol**](createprotocol.md) per eseguire le operazioni seguenti:

-   Specificare il protocollo rilevato dal parser.
-   Specificare i punti di ingresso per le rimanenti funzioni di esportazione del parser Network Monitor chiamate.

Quando Network Monitor chiama **DllMain** per l'ultima volta, **DllMain** chiama [**DestroyProtocol**](destroyprotocol.md) per rilasciare tutte le risorse che Network Monitor usa per archiviare le informazioni sul parser.

La procedura seguente identifica i passaggi necessari per implementare **DllMain.**

**Per implementare DllMain**

1.  Specificare la [**struttura ENTRYPOINTS**](entrypoints.md) per la [**funzione CreateProtocol**](createprotocol.md) e la variabile attach globale. La variabile Attach viene usata per tenere traccia del numero di istanze del protocollo in esecuzione.
2.  Esaminare il valore del parametro *Command* impostato dal sistema operativo.

    Se il *parametro Command* è impostato su DLL PROCESS ATTACH e Attach è 0, chiamare \_ \_ [**CreateProtocol**](createprotocol.md) per specificare il nome del protocollo e i punti di ingresso per le funzioni di esportazione seguenti.

    -   **Registra**
    -   **Annullamento registrazione**
    -   **RecognizeFrame**
    -   **Proprietàallegato**
    -   **FormatProperties** (obbligatorio solo se Network Monitor verranno visualizzate le proprietà del protocollo).

    Se il *parametro Command* è impostato su DLL PROCESS DETACH e Attach è 0, chiamare DestroyProtocol usando l'handle di istanza restituito \_ da \_ [**CreateProtocol.**](createprotocol.md) [](destroyprotocol.md)

3.  Restituisce **TRUE** perché la funzione del parser **DllMain** deve sempre restituire **TRUE.**

Di seguito è riportata un'implementazione di base **di DllMain.** L'esempio di codice usa un'istruzione case per intercettare i valori del parametro *Command* per determinare se è necessario chiamare [**CreateProtocol**](createprotocol.md) o [**DestroyProtocol.**](destroyprotocol.md)

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

 

 



