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
# <a name="implementing-dllmain-parser"></a><span data-ttu-id="f6ea7-103">Implementazione del parser DllMain</span><span class="sxs-lookup"><span data-stu-id="f6ea7-103">Implementing DllMain Parser</span></span>

<span data-ttu-id="f6ea7-104">Network Monitor utilizza la funzione di esportazione **DllMain** per identificare l'esistenza del parser e rilasciare le risorse utilizzate da Network Monitor per archiviare le informazioni sul parser.</span><span class="sxs-lookup"><span data-stu-id="f6ea7-104">Network Monitor uses the **DllMain** export function to identify the existence of the parser, and release resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="f6ea7-105">Quando Network Monitor chiama **DllMain** per la prima volta, la dll del parser chiama [**CreateProtocol**](createprotocol.md) per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f6ea7-105">When Network Monitor calls **DllMain** for the first time, the parser DLL calls [**CreateProtocol**](createprotocol.md) to do the following:</span></span>

-   <span data-ttu-id="f6ea7-106">Specificare il protocollo rilevato dal parser.</span><span class="sxs-lookup"><span data-stu-id="f6ea7-106">Specify the protocol that the parser detects.</span></span>
-   <span data-ttu-id="f6ea7-107">Fornire punti di ingresso per le funzioni di esportazione del parser rimanenti che Network Monitor chiamate.</span><span class="sxs-lookup"><span data-stu-id="f6ea7-107">Provide entry points for remaining parser export functions that Network Monitor calls.</span></span>

<span data-ttu-id="f6ea7-108">Quando Network Monitor chiama **DllMain** per l'ultima volta, **DllMain** chiama [**DestroyProtocol**](destroyprotocol.md) per rilasciare tutte le risorse utilizzate da Network Monitor per archiviare le informazioni sul parser.</span><span class="sxs-lookup"><span data-stu-id="f6ea7-108">When Network Monitor calls **DllMain** for the last time, **DllMain** calls [**DestroyProtocol**](destroyprotocol.md) to release all resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="f6ea7-109">Nella procedura seguente vengono identificati i passaggi necessari per implementare **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="f6ea7-109">The following procedure identifies the steps necessary to implement **DllMain**.</span></span>

<span data-ttu-id="f6ea7-110">**Per implementare DllMain**</span><span class="sxs-lookup"><span data-stu-id="f6ea7-110">**To implement DllMain**</span></span>

1.  <span data-ttu-id="f6ea7-111">Specificare la struttura [**ENTRYPOINTS**](entrypoints.md) per la funzione [**CreateProtocol**](createprotocol.md) e la variabile di connessione globale.</span><span class="sxs-lookup"><span data-stu-id="f6ea7-111">Specify the [**ENTRYPOINTS**](entrypoints.md) structure for the [**CreateProtocol**](createprotocol.md) function and global Attach variable.</span></span> <span data-ttu-id="f6ea7-112">La variabile di associazione viene utilizzata per tenere traccia del numero di istanze di protocollo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f6ea7-112">The Attach variable is used to track the number of protocol instances that are running.</span></span>
2.  <span data-ttu-id="f6ea7-113">Esaminare il valore del parametro del *comando* impostato dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f6ea7-113">Look at the value of the *Command* parameter that the operating system sets.</span></span>

    <span data-ttu-id="f6ea7-114">Se il parametro del *comando* è impostato su dll \_ processo \_ Connetti e Connetti è 0, chiamare [**CreateProtocol**](createprotocol.md) per fornire il nome del protocollo e i punti di ingresso per le funzioni di esportazione seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6ea7-114">If the *Command* parameter is set to DLL\_PROCESS\_ATTACH and Attach is 0, then call [**CreateProtocol**](createprotocol.md) to provide the protocol name and entry points for the following export functions.</span></span>

    -   <span data-ttu-id="f6ea7-115">**Registra**</span><span class="sxs-lookup"><span data-stu-id="f6ea7-115">**Register**</span></span>
    -   <span data-ttu-id="f6ea7-116">**Annullamento registrazione**</span><span class="sxs-lookup"><span data-stu-id="f6ea7-116">**Deregister**</span></span>
    -   <span data-ttu-id="f6ea7-117">**RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="f6ea7-117">**RecognizeFrame**</span></span>
    -   <span data-ttu-id="f6ea7-118">**AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="f6ea7-118">**AttachProperties**</span></span>
    -   <span data-ttu-id="f6ea7-119">**FormatProperties** (obbligatorio solo se Network Monitor visualizzerà le proprietà del protocollo).</span><span class="sxs-lookup"><span data-stu-id="f6ea7-119">**FormatProperties** (only required if Network Monitor will be displaying the protocol properties).</span></span>

    <span data-ttu-id="f6ea7-120">Se il parametro del *comando* è impostato su dll \_ processo di \_ scollegamento e il collegamento è 0, chiamare [**DestroyProtocol**](destroyprotocol.md) usando l'handle dell'istanza restituito da [**CreateProtocol**](createprotocol.md) .</span><span class="sxs-lookup"><span data-stu-id="f6ea7-120">If the *Command* parameter is set to DLL\_PROCESS\_DETACH and Attach is 0, then call [**DestroyProtocol**](destroyprotocol.md) using the instance handle that [**CreateProtocol**](createprotocol.md) returns.</span></span>

3.  <span data-ttu-id="f6ea7-121">Restituisce **true** perché la funzione del parser **DllMain** deve restituire sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="f6ea7-121">Return **TRUE** because the **DllMain** parser function must always return **TRUE**.</span></span>

<span data-ttu-id="f6ea7-122">Di seguito è riportata un'implementazione di base di **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="f6ea7-122">The following is a basic implementation of **DllMain**.</span></span> <span data-ttu-id="f6ea7-123">Nell'esempio di codice viene utilizzata un'istruzione case per intercettare i valori del parametro *Command* per determinare se è necessario chiamare [**CreateProtocol**](createprotocol.md) o [**DestroyProtocol**](destroyprotocol.md) .</span><span class="sxs-lookup"><span data-stu-id="f6ea7-123">The code example uses a case statement to trap values of the *Command* parameter to determine if [**CreateProtocol**](createprotocol.md) or [**DestroyProtocol**](destroyprotocol.md) should be called.</span></span>

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

 

 



