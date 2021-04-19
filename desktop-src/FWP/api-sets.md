---
title: API PAM
description: L'API Windows Filtering Platform (WFP) è divisa nei componenti seguenti.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4230c82105f85c36e6fb112508a7128758b2ad60
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "106300720"
---
# <a name="wfp-api"></a><span data-ttu-id="f88af-103">API PAM</span><span class="sxs-lookup"><span data-stu-id="f88af-103">WFP API</span></span>

<span data-ttu-id="f88af-104">L'API Windows Filtering Platform (WFP) è divisa nei componenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="f88af-104">The Windows Filtering Platform (WFP) API is divided into the following components.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f88af-105">Componente</span><span class="sxs-lookup"><span data-stu-id="f88af-105">Component</span></span></th>
<th><span data-ttu-id="f88af-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f88af-106">Description</span></span></th>
<th><span data-ttu-id="f88af-107">File di intestazione</span><span class="sxs-lookup"><span data-stu-id="f88af-107">Header Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f88af-108"><a href="/windows-hardware/drivers/ddi/_netvista/">API callout</a> (FWPS) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f88af-108"><a href="/windows-hardware/drivers/ddi/_netvista/">Callout API</a> (FWPS)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f88af-109"><a href="/windows-hardware/drivers/ddi/_netvista/">Tipi di dati</a> utilizzati dai callout. <strong>Nota</strong>  Questi tipi di dati sono documentati in Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="f88af-109"><a href="/windows-hardware/drivers/ddi/_netvista/">Data types</a> used by callouts.<strong>Note</strong>  These data types are documented in the Microsoft Windows Driver Development Kit (DDK).</span></span><br/></td>
<td><dl> <span data-ttu-id="f88af-110">fwpstypes. h</span><span class="sxs-lookup"><span data-stu-id="f88af-110">fwpstypes.h</span></span><br />
<span data-ttu-id="f88af-111">fwpstypes. idl</span><span class="sxs-lookup"><span data-stu-id="f88af-111">fwpstypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f88af-112"><a href="/windows-hardware/drivers/ddi/_netvista/">Funzioni</a> e <a href="/windows-hardware/drivers/ddi/_netvista/">tipi enumerati</a> usati per implementare i callout. <strong>Nota</strong>  Queste funzioni e i tipi enumerati sono documentati in DDK.</span><span class="sxs-lookup"><span data-stu-id="f88af-112"><a href="/windows-hardware/drivers/ddi/_netvista/">Functions</a> and <a href="/windows-hardware/drivers/ddi/_netvista/">enumerated types</a> used to implement callouts.<strong>Note</strong>  These functions and enumerated types are documented in the DDK.</span></span><br/></td>
<td><dl> <span data-ttu-id="f88af-113">fwpsu. h</span><span class="sxs-lookup"><span data-stu-id="f88af-113">fwpsu.h</span></span><br />
<span data-ttu-id="f88af-114">fwpsk. h</span><span class="sxs-lookup"><span data-stu-id="f88af-114">fwpsk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f88af-115">API IKE/AuthIP (IKEEXT) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="f88af-115">IKE/AuthIP API (IKEEXT)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f88af-116"><a href="fwp-enums.md">Tipi enumerati</a> e <a href="fwp-structs.md">strutture</a> usati per gestire le associazioni di sicurezza e i criteri della modalità principale IKE e AuthIP (mm).</span><span class="sxs-lookup"><span data-stu-id="f88af-116"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IKE and AuthIP main mode (MM) policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="f88af-117">iketypes. h</span><span class="sxs-lookup"><span data-stu-id="f88af-117">iketypes.h</span></span><br />
<span data-ttu-id="f88af-118">iketypes. idl</span><span class="sxs-lookup"><span data-stu-id="f88af-118">iketypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f88af-119"><a href="fwp-ike-functions.md">Funzioni</a> usate per gestire i criteri e le associazioni di sicurezza di IKE e AuthIP mm.</span><span class="sxs-lookup"><span data-stu-id="f88af-119"><a href="fwp-ike-functions.md">Functions</a> used for managing IKE and AuthIP MM policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="f88af-120">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="f88af-120">fwpmu.h</span></span><br />
<span data-ttu-id="f88af-121">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="f88af-121">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f88af-122">API IPsec (IPSEC) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="f88af-122">IPsec API (IPSEC)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f88af-123"><a href="fwp-enums.md">Tipi enumerati</a> e <a href="fwp-structs.md">strutture</a> utilizzati per gestire i criteri IPSec e le associazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f88af-123"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="f88af-124">ipsectypes. h</span><span class="sxs-lookup"><span data-stu-id="f88af-124">ipsectypes.h</span></span><br />
<span data-ttu-id="f88af-125">ipsectypes. idl</span><span class="sxs-lookup"><span data-stu-id="f88af-125">ipsectypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f88af-126"><a href="fwp-ipsec-functions.md">Funzioni</a> utilizzate per gestire i criteri IPSec e le associazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f88af-126"><a href="fwp-ipsec-functions.md">Functions</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="f88af-127">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="f88af-127">fwpmu.h</span></span><br />
<span data-ttu-id="f88af-128">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="f88af-128">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f88af-129">API di gestione (FWPM) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="f88af-129">Management API (FWPM)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f88af-130"><a href="fwp-enums.md">Tipi enumerati</a> e <a href="fwp-structs.md">strutture</a> utilizzati per gestire il motore di filtro.</span><span class="sxs-lookup"><span data-stu-id="f88af-130"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing the filter engine.</span></span></td>
<td><dl> <span data-ttu-id="f88af-131">fwpmtypes. h</span><span class="sxs-lookup"><span data-stu-id="f88af-131">fwpmtypes.h</span></span><br />
<span data-ttu-id="f88af-132">fwpmtypes. idl</span><span class="sxs-lookup"><span data-stu-id="f88af-132">fwpmtypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f88af-133"><a href="fwp-mgmt-functions.md">Funzioni</a> utilizzate per gestire il motore di filtro.</span><span class="sxs-lookup"><span data-stu-id="f88af-133"><a href="fwp-mgmt-functions.md">Functions</a> used for managing the filter engine.</span></span> <span data-ttu-id="f88af-134">Queste funzioni vengono usate per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="f88af-134">These functions are used to perform the following tasks:</span></span><br/>
<ul>
<li><span data-ttu-id="f88af-135">Set ed esecuzione di query su filtri, provider e callout.</span><span class="sxs-lookup"><span data-stu-id="f88af-135">Set and query filters, providers, and callouts.</span></span></li>
<li><span data-ttu-id="f88af-136">Recuperare le statistiche IPsec.</span><span class="sxs-lookup"><span data-stu-id="f88af-136">Retrieve IPsec statistics.</span></span></li>
<li><span data-ttu-id="f88af-137">Configurare la piattaforma filtro Windows.</span><span class="sxs-lookup"><span data-stu-id="f88af-137">Configure the Windows Filtering Platform.</span></span></li>
</ul></td>
<td><dl> <span data-ttu-id="f88af-138">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="f88af-138">fwpmu.h</span></span><br />
<span data-ttu-id="f88af-139">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="f88af-139">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f88af-140">API condivisa (FWP)</span><span class="sxs-lookup"><span data-stu-id="f88af-140">Shared API (FWP)</span></span></td>
<td><span data-ttu-id="f88af-141"><a href="fwp-enums.md">Tipi enumerati</a> fondamentali e <a href="fwp-structs.md">strutture</a> condivise attraverso la piattaforma filtro Windows.</span><span class="sxs-lookup"><span data-stu-id="f88af-141">Fundamental <a href="fwp-enums.md">enumerated types</a> and <a href="fwp-structs.md">structures</a> shared across the Windows Filtering Platform.</span></span></td>
<td><dl> <span data-ttu-id="f88af-142">fwptypes. h</span><span class="sxs-lookup"><span data-stu-id="f88af-142">fwptypes.h</span></span><br />
<span data-ttu-id="f88af-143">fwptypes. idl</span><span class="sxs-lookup"><span data-stu-id="f88af-143">fwptypes.idl</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f88af-144">I nomi dei tipi di dati sono delimitati da caratteri maiuscoli e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="f88af-144">Data type names are all upper-case and underscore-delimited.</span></span> <span data-ttu-id="f88af-145">Il nome inizia sempre con un prefisso che identifica il gruppo di componenti, ad esempio [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).</span><span class="sxs-lookup"><span data-stu-id="f88af-145">The name always begins with a prefix that identifies its component group, such as [**FWPM\_PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).</span></span>

