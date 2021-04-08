---
description: Per forzare un'applicazione client COM a utilizzare sempre la stessa copia di un server COM, creare il pacchetto di installazione dell'applicazione per specificare una relazione dei componenti isolati tra il server e il client COM.
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: Installazione di un componente COM in un percorso privato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838b3f40c513fd0998402893543e88526e4a6d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879926"
---
# <a name="installing-a-com-component-to-a-private-location"></a><span data-ttu-id="5dc66-103">Installazione di un componente COM in un percorso privato</span><span class="sxs-lookup"><span data-stu-id="5dc66-103">Installing a COM Component to a Private Location</span></span>

<span data-ttu-id="5dc66-104">Per forzare un'applicazione client COM a utilizzare sempre la stessa copia di un server COM, creare il pacchetto di installazione dell'applicazione per specificare una relazione dei [componenti isolati](isolated-components.md) tra il server e il client com.</span><span class="sxs-lookup"><span data-stu-id="5dc66-104">To force a COM-client application to always use the same copy of a COM-server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the COM server and client.</span></span> <span data-ttu-id="5dc66-105">Verrà installata una copia privata del componente server COM in un percorso utilizzato esclusivamente dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="5dc66-105">This installs a private copy of the COM-server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="5dc66-106">Quando si crea il pacchetto, effettuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5dc66-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="5dc66-107">Inserire la DLL del server COM e il client exe in componenti distinti.</span><span class="sxs-lookup"><span data-stu-id="5dc66-107">Put the COM server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="5dc66-108">Immettere un record nella [tabella IsolatedComponent](isolatedcomponent-table.md) con il componente COM-client nella \_ colonna Shared Component e l'applicazione client nella \_ colonna applicazione componente.</span><span class="sxs-lookup"><span data-stu-id="5dc66-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the COM-client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="5dc66-109">Includere l' [azione IsolateComponents](isolatecomponents-action.md) nelle tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="5dc66-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="5dc66-110">Impostare il bit msidbComponentAttributesSharedDllRefCount nel record della [tabella dei componenti](component-table.md) per il componente \_ condiviso.</span><span class="sxs-lookup"><span data-stu-id="5dc66-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="5dc66-111">Il programma di installazione richiede questo refcount globale sul percorso condiviso per proteggere i file condivisi e la registrazione nei casi in cui vi sia una condivisione con altre tecnologie di installazione.</span><span class="sxs-lookup"><span data-stu-id="5dc66-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



