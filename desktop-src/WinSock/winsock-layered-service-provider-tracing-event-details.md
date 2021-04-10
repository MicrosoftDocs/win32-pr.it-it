---
description: Dettagli della traccia delle modifiche del catalogo Winsock
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Dettagli della traccia delle modifiche del catalogo Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6258ca87d5d1fba2de9364e5524110bb43c76513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130403"
---
# <a name="winsock-catalog-change-tracing-details"></a><span data-ttu-id="4b643-103">Dettagli della traccia delle modifiche del catalogo Winsock</span><span class="sxs-lookup"><span data-stu-id="4b643-103">Winsock Catalog Change Tracing Details</span></span>

> [!Note]  
> <span data-ttu-id="4b643-104">I provider di servizi sovrapposti sono deprecati.</span><span class="sxs-lookup"><span data-stu-id="4b643-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="4b643-105">A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="4b643-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="4b643-106">La traccia eventi di modifica del catalogo Winsock per i provider di servizi su più livelli (LSP) è correlata all'installazione di LSP, alla rimozione di LSP, alla disabilitazione di LSP e alla reimpostazione del catalogo Winsock</span><span class="sxs-lookup"><span data-stu-id="4b643-106">Winsock Catalog Change event tracing for layered Service providers (LSPs) is related to LSP installation, LSP removal, LSP disable, and Winsock catalog reset operations.</span></span> <span data-ttu-id="4b643-107">Tutti gli eventi seguenti vengono scritti nel canale *Microsoft-Windows-Winsock-ws2help/Operational* , che è diverso dall'altra traccia degli eventi di rete Winsock registrata in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4b643-107">All of the following events are written to the *Microsoft-Windows-Winsock-WS2HELP/Operational* channel which is different from the other Winsock network event tracing logged on Windows Vista and later.</span></span>

<span data-ttu-id="4b643-108">Di seguito vengono descritti in dettaglio tutti gli eventi del LSP Winsock che possono essere tracciati e vengono descritti i parametri e le informazioni registrate.</span><span class="sxs-lookup"><span data-stu-id="4b643-108">The following details each of the Winsock LSP events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="lsp-install"></a><span data-ttu-id="4b643-109">Installazione LSP</span><span class="sxs-lookup"><span data-stu-id="4b643-109">LSP Install</span></span>

<span data-ttu-id="4b643-110">ID evento = 1</span><span class="sxs-lookup"><span data-stu-id="4b643-110">Event ID = 1</span></span>

<span data-ttu-id="4b643-111">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="4b643-111">Level = 4 (Information)</span></span>

<span data-ttu-id="4b643-112">Per un'operazione di installazione di LSP vengono tracciati gli eventi LSP seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b643-112">The following Winsock LSP events are traced for an LSP install operation:</span></span>

-   <span data-ttu-id="4b643-113">Una voce di protocollo viene installata nel catalogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="4b643-113">A protocol entry is installed into the Winsock catalog.</span></span>

<span data-ttu-id="4b643-114">Per un evento di installazione LSP vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b643-114">The following parameters are logged for a LSP install event:</span></span>



| <span data-ttu-id="4b643-115">Parametro</span><span class="sxs-lookup"><span data-stu-id="4b643-115">Parameter</span></span>                                                                                                | <span data-ttu-id="4b643-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b643-116">Description</span></span>                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b643-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome LSP</span><span class="sxs-lookup"><span data-stu-id="4b643-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="4b643-118">Nome dello LSP ottenuto dal membro **szProtocol** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da installare.</span><span class="sxs-lookup"><span data-stu-id="4b643-118">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/> |
| <span data-ttu-id="4b643-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo</span><span class="sxs-lookup"><span data-stu-id="4b643-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="4b643-120">Il catalogo Winsock (32 bit o 64 bit) in cui viene installato lo LSP.</span><span class="sxs-lookup"><span data-stu-id="4b643-120">The Winsock catalog (32-bit or 64-bit) where the LSP is being installed.</span></span> <span data-ttu-id="4b643-121">Si tratta di un valore intero che può essere 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="4b643-121">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="4b643-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installazione</span><span class="sxs-lookup"><span data-stu-id="4b643-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="4b643-123">Il nome file del modulo dell'applicazione che effettua la chiamata di installazione di LSP.</span><span class="sxs-lookup"><span data-stu-id="4b643-123">The module filename of the application making the LSP install call.</span></span><br/>                                                                                          |
| <span data-ttu-id="4b643-124"><span id="GUID"></span><span id="guid"></span>GUID</span><span class="sxs-lookup"><span data-stu-id="4b643-124"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="4b643-125">Valore GUID del provider di trasporto Winsock in cui viene installato il LSP.</span><span class="sxs-lookup"><span data-stu-id="4b643-125">The GUID value of the Winsock transport provider that the LSP is being installed under.</span></span><br/>                                                                      |
| <span data-ttu-id="4b643-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria</span><span class="sxs-lookup"><span data-stu-id="4b643-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="4b643-127">Membro **dwCatalogEntryId** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da installare.</span><span class="sxs-lookup"><span data-stu-id="4b643-127">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/>                                |



 