<span data-ttu-id="f88af-146">I nomi di funzione sono di combinazione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f88af-146">Function names are mixed-case and case-delimited.</span></span> <span data-ttu-id="f88af-147">Il nome inizia sempre con un prefisso che identifica il gruppo di componenti, ad esempio [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).</span><span class="sxs-lookup"><span data-stu-id="f88af-147">The name always begins with a prefix that identifies its component group, such as [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).</span></span>

<span data-ttu-id="f88af-148">La maggior parte dei nomi di funzione e di dati termina con un numero di versione.</span><span class="sxs-lookup"><span data-stu-id="f88af-148">Most data and function names end with a version number.</span></span> <span data-ttu-id="f88af-149">Il file di intestazione fwpvi. h esegue il mapping dei nomi delle funzioni e dei dati indipendenti dalla versione alla versione appropriata per l'uso con un determinato sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f88af-149">The fwpvi.h header file maps version-independent data and function names to the version that is appropriate for use with a given operating system.</span></span> <span data-ttu-id="f88af-150">Per ulteriori informazioni, vedere la pagina relativa ai [nomi Version-Independent WFP e alle versioni specifiche di Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).</span><span class="sxs-lookup"><span data-stu-id="f88af-150">For more information, see [WFP Version-Independent Names and Targeting Specific Versions of Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).</span></span>

