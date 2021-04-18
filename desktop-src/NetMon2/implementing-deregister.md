---
description: Network Monitor passa tutti i frame di un'acquisizione ai parser, quindi inizia a chiamare la funzione di annullamento della registrazione per tutti i protocolli identificati. Ogni DLL del parser deve implementare una funzione di annullamento della registrazione per ogni protocollo supportato dalla DLL del parser.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implementazione della deregistrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee07c5b6b3c746e9c29811332b9e7674e49db26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306560"
---
# <a name="implementing-deregister"></a><span data-ttu-id="b5bf9-104">Implementazione della deregistrazione</span><span class="sxs-lookup"><span data-stu-id="b5bf9-104">Implementing Deregister</span></span>

<span data-ttu-id="b5bf9-105">Network Monitor passa tutti i frame di un'acquisizione ai parser, quindi inizia a chiamare la funzione di [**annullamento della registrazione**](deregister.md) per tutti i protocolli identificati.</span><span class="sxs-lookup"><span data-stu-id="b5bf9-105">Network Monitor passes all the frames of a capture to the parsers, and then starts calling the [**Deregister**](deregister.md) function for all the protocols it identifies.</span></span> <span data-ttu-id="b5bf9-106">Ogni DLL del parser deve implementare una funzione di **annullamento della registrazione** per ogni protocollo supportato dalla dll del parser.</span><span class="sxs-lookup"><span data-stu-id="b5bf9-106">Each parser DLL must implement a **Deregister** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="b5bf9-107">Ogni implementazione della funzione [**deregister**](deregister.md) deve chiamare la funzione [**DestroyProtocolDatabase**](destroypropertydatabase.md) per rilasciare le risorse utilizzate per creare il database.</span><span class="sxs-lookup"><span data-stu-id="b5bf9-107">Each implementation of the [**Deregister**](deregister.md) function must call the [**DestroyProtocolDatabase**](destroypropertydatabase.md) function to release the resources that are used to create the database.</span></span>

<span data-ttu-id="b5bf9-108">Nella procedura seguente viene identificato il passaggio necessario per implementare la [**Deregistrazione**](deregister.md).</span><span class="sxs-lookup"><span data-stu-id="b5bf9-108">The following procedure identifies the one step necessary to implement [**Deregister**](deregister.md).</span></span>

<span data-ttu-id="b5bf9-109">**Per implementare la deregistrazione per un protocollo**</span><span class="sxs-lookup"><span data-stu-id="b5bf9-109">**To implement Deregister for one protocol**</span></span>

-   <span data-ttu-id="b5bf9-110">Chiamare [**DestroyProtocolDatabase**](destroypropertydatabase.md) per rilasciare le risorse di database.</span><span class="sxs-lookup"><span data-stu-id="b5bf9-110">Call [**DestroyProtocolDatabase**](destroypropertydatabase.md) to release the database resources.</span></span>

<span data-ttu-id="b5bf9-111">Di seguito è riportata un'implementazione di base di [**deregister**](deregister.md).</span><span class="sxs-lookup"><span data-stu-id="b5bf9-111">The following is a basic implementation of [**Deregister**](deregister.md).</span></span> <span data-ttu-id="b5bf9-112">Si noti che nell'esempio di codice viene illustrata la versione delle risorse utilizzate per la creazione di un database di proprietà.</span><span class="sxs-lookup"><span data-stu-id="b5bf9-112">Note that the code example shows the release of resources that are used to create a property database.</span></span>

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