## <a name="lsp-uninstall"></a><span data-ttu-id="4b643-128">Disinstallazione di LSP</span><span class="sxs-lookup"><span data-stu-id="4b643-128">LSP Uninstall</span></span>

<span data-ttu-id="4b643-129">ID evento = 2</span><span class="sxs-lookup"><span data-stu-id="4b643-129">Event ID = 2</span></span>

<span data-ttu-id="4b643-130">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="4b643-130">Level = 4 (Information)</span></span>

<span data-ttu-id="4b643-131">Per un'operazione di disinstallazione di LSP vengono tracciati gli eventi LSP seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b643-131">The following Winsock LSP events are traced for an LSP uninstall operation:</span></span>

-   <span data-ttu-id="4b643-132">Una voce di protocollo viene rimossa dal catalogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="4b643-132">A protocol entry is removed from the Winsock catalog.</span></span>

<span data-ttu-id="4b643-133">Per un evento di disinstallazione LSP vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b643-133">The following parameters are logged for a LSP uninstall event:</span></span>



| <span data-ttu-id="4b643-134">Parametro</span><span class="sxs-lookup"><span data-stu-id="4b643-134">Parameter</span></span>                                                                                                | <span data-ttu-id="4b643-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b643-135">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b643-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome LSP</span><span class="sxs-lookup"><span data-stu-id="4b643-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="4b643-137">Nome dell'oggetto LSP ottenuto dal membro **szProtocol** della struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4b643-137">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/> |
| <span data-ttu-id="4b643-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo</span><span class="sxs-lookup"><span data-stu-id="4b643-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="4b643-139">Il catalogo Winsock (32 bit o 64 bit) in cui viene rimosso lo LSP.</span><span class="sxs-lookup"><span data-stu-id="4b643-139">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="4b643-140">Si tratta di un valore intero che può essere 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="4b643-140">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="4b643-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installazione</span><span class="sxs-lookup"><span data-stu-id="4b643-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="4b643-142">Il nome file del modulo dell'applicazione che effettua la chiamata di rimozione LSP.</span><span class="sxs-lookup"><span data-stu-id="4b643-142">The module filename of the application making the LSP remove call.</span></span><br/>                                                                                         |
| <span data-ttu-id="4b643-143"><span id="GUID"></span><span id="guid"></span>GUID</span><span class="sxs-lookup"><span data-stu-id="4b643-143"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="4b643-144">Valore GUID del provider di trasporto Winsock da cui viene rimosso il LSP.</span><span class="sxs-lookup"><span data-stu-id="4b643-144">The GUID value of the Winsock transport provider that the LSP is removed from.</span></span><br/>                                                                             |
| <span data-ttu-id="4b643-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria</span><span class="sxs-lookup"><span data-stu-id="4b643-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="4b643-146">Membro **dwCatalogEntryId** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4b643-146">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/>                                |



 

## <a name="lsp-disable"></a><span data-ttu-id="4b643-147">Disabilitazione LSP</span><span class="sxs-lookup"><span data-stu-id="4b643-147">LSP Disable</span></span>

<span data-ttu-id="4b643-148">ID evento = 3</span><span class="sxs-lookup"><span data-stu-id="4b643-148">Event ID = 3</span></span>

<span data-ttu-id="4b643-149">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="4b643-149">Level = 4 (Information)</span></span>

<span data-ttu-id="4b643-150">Per un'operazione di disabilitazione di LSP sono tracciati gli eventi LSP seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b643-150">The following Winsock LSP events are traced for an LSP disable operation:</span></span>

