---
description: Un amministratore può forzare un'applicazione client a utilizzare sempre la stessa copia di un server non COM in un pacchetto esistente&\# 8212; senza influire sulle altre applicazioni&\# 8212; specificando una relazione dei componenti isolati tra il server e il client.
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: Creare un componente non COM in un pacchetto esistente privato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87a74a4f9fe7c3770100f78dd0fcd154772943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308183"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a><span data-ttu-id="dafb8-103">Creare un componente non COM in un pacchetto esistente privato</span><span class="sxs-lookup"><span data-stu-id="dafb8-103">Make a non-COM Component in an Existing Package Private</span></span>

<span data-ttu-id="dafb8-104">Un amministratore può forzare un'applicazione client a utilizzare sempre la stessa copia di un server non COM in un pacchetto esistente, senza influire sulle altre applicazioni, specificando una relazione dei [componenti isolati](isolated-components.md) tra il server e il client.</span><span class="sxs-lookup"><span data-stu-id="dafb8-104">An administrator can force a client application to always use the same copy of a non-COM server in an existing package—without affecting other applications—by specifying an [isolated components](isolated-components.md) relationship between the server and client.</span></span> <span data-ttu-id="dafb8-105">Verrà installata una copia privata del componente server in una posizione utilizzata esclusivamente dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="dafb8-105">This installs a private copy of the server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="dafb8-106">L'amministratore deve utilizzare le trasformazioni o uno strumento di creazione di pacchetti per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dafb8-106">The administrator needs to use transforms or a package authoring tool to do the following:</span></span>

-   <span data-ttu-id="dafb8-107">Inserire la DLL del server e il client exe in componenti distinti.</span><span class="sxs-lookup"><span data-stu-id="dafb8-107">Put the server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="dafb8-108">Immettere un record nella [tabella IsolatedComponent](isolatedcomponent-table.md) con il componente client nella \_ colonna Shared Component e l'applicazione client nella \_ colonna applicazione componente.</span><span class="sxs-lookup"><span data-stu-id="dafb8-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="dafb8-109">Includere l' [azione IsolateComponents](isolatecomponents-action.md) nelle tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="dafb8-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="dafb8-110">Impostare il bit **msidbComponentAttributesSharedDllRefCount** nel record della [tabella dei componenti](component-table.md) per il componente \_ condiviso.</span><span class="sxs-lookup"><span data-stu-id="dafb8-110">Set the **msidbComponentAttributesSharedDllRefCount** bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="dafb8-111">Il programma di installazione richiede questo refcount globale sul percorso condiviso per proteggere i file condivisi e la registrazione nei casi in cui vi sia una condivisione con altre tecnologie di installazione.</span><span class="sxs-lookup"><span data-stu-id="dafb8-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



