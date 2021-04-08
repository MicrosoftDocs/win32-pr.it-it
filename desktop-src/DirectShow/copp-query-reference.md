---
description: Riferimento alla query COPP
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: Riferimento alla query COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41de36f3cdcc37a38e2ebc53caa7b6b37c204d9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049061"
---
# <a name="copp-query-reference"></a><span data-ttu-id="065ce-103">Riferimento alla query COPP</span><span class="sxs-lookup"><span data-stu-id="065ce-103">COPP Query Reference</span></span>

<span data-ttu-id="065ce-104">In questa sezione vengono descritte le query di stato supportate da Certified Output Protocol (COPP).</span><span class="sxs-lookup"><span data-stu-id="065ce-104">This section describes the status queries that are supported by Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="065ce-105">Per ogni query, viene elencato il GUID che definisce la query insieme ai dati di input e ai dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="065ce-105">For each query, the GUID that defines the query is listed, along with the input data and return data.</span></span>



| <span data-ttu-id="065ce-106">Query</span><span class="sxs-lookup"><span data-stu-id="065ce-106">Query</span></span>                   | <span data-ttu-id="065ce-107">GUID</span><span class="sxs-lookup"><span data-stu-id="065ce-107">GUID</span></span>                                     |
|-------------------------|------------------------------------------|
| <span data-ttu-id="065ce-108">Dati bus</span><span class="sxs-lookup"><span data-stu-id="065ce-108">Bus Data</span></span>                | <span data-ttu-id="065ce-109">**\_COPPQUERYBUSDATA DXVA**</span><span class="sxs-lookup"><span data-stu-id="065ce-109">**DXVA\_COPPQueryBusData**</span></span>               |
| <span data-ttu-id="065ce-110">Tipo connettore</span><span class="sxs-lookup"><span data-stu-id="065ce-110">Connector Type</span></span>          | <span data-ttu-id="065ce-111">**\_COPPQUERYCONNECTORTYPE DXVA**</span><span class="sxs-lookup"><span data-stu-id="065ce-111">**DXVA\_COPPQueryConnectorType**</span></span>         |
| <span data-ttu-id="065ce-112">Visualizza dati</span><span class="sxs-lookup"><span data-stu-id="065ce-112">Display Data</span></span>            | <span data-ttu-id="065ce-113">**\_COPPQUERYDISPLAYDATA DXVA**</span><span class="sxs-lookup"><span data-stu-id="065ce-113">**DXVA\_COPPQueryDisplayData**</span></span>           |
| <span data-ttu-id="065ce-114">Dati chiave HDCP</span><span class="sxs-lookup"><span data-stu-id="065ce-114">HDCP Key Data</span></span>           | <span data-ttu-id="065ce-115">**\_COPPQUERYHDCPKEYDATA DXVA**</span><span class="sxs-lookup"><span data-stu-id="065ce-115">**DXVA\_COPPQueryHDCPKeyData**</span></span>           |
| <span data-ttu-id="065ce-116">Livello di protezione globale</span><span class="sxs-lookup"><span data-stu-id="065ce-116">Global Protection Level</span></span> | <span data-ttu-id="065ce-117">**\_COPPQUERYGLOBALPROTECTIONLEVEL DXVA**</span><span class="sxs-lookup"><span data-stu-id="065ce-117">**DXVA\_COPPQueryGlobalProtectionLevel**</span></span> |
| <span data-ttu-id="065ce-118">Livello di protezione locale</span><span class="sxs-lookup"><span data-stu-id="065ce-118">Local Protection Level</span></span>  | <span data-ttu-id="065ce-119">**\_COPPQUERYLOCALPROTECTIONLEVEL DXVA**</span><span class="sxs-lookup"><span data-stu-id="065ce-119">**DXVA\_COPPQueryLocalProtectionLevel**</span></span>  |
| <span data-ttu-id="065ce-120">Tipo di protezione</span><span class="sxs-lookup"><span data-stu-id="065ce-120">Protection Type</span></span>         | <span data-ttu-id="065ce-121">**\_COPPQUERYPROTECTIONTYPE DXVA**</span><span class="sxs-lookup"><span data-stu-id="065ce-121">**DXVA\_COPPQueryProtectionType**</span></span>        |
| <span data-ttu-id="065ce-122">Signaling</span><span class="sxs-lookup"><span data-stu-id="065ce-122">Signaling</span></span>               | <span data-ttu-id="065ce-123">**\_COPPQUERYSIGNALING DXVA**</span><span class="sxs-lookup"><span data-stu-id="065ce-123">**DXVA\_COPPQuerySignaling**</span></span>             |



 