-   <span data-ttu-id="4b643-151">Una voce di protocollo è disabilitata nel catalogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="4b643-151">A protocol entry is disabled in the Winsock catalog.</span></span>

<span data-ttu-id="4b643-152">I parametri seguenti vengono registrati per un evento di disabilitazione LSP:</span><span class="sxs-lookup"><span data-stu-id="4b643-152">The following parameters are logged for a LSP disable event:</span></span>



| <span data-ttu-id="4b643-153">Parametro</span><span class="sxs-lookup"><span data-stu-id="4b643-153">Parameter</span></span>                                                                                                | <span data-ttu-id="4b643-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b643-154">Description</span></span>                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b643-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome LSP</span><span class="sxs-lookup"><span data-stu-id="4b643-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="4b643-156">Nome dello LSP ottenuto dal membro **szProtocol** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP disabilitato.</span><span class="sxs-lookup"><span data-stu-id="4b643-156">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/> |
| <span data-ttu-id="4b643-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo</span><span class="sxs-lookup"><span data-stu-id="4b643-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="4b643-158">Il catalogo Winsock (32 bit o 64 bit) in cui lo LSP viene disabilitato.</span><span class="sxs-lookup"><span data-stu-id="4b643-158">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="4b643-159">Si tratta di un valore intero che può essere 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="4b643-159">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="4b643-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installazione</span><span class="sxs-lookup"><span data-stu-id="4b643-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="4b643-161">Il nome file del modulo dell'applicazione che effettua la chiamata di disabilitazione di LSP.</span><span class="sxs-lookup"><span data-stu-id="4b643-161">The module filename of the application making the LSP disable call.</span></span><br/>                                                                                         |
| <span data-ttu-id="4b643-162"><span id="GUID"></span><span id="guid"></span>GUID</span><span class="sxs-lookup"><span data-stu-id="4b643-162"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="4b643-163">Valore GUID del provider di trasporto Winsock in cui lo LSP viene disabilitato.</span><span class="sxs-lookup"><span data-stu-id="4b643-163">The GUID value of the Winsock transport provider where the LSP is being disabled.</span></span><br/>                                                                           |
| <span data-ttu-id="4b643-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria</span><span class="sxs-lookup"><span data-stu-id="4b643-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="4b643-165">Membro **dwCatalogEntryId** della struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP disabilitato.</span><span class="sxs-lookup"><span data-stu-id="4b643-165">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/>                                |



 

## <a name="winsock-catalog-reset"></a><span data-ttu-id="4b643-166">Reimpostazione del catalogo Winsock</span><span class="sxs-lookup"><span data-stu-id="4b643-166">Winsock Catalog Reset</span></span>

<span data-ttu-id="4b643-167">ID evento = 4</span><span class="sxs-lookup"><span data-stu-id="4b643-167">Event ID = 4</span></span>

<span data-ttu-id="4b643-168">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="4b643-168">Level = 4 (Information)</span></span>

<span data-ttu-id="4b643-169">Per un'operazione di reimpostazione del catalogo Winsock vengono tracciati gli eventi LSP seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b643-169">The following Winsock LSP events are traced for a Winsock catalog reset operation:</span></span>

-   <span data-ttu-id="4b643-170">Il catalogo Winsock è stato reimpostato.</span><span class="sxs-lookup"><span data-stu-id="4b643-170">The Winsock catalog is reset.</span></span>

<span data-ttu-id="4b643-171">Per un evento di reimpostazione del catalogo Winsock vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b643-171">The following parameters are logged for a Winsock catalog reset event:</span></span>



| <span data-ttu-id="4b643-172">Parametro</span><span class="sxs-lookup"><span data-stu-id="4b643-172">Parameter</span></span>                                                                                        | <span data-ttu-id="4b643-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b643-173">Description</span></span>                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b643-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo</span><span class="sxs-lookup"><span data-stu-id="4b643-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/> | <span data-ttu-id="4b643-175">Il catalogo Winsock (32 bit o 64 bit) che viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="4b643-175">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="4b643-176">Si tratta di un valore intero che può essere 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="4b643-176">This is an integer value that is either 32 or 64.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="4b643-177">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b643-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b643-178">Controllo della traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="4b643-178">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="4b643-179">Traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="4b643-179">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="4b643-180">Livelli di traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="4b643-180">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="4b643-181">Dettagli traccia eventi di rete Winsock</span><span class="sxs-lookup"><span data-stu-id="4b643-181">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 
