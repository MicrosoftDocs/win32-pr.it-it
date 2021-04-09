---
description: Per forzare l'utilizzo sempre della stessa copia di un server non COM da parte di un'applicazione client, creare il pacchetto di installazione dell'applicazione in modo da specificare una relazione dei componenti isolati tra il server e il client.
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: Installazione di un componente non COM in una posizione privata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ea4e10e7a08fd008352a36feca537685ee4390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885522"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a><span data-ttu-id="3bf24-103">Installazione di un componente non COM in una posizione privata</span><span class="sxs-lookup"><span data-stu-id="3bf24-103">Installing a non-COM Component to a Private Location</span></span>

<span data-ttu-id="3bf24-104">Per forzare l'utilizzo sempre della stessa copia di un server non COM da parte di un'applicazione client, creare il pacchetto di installazione dell'applicazione in modo da specificare una relazione dei [componenti isolati](isolated-components.md) tra il server e il client.</span><span class="sxs-lookup"><span data-stu-id="3bf24-104">To force a client application to always use the same copy of a non-COM server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the server and client.</span></span> <span data-ttu-id="3bf24-105">Verrà installata una copia privata del componente server in una posizione utilizzata esclusivamente dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="3bf24-105">This installs a private copy of the server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="3bf24-106">Quando si crea il pacchetto, effettuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3bf24-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="3bf24-107">Inserire la DLL del server e il client exe in componenti distinti.</span><span class="sxs-lookup"><span data-stu-id="3bf24-107">Put the server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="3bf24-108">Immettere un record nella [tabella IsolatedComponent](isolatedcomponent-table.md) con il componente client nella \_ colonna Shared Component e l'applicazione client nella \_ colonna applicazione componente.</span><span class="sxs-lookup"><span data-stu-id="3bf24-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="3bf24-109">Includere l' [azione IsolateComponents](isolatecomponents-action.md) nelle tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="3bf24-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="3bf24-110">Impostare il bit msidbComponentAttributesSharedDllRefCount nel record della [tabella dei componenti](component-table.md) per il componente \_ condiviso.</span><span class="sxs-lookup"><span data-stu-id="3bf24-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="3bf24-111">Il programma di installazione richiede questo refcount globale sul percorso condiviso per proteggere i file condivisi e la registrazione nei casi in cui vi sia una condivisione con altre tecnologie di installazione.</span><span class="sxs-lookup"><span data-stu-id="3bf24-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>
-   <span data-ttu-id="3bf24-112">Evitare di creare un percorso registrato condiviso tra i componenti.</span><span class="sxs-lookup"><span data-stu-id="3bf24-112">Avoid authoring a shared registered path across components.</span></span>

 

 