<span data-ttu-id="f88af-151">Ogni componente non è autonomo.</span><span class="sxs-lookup"><span data-stu-id="f88af-151">Each component does not stand alone.</span></span> <span data-ttu-id="f88af-152">Ad esempio, i criteri della modalità principale IKE (MM) sono definiti nel componente IKEEXT, ma vengono archiviati in un contesto del provider e sono associati a un filtro che si trovano nel componente API FWPM.</span><span class="sxs-lookup"><span data-stu-id="f88af-152">For example, IKE main mode (MM) policies are defined in the IKEEXT component, but are stored in a provider context and are associated with a filter both of which are found in the FWPM API component.</span></span>

## <a name="user-mode-and-kernel-mode-public-header-files"></a><span data-ttu-id="f88af-153">User-Mode e Kernel-Mode file di intestazione pubblica</span><span class="sxs-lookup"><span data-stu-id="f88af-153">User-Mode and Kernel-Mode Public Header Files</span></span>

<span data-ttu-id="f88af-154">La maggior parte delle funzioni PAM può essere chiamata dalla modalità utente o dalla modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="f88af-154">Most of the WFP functions can be called from either user mode or kernel mode.</span></span> <span data-ttu-id="f88af-155">Tuttavia, le funzioni in modalità utente restituiscono un valore **DWORD** che rappresenta un codice di errore Win32, mentre le funzioni in modalità kernel restituiscono un valore **NTSTATUS** che rappresenta un codice di stato NT.</span><span class="sxs-lookup"><span data-stu-id="f88af-155">However, user-mode functions return a **DWORD** value that represents a Win32 error code, whereas kernel-mode functions return an **NTSTATUS** value that represents an NT status code.</span></span> <span data-ttu-id="f88af-156">Di conseguenza, i nomi di funzione e la semantica sono identici tra la modalità utente e la modalità kernel, ma le firme di funzione non lo sono.</span><span class="sxs-lookup"><span data-stu-id="f88af-156">As a result, function names and semantics are identical between user mode and kernel mode, but function signatures are not.</span></span> <span data-ttu-id="f88af-157">Questa operazione richiede intestazioni specifiche in modalità utente e kernel separate per i prototipi di funzione.</span><span class="sxs-lookup"><span data-stu-id="f88af-157">This requires separate user-mode and kernel-mode specific headers for the function prototypes.</span></span> <span data-ttu-id="f88af-158">I nomi dei file di intestazione in modalità utente terminano con "u" e i nomi dei file di intestazione in modalità kernel terminano con "k".</span><span class="sxs-lookup"><span data-stu-id="f88af-158">User-mode header file names end in "u" and kernel-mode header file names end in "k".</span></span>

<span data-ttu-id="f88af-159">Nella tabella seguente sono elencati i file di intestazione Win32 che definiscono le funzioni Pam.</span><span class="sxs-lookup"><span data-stu-id="f88af-159">The following table lists the Win32 header files that define the WFP functions.</span></span>

