---
description: Un amministratore può forzare un'applicazione client COM a utilizzare sempre la stessa copia di un server COM in un pacchetto esistente&\# 8212; senza influire sulle altre applicazioni&\# 8212; specificando una relazione dei componenti isolati tra il server e il client com.
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: Rendere privato un componente COM in un pacchetto esistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4935d20c5034af81a52c18d35454553b04cfb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316268"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a><span data-ttu-id="9f152-103">Rendere privato un componente COM in un pacchetto esistente</span><span class="sxs-lookup"><span data-stu-id="9f152-103">Make a COM Component in an Existing Package Private</span></span>

<span data-ttu-id="9f152-104">Un amministratore può forzare un'applicazione client COM a utilizzare sempre la stessa copia di un server COM in un pacchetto esistente, senza influire sulle altre applicazioni, specificando una relazione dei [componenti isolati](isolated-components.md) tra il server e il client com.</span><span class="sxs-lookup"><span data-stu-id="9f152-104">An administrator can force a COM-client application to always use the same copy of a COM-server in an existing package—without affecting other applications—by specifying an [isolated components](isolated-components.md) relationship between the COM server and client.</span></span> <span data-ttu-id="9f152-105">Verrà installata una copia privata del componente server COM in un percorso utilizzato esclusivamente dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="9f152-105">This installs a private copy of the COM-server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="9f152-106">L'amministratore deve utilizzare le trasformazioni o uno strumento di creazione di pacchetti per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9f152-106">The administrator needs to use transforms or a package authoring tool to do the following:</span></span>

-   <span data-ttu-id="9f152-107">Inserire la DLL del server COM e il client exe in componenti distinti.</span><span class="sxs-lookup"><span data-stu-id="9f152-107">Put the COM server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="9f152-108">Immettere un record nella [tabella IsolatedComponent](isolatedcomponent-table.md) con il componente COM-client nella \_ colonna Shared Component e l'applicazione client nella \_ colonna applicazione componente.</span><span class="sxs-lookup"><span data-stu-id="9f152-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the COM-client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="9f152-109">Includere l' [azione IsolateComponents](isolatecomponents-action.md) nelle tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="9f152-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="9f152-110">Impostare il bit **msidbComponentAttributesSharedDllRefCount** nel record della [tabella dei componenti](component-table.md) per il componente \_ condiviso.</span><span class="sxs-lookup"><span data-stu-id="9f152-110">Set the **msidbComponentAttributesSharedDllRefCount** bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="9f152-111">Il programma di installazione richiede questo refcount globale sul percorso condiviso per proteggere i file condivisi e la registrazione nei casi in cui vi sia una condivisione con altre tecnologie di installazione.</span><span class="sxs-lookup"><span data-stu-id="9f152-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



