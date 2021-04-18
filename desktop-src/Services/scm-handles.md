---
description: SCM supporta i tipi di handle per consentire l'accesso agli oggetti seguenti.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Handle SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8a84fb09dbc95f3e1b5f5cee432de616f5ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318221"
---
# <a name="scm-handles"></a><span data-ttu-id="9a9af-103">Handle SCM</span><span class="sxs-lookup"><span data-stu-id="9a9af-103">SCM Handles</span></span>

<span data-ttu-id="9a9af-104">SCM supporta i tipi di handle per consentire l'accesso agli oggetti seguenti.</span><span class="sxs-lookup"><span data-stu-id="9a9af-104">The SCM supports handle types to allow access to the following objects.</span></span>

-   <span data-ttu-id="9a9af-105">Database dei servizi installati.</span><span class="sxs-lookup"><span data-stu-id="9a9af-105">The database of installed services.</span></span>
-   <span data-ttu-id="9a9af-106">Un servizio.</span><span class="sxs-lookup"><span data-stu-id="9a9af-106">A service.</span></span>
-   <span data-ttu-id="9a9af-107">Blocco del database.</span><span class="sxs-lookup"><span data-stu-id="9a9af-107">The database lock.</span></span>

<span data-ttu-id="9a9af-108">Un oggetto SCManager rappresenta il database dei servizi installati.</span><span class="sxs-lookup"><span data-stu-id="9a9af-108">An SCManager object represents the database of installed services.</span></span> <span data-ttu-id="9a9af-109">Si tratta di un oggetto contenitore che include oggetti servizio.</span><span class="sxs-lookup"><span data-stu-id="9a9af-109">It is a container object that holds service objects.</span></span> <span data-ttu-id="9a9af-110">La funzione [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) restituisce un handle a un oggetto SCManager in un computer specificato.</span><span class="sxs-lookup"><span data-stu-id="9a9af-110">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function returns a handle to an SCManager object on a specified computer.</span></span> <span data-ttu-id="9a9af-111">Questo handle viene utilizzato per l'installazione, l'eliminazione, l'apertura e l'enumerazione dei servizi e per il blocco del database dei servizi.</span><span class="sxs-lookup"><span data-stu-id="9a9af-111">This handle is used when installing, deleting, opening, and enumerating services and when locking the services database.</span></span>

<span data-ttu-id="9a9af-112">Un oggetto servizio rappresenta un servizio installato.</span><span class="sxs-lookup"><span data-stu-id="9a9af-112">A service object represents an installed service.</span></span> <span data-ttu-id="9a9af-113">Le funzioni [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) restituiscono handle ai servizi installati.</span><span class="sxs-lookup"><span data-stu-id="9a9af-113">The [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions return handles to installed services.</span></span>

<span data-ttu-id="9a9af-114">Le funzioni [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)e [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) possono richiedere tipi diversi di accesso agli oggetti SCManager e Service.</span><span class="sxs-lookup"><span data-stu-id="9a9af-114">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea), and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions can request different types of access to SCManager and service objects.</span></span> <span data-ttu-id="9a9af-115">L'accesso richiesto viene concesso o negato a seconda del token di accesso del processo chiamante e del descrittore di sicurezza associato all'oggetto SCManager o al servizio.</span><span class="sxs-lookup"><span data-stu-id="9a9af-115">The requested access is granted or denied depending on the access token of the calling process and the security descriptor associated with the SCManager or service object.</span></span>

<span data-ttu-id="9a9af-116">La funzione [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) chiude gli handle agli oggetti SCManager e Service.</span><span class="sxs-lookup"><span data-stu-id="9a9af-116">The [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) function closes handles to SCManager and service objects.</span></span> <span data-ttu-id="9a9af-117">Quando questi handle non sono più necessari, assicurarsi di chiuderli.</span><span class="sxs-lookup"><span data-stu-id="9a9af-117">When you no longer need these handles, be sure to close them.</span></span>

 

 