| <span data-ttu-id="f88af-160">File di intestazione</span><span class="sxs-lookup"><span data-stu-id="f88af-160">Header Files</span></span> | <span data-ttu-id="f88af-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f88af-161">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f88af-162">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="f88af-162">fwpmk.h</span></span>      | <span data-ttu-id="f88af-163">Prototipi di funzioni in modalità kernel per i componenti FWPM, IPsec e IKEEXT.</span><span class="sxs-lookup"><span data-stu-id="f88af-163">Kernel-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="f88af-164">Disponibile solo nel DDK.</span><span class="sxs-lookup"><span data-stu-id="f88af-164">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="f88af-165">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="f88af-165">fwpmu.h</span></span>      | <span data-ttu-id="f88af-166">Prototipi di funzioni in modalità utente per i componenti FWPM, IPsec e IKEEXT.</span><span class="sxs-lookup"><span data-stu-id="f88af-166">User-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="f88af-167">Disponibile solo in Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f88af-167">Available in the Microsoft Windows Software Development Kit (SDK) only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f88af-168">fwpsk. h</span><span class="sxs-lookup"><span data-stu-id="f88af-168">fwpsk.h</span></span>      | <span data-ttu-id="f88af-169">Prototipi di funzioni in modalità kernel e tipi enumerati per il componente FWPS.</span><span class="sxs-lookup"><span data-stu-id="f88af-169">Kernel-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="f88af-170">Disponibile solo nel DDK.</span><span class="sxs-lookup"><span data-stu-id="f88af-170">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f88af-171">fwpsu. h</span><span class="sxs-lookup"><span data-stu-id="f88af-171">fwpsu.h</span></span>      | <span data-ttu-id="f88af-172">Prototipi di funzioni in modalità utente e tipi enumerati per il componente FWPS.</span><span class="sxs-lookup"><span data-stu-id="f88af-172">User-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="f88af-173">Disponibile solo nel Windows SDK. **Nota**  I tipi enumerati FWPS in modalità utente sono identici ai tipi enumerati FWPS in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="f88af-173">Available in the Windows SDK only.**Note**  The user-mode FWPS enumerated types are identical to the kernel-mode FWPS enumerated types.</span></span> <span data-ttu-id="f88af-174">Di conseguenza, questi tipi sono documentati solo nel DDK.</span><span class="sxs-lookup"><span data-stu-id="f88af-174">In consequence, these types are documented in the DDK only.</span></span><br/> <span data-ttu-id="f88af-175">**Nota**  I prototipi di funzione FWPS in modalità utente sono identici ai prototipi di funzione FWPS in modalità kernel, ad eccezione del codice restituito.</span><span class="sxs-lookup"><span data-stu-id="f88af-175">**Note**  The user-mode FWPS function prototypes are identical to the kernel-mode FWPS function prototypes with the exception of the return code.</span></span> <span data-ttu-id="f88af-176">Le funzioni FWPS in modalità utente restituiscono un **valore DWORD**, mentre le funzioni FWPS in modalità kernel restituiscono un **NTSTATUS**.</span><span class="sxs-lookup"><span data-stu-id="f88af-176">User-mode FWPS functions return a **DWORD**, whereas kernel-mode FWPS functions return an **NTSTATUS**.</span></span> <span data-ttu-id="f88af-177">Di conseguenza, queste funzioni sono documentate solo nel DDK.</span><span class="sxs-lookup"><span data-stu-id="f88af-177">In consequence, these functions are documented in the DDK only.</span></span><br/> |



 

<span data-ttu-id="f88af-178">Tutte le funzioni in modalità utente vengono esportate da fwpuclnt.dll.</span><span class="sxs-lookup"><span data-stu-id="f88af-178">All user-mode functions are exported from fwpuclnt.dll.</span></span> <span data-ttu-id="f88af-179">Tutte le funzioni in modalità kernel vengono esportate da fwpkclnt.sys.</span><span class="sxs-lookup"><span data-stu-id="f88af-179">All kernel-mode functions are exported from fwpkclnt.sys.</span></span>

### <a name="management-fwpm-and-callout-fwps-data-types"></a><span data-ttu-id="f88af-180">Tipi di dati di gestione (FWPM) e callout (FWPS)</span><span class="sxs-lookup"><span data-stu-id="f88af-180">Management (FWPM) and Callout (FWPS) Data Types</span></span>