<span data-ttu-id="065ce-124">Query sui dati del bus</span><span class="sxs-lookup"><span data-stu-id="065ce-124">Bus Data Query</span></span>

<span data-ttu-id="065ce-125">Restituisce il tipo di bus di I/O utilizzato dalla scheda grafica.</span><span class="sxs-lookup"><span data-stu-id="065ce-125">Returns the type of I/O bus used by the graphics adapter.</span></span>

-   <span data-ttu-id="065ce-126">**GUID**: DXVA \_ COPPQueryBusData</span><span class="sxs-lookup"><span data-stu-id="065ce-126">**GUID**: DXVA\_COPPQueryBusData</span></span>
-   <span data-ttu-id="065ce-127">**Dati di input**: nessuno.</span><span class="sxs-lookup"><span data-stu-id="065ce-127">**Input data**: None.</span></span>
-   <span data-ttu-id="065ce-128">**Dati restituiti**: restituisce una [**struttura \_ COPPStatusData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="065ce-128">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="065ce-129">Il tipo di bus viene restituito nel membro **dwData** come flag dell'enumerazione [**\_ BusType di Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) .</span><span class="sxs-lookup"><span data-stu-id="065ce-129">The bus type is returned in the **dwData** member as a flag from the [**COPP\_BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) enumeration.</span></span>

<span data-ttu-id="065ce-130">Query tipo connettore</span><span class="sxs-lookup"><span data-stu-id="065ce-130">Connector Type Query</span></span>

<span data-ttu-id="065ce-131">Restituisce il tipo di connettore fisico.</span><span class="sxs-lookup"><span data-stu-id="065ce-131">Returns the physical connector type.</span></span>

-   <span data-ttu-id="065ce-132">**GUID**: DXVA \_ COPPQueryConnectorType</span><span class="sxs-lookup"><span data-stu-id="065ce-132">**GUID**: DXVA\_COPPQueryConnectorType</span></span>
-   <span data-ttu-id="065ce-133">**Dati di input**: nessuno.</span><span class="sxs-lookup"><span data-stu-id="065ce-133">**Input data**: None.</span></span>
-   <span data-ttu-id="065ce-134">**Dati restituiti**: restituisce una [**struttura \_ COPPStatusData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="065ce-134">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="065ce-135">Il tipo di connettore viene restituito nel membro **dwData** come flag dell'enumerazione [**\_ ConnectorType di Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) .</span><span class="sxs-lookup"><span data-stu-id="065ce-135">The connector type is returned in the **dwData** member as a flag from the [**COPP\_ConnectorType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) enumeration.</span></span>

<span data-ttu-id="065ce-136">Query dei dati di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="065ce-136">Display Data Query</span></span>

<span data-ttu-id="065ce-137">Restituisce una descrizione del segnale video trasmesso sul connettore.</span><span class="sxs-lookup"><span data-stu-id="065ce-137">Returns a description of the video signal that is being transmitted over the connector.</span></span>

<span data-ttu-id="065ce-138">Il segnale video trasmesso sul connettore non ha necessariamente lo stesso formato della modalità di visualizzazione del desktop.</span><span class="sxs-lookup"><span data-stu-id="065ce-138">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="065ce-139">Ad esempio, la modalità di visualizzazione del desktop può essere 1024x768 pixel a 85 Hz, mentre il connettore potrebbe essere un connettore S-video che trasmette un segnale video a 720x480 pixel, 60/1.01 Hz interlacciato.</span><span class="sxs-lookup"><span data-stu-id="065ce-139">For example, the desktop display mode might be 1024x768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720x480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="065ce-140">In tal caso, il driver restituirà la risoluzione del segnale S-video, non la risoluzione del desktop.</span><span class="sxs-lookup"><span data-stu-id="065ce-140">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

-   <span data-ttu-id="065ce-141">**GUID**: DXVA \_ COPPQueryDisplayData</span><span class="sxs-lookup"><span data-stu-id="065ce-141">**GUID**: DXVA\_COPPQueryDisplayData</span></span>
-   <span data-ttu-id="065ce-142">**Dati di input**: nessuno.</span><span class="sxs-lookup"><span data-stu-id="065ce-142">**Input data**: None.</span></span>
-   <span data-ttu-id="065ce-143">**Dati restituiti**: restituisce una [**struttura \_ COPPStatusDisplayData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) .</span><span class="sxs-lookup"><span data-stu-id="065ce-143">**Return data**: Returns a [**DXVA\_COPPStatusDisplayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) structure.</span></span>

<span data-ttu-id="065ce-144">Query sui dati della chiave HDCP</span><span class="sxs-lookup"><span data-stu-id="065ce-144">HDCP Key Data Query</span></span>

<span data-ttu-id="065ce-145">Restituisce il vettore di selezione della chiave HDCP del dispositivo (B-KSV).</span><span class="sxs-lookup"><span data-stu-id="065ce-145">Returns the device's HDCP key selection vector (B-KSV).</span></span>

<span data-ttu-id="065ce-146">KSV è un identificatore fornito al produttore del dispositivo e viene usato nel processo di autenticazione e configurazione di HDCP.</span><span class="sxs-lookup"><span data-stu-id="065ce-146">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="065ce-147">L'applicazione deve controllare questo valore rispetto all'elenco di KSVs revocati.</span><span class="sxs-lookup"><span data-stu-id="065ce-147">The application should check this value against the list of revoked KSVs.</span></span> <span data-ttu-id="065ce-148">Il meccanismo per ottenere l'elenco di revoche KSV non rientra nell'ambito del protocollo COPP.</span><span class="sxs-lookup"><span data-stu-id="065ce-148">The mechanism for obtaining the KSV revocation list is outside the scope of the COPP protocol.</span></span> <span data-ttu-id="065ce-149">Per ulteriori informazioni, consultare la specifica HDCP.</span><span class="sxs-lookup"><span data-stu-id="065ce-149">For more information, consult the HDCP specification.</span></span>

<span data-ttu-id="065ce-150">Questa query determina anche se il dispositivo HDCP connesso è un monitor o un ripetitore HDCP.</span><span class="sxs-lookup"><span data-stu-id="065ce-150">This query also determines whether the connected HDCP device is a monitor or an HDCP repeater.</span></span> <span data-ttu-id="065ce-151">L'applicazione non deve riprodurre contenuti protetti se il dispositivo HDCP è un ripetitore HDCP, perché questi non sono supportati da COPP.</span><span class="sxs-lookup"><span data-stu-id="065ce-151">The application should not play protected content if the HDCP device is an HDCP repeater, because these are not supported by COPP.</span></span>

-   <span data-ttu-id="065ce-152">**GUID**: DXVA \_ COPPQueryHDCPKeyData</span><span class="sxs-lookup"><span data-stu-id="065ce-152">**GUID**: DXVA\_COPPQueryHDCPKeyData</span></span>
-   <span data-ttu-id="065ce-153">**Dati di input**: nessuno.</span><span class="sxs-lookup"><span data-stu-id="065ce-153">**Input data**: None.</span></span>
-   <span data-ttu-id="065ce-154">**Dati restituiti**: restituisce una [**struttura \_ COPPStatusHDCPKeyData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) .</span><span class="sxs-lookup"><span data-stu-id="065ce-154">**Return data**: Returns a [**DXVA\_COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) structure.</span></span>

<span data-ttu-id="065ce-155">Query livello di protezione globale</span><span class="sxs-lookup"><span data-stu-id="065ce-155">Global Protection Level Query</span></span>

<span data-ttu-id="065ce-156">Restituisce il livello di protezione globale per un meccanismo di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="065ce-156">Returns the global protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="065ce-157">Il livello di protezione globale è il livello di protezione attualmente applicato al connettore, indipendentemente dal modo in cui il driver di grafica ha richiesto di applicare la protezione.</span><span class="sxs-lookup"><span data-stu-id="065ce-157">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="065ce-158">Ad esempio, un'applicazione può impostare il livello di protezione ACP chiamando la funzione **ChangeDisplaySettingsEx** .</span><span class="sxs-lookup"><span data-stu-id="065ce-158">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="065ce-159">In tal caso, il livello di protezione globale rifletterebbe questa impostazione, anche se non è stata richiesta tramite COPP.</span><span class="sxs-lookup"><span data-stu-id="065ce-159">In that case, the global protection level would reflect this setting, even though it was not requested through COPP.</span></span>

-   <span data-ttu-id="065ce-160">**GUID**: DXVA \_ COPPQueryGlobalProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="065ce-160">**GUID**: DXVA\_COPPQueryGlobalProtectionLevel</span></span>
-   <span data-ttu-id="065ce-161">**Dati di input**: meccanismo di protezione per la query, specificato come intero a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="065ce-161">**Input data**: The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="065ce-162">Vedere [flag del tipo di protezione Copp](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="065ce-162">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="065ce-163">**Dati restituiti**: restituisce una [**struttura \_ COPPStatusData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="065ce-163">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="065ce-164">Il livello di protezione corrente viene restituito nel membro **dwData** .</span><span class="sxs-lookup"><span data-stu-id="065ce-164">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="065ce-165">Il significato di questo valore dipende dal meccanismo di protezione su cui viene eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="065ce-165">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="065ce-166">Per ogni meccanismo di protezione, il valore del membro **dwData** è un flag di un'enumerazione diversa, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="065ce-166">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="065ce-167">Meccanismo di protezione</span><span class="sxs-lookup"><span data-stu-id="065ce-167">Protection mechanism</span></span> | <span data-ttu-id="065ce-168">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="065ce-168">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="065ce-169">ACP</span><span class="sxs-lookup"><span data-stu-id="065ce-169">ACP</span></span>                  | [<span data-ttu-id="065ce-170">**\_Livello di \_ protezione \_ ACP Copp**</span><span class="sxs-lookup"><span data-stu-id="065ce-170">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="065ce-171">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="065ce-171">CGMS-A</span></span>               | [<span data-ttu-id="065ce-172">**\_Livello di \_ protezione \_ CGMSA di Copp**</span><span class="sxs-lookup"><span data-stu-id="065ce-172">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="065ce-173">PROTOCOLLO HDCP</span><span class="sxs-lookup"><span data-stu-id="065ce-173">HDCP</span></span>                 | [<span data-ttu-id="065ce-174">**\_Livello di \_ protezione Copp HDCP \_**</span><span class="sxs-lookup"><span data-stu-id="065ce-174">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="065ce-175">Query livello di protezione locale</span><span class="sxs-lookup"><span data-stu-id="065ce-175">Local Protection Level Query</span></span>

<span data-ttu-id="065ce-176">Restituisce il livello di protezione locale per un meccanismo di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="065ce-176">Returns the local protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="065ce-177">Il livello di protezione locale è il livello di protezione richiesto tramite la sessione COPP corrente.</span><span class="sxs-lookup"><span data-stu-id="065ce-177">The local protection level is the protection level that was requested through the current COPP session.</span></span> <span data-ttu-id="065ce-178">Il driver potrebbe impostare un livello di protezione superiore.</span><span class="sxs-lookup"><span data-stu-id="065ce-178">The driver might set a higher protection level.</span></span>

-   <span data-ttu-id="065ce-179">**GUID**: DXVA \_ COPPQueryLocalProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="065ce-179">**GUID**: DXVA\_COPPQueryLocalProtectionLevel</span></span>
-   <span data-ttu-id="065ce-180">**Dati di input**: meccanismo di protezione per la query, come intero a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="065ce-180">**Input data**: The protection mechanism to query, as a 32-bit integer.</span></span> <span data-ttu-id="065ce-181">Vedere [flag del tipo di protezione Copp](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="065ce-181">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="065ce-182">**Dati restituiti**: restituisce una [**struttura \_ COPPStatusData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="065ce-182">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="065ce-183">Il livello di protezione corrente viene restituito nel membro **dwData** .</span><span class="sxs-lookup"><span data-stu-id="065ce-183">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="065ce-184">Il significato di questo valore dipende dal meccanismo di protezione su cui viene eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="065ce-184">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="065ce-185">Per ogni meccanismo di protezione, il valore del membro **dwData** è un flag di un'enumerazione diversa, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="065ce-185">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="065ce-186">Meccanismo di protezione</span><span class="sxs-lookup"><span data-stu-id="065ce-186">Protection mechanism</span></span> | <span data-ttu-id="065ce-187">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="065ce-187">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="065ce-188">ACP</span><span class="sxs-lookup"><span data-stu-id="065ce-188">ACP</span></span>                  | [<span data-ttu-id="065ce-189">**\_Livello di \_ protezione \_ ACP Copp**</span><span class="sxs-lookup"><span data-stu-id="065ce-189">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="065ce-190">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="065ce-190">CGMS-A</span></span>               | [<span data-ttu-id="065ce-191">**\_Livello di \_ protezione \_ CGMSA di Copp**</span><span class="sxs-lookup"><span data-stu-id="065ce-191">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="065ce-192">PROTOCOLLO HDCP</span><span class="sxs-lookup"><span data-stu-id="065ce-192">HDCP</span></span>                 | [<span data-ttu-id="065ce-193">**\_Livello di \_ protezione Copp HDCP \_**</span><span class="sxs-lookup"><span data-stu-id="065ce-193">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="065ce-194">Query del tipo di protezione</span><span class="sxs-lookup"><span data-stu-id="065ce-194">Protection Type Query</span></span>

<span data-ttu-id="065ce-195">Restituisce i meccanismi di protezione disponibili per il connettore.</span><span class="sxs-lookup"><span data-stu-id="065ce-195">Returns the protection mechanisms that are available for the connector.</span></span>

-   <span data-ttu-id="065ce-196">**GUID**: DXVA \_ COPPQueryProtectionType</span><span class="sxs-lookup"><span data-stu-id="065ce-196">**GUID**: DXVA\_COPPQueryProtectionType</span></span>
-   <span data-ttu-id="065ce-197">**Dati di input**: nessuno.</span><span class="sxs-lookup"><span data-stu-id="065ce-197">**Input data**: None.</span></span>
-   <span data-ttu-id="065ce-198">**Dati restituiti**: restituisce una [**struttura \_ COPPStatusData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="065ce-198">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="065ce-199">I meccanismi di protezione vengono restituiti nel membro **dwData** come una combinazione di zero o più flag.</span><span class="sxs-lookup"><span data-stu-id="065ce-199">The protection mechanisms are returned in the **dwData** member as a combination of zero or more flags.</span></span> <span data-ttu-id="065ce-200">Vedere [flag del tipo di protezione Copp](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="065ce-200">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span> <span data-ttu-id="065ce-201">Se è disponibile più di un meccanismo di protezione, i flag vengono combinati con un **or** bit per bit.</span><span class="sxs-lookup"><span data-stu-id="065ce-201">If more than one protection mechanism is available, the flags are combined with a bitwise **OR**.</span></span>

<span data-ttu-id="065ce-202">Query di segnalazione</span><span class="sxs-lookup"><span data-stu-id="065ce-202">Signaling Query</span></span>

<span data-ttu-id="065ce-203">Restituisce un elenco di tutti gli standard di protezione supportati dal driver, lo standard attualmente attivo e le proporzioni correnti o altri dati di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="065ce-203">Returns a list of all the protection standards that are supported by the driver, the standard that is currently active, and the current aspect ratio or other signaling data.</span></span>

-   <span data-ttu-id="065ce-204">**GUID**: DXVA \_ COPPQuerySignaling</span><span class="sxs-lookup"><span data-stu-id="065ce-204">**GUID**: DXVA\_COPPQuerySignaling</span></span>
-   <span data-ttu-id="065ce-205">**Dati di input**: nessuno.</span><span class="sxs-lookup"><span data-stu-id="065ce-205">**Input data**: None.</span></span>
-   <span data-ttu-id="065ce-206">**Dati restituiti**: restituisce una [**struttura \_ COPPStatusSignalingCmdData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) .</span><span class="sxs-lookup"><span data-stu-id="065ce-206">**Return data**: Returns a [**DXVA\_COPPStatusSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="065ce-207">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="065ce-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="065ce-208">Uso di COPP (Certified Output Protocol)</span><span class="sxs-lookup"><span data-stu-id="065ce-208">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