<span data-ttu-id="f88af-181">La maggior parte dei tipi di dati FWPM, usati per le attività di gestione, ad esempio l'aggiunta di filtri o callout da un'applicazione o un driver, hanno controparti FWPS.</span><span class="sxs-lookup"><span data-stu-id="f88af-181">Most FWPM data types, which are used for management tasks such as adding filters or callouts from an application or driver, have FWPS counterparts.</span></span> <span data-ttu-id="f88af-182">I tipi di dati FWPS vengono usati durante l'effettivo filtro del traffico di rete nel contesto di una routine di callout per la classificazione.</span><span class="sxs-lookup"><span data-stu-id="f88af-182">The FWPS data types are used during the actual filtering of network traffic, in the context of a callout routine for classification.</span></span>

<span data-ttu-id="f88af-183">Per aggiungere un filtro a un determinato livello del motore di filtro, ad esempio, il programmatore deve usare un tipo FWPM, come: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` .</span><span class="sxs-lookup"><span data-stu-id="f88af-183">For example, in order to add a filter to a certain filtering engine layer, the programmer should use an FWPM type, like: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET`.</span></span> <span data-ttu-id="f88af-184">Per verificare da quale livello viene chiamato un callout, il programmatore deve usare il tipo FWPS corrispondente: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .</span><span class="sxs-lookup"><span data-stu-id="f88af-184">To check which layer a callout is being called from, the programmer should use the corresponding FWPS type: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)`.</span></span>

<span data-ttu-id="f88af-185">Alcune controparti FWPS per i tipi di dati FWPM stanno espandendo i tipi di dati FWPM originali.</span><span class="sxs-lookup"><span data-stu-id="f88af-185">Some FWPS counterparts to FWPM data types are expanding the original FWPM data types.</span></span> <span data-ttu-id="f88af-186">Ad esempio, per aggiungere una condizione di filtro a molti livelli del motore di filtro, il programmatore specifica `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` indipendentemente dal livello del motore di filtraggio.</span><span class="sxs-lookup"><span data-stu-id="f88af-186">For example, to add a filter condition at many filtering engine layers, the programmer specifies the `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` regardless of the filtering engine layer.</span></span> <span data-ttu-id="f88af-187">Per trovare un valore della condizione di filtro, il programmatore specifica un tipo FWPS specifico del livello, ad esempio: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` .</span><span class="sxs-lookup"><span data-stu-id="f88af-187">To find a filter condition value, the programmer specifies a layer specific FWPS type, like: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]`.</span></span>

<span data-ttu-id="f88af-188">I tipi di dati FWPS sono in genere inferiori alle rispettive controparti FWPM.</span><span class="sxs-lookup"><span data-stu-id="f88af-188">The FWPS data types are generally smaller than their FWPM counterparts.</span></span> <span data-ttu-id="f88af-189">Ad esempio, gli [**identificatori del livello di filtro FWPM**](management-filtering-layer-identifiers-.md) sono **GUID** s (16 byte), mentre gli [identificatori del livello di filtro FWPS](/windows-hardware/drivers/network/management-filtering-layer-identifiers) sono **UInt16** (16 bit).</span><span class="sxs-lookup"><span data-stu-id="f88af-189">For example, the [**FWPM filtering layer identifiers**](management-filtering-layer-identifiers-.md) are **GUID** s (16-bytes) whereas the [FWPS filtering layer identifiers](/windows-hardware/drivers/network/management-filtering-layer-identifiers) are **UINT16** (16-bits).</span></span> <span data-ttu-id="f88af-190">Le dimensioni più piccole per i tipi di dati FWPS migliorano le prestazioni del sistema poiché i confronti integer superano i confronti **GUID** per il traffico in tempo reale</span><span class="sxs-lookup"><span data-stu-id="f88af-190">The smaller size for FWPS data types improves system performance since integer comparisons outweigh **GUID** comparisons for real-time traffic.</span></span> <span data-ttu-id="f88af-191">Inoltre, la memoria del kernel viene usata in modo efficiente poiché i tipi FWPS sono tutti usati nel kernel per la gestione dei filtri, mentre i tipi FWPM vengono archiviati in modalità utente per gestire i diversi livelli.</span><span class="sxs-lookup"><span data-stu-id="f88af-191">Also, the kernel memory is used efficiently since the FWPS types are all used in the kernel for managing the filters, whereas the FWPM types are stored in user-mode to manage the different layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f88af-192">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f88af-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f88af-193">Modello a oggetti dell'API WFP</span><span class="sxs-lookup"><span data-stu-id="f88af-193">WFP API Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="f88af-194">Gestione degli oggetti dell'API WFP</span><span class="sxs-lookup"><span data-stu-id="f88af-194">WFP API Object Management</span></span>](object-management.md)
</dt> </dl>

