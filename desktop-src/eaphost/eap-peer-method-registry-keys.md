---
title: Valori del registro di sistema del metodo peer EAP
description: Informazioni sui valori specifici del registro di sistema necessari per i metodi peer EAP. Vedere un elenco di valori del registro di sistema e visualizzare altre risorse disponibili.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796260a25f824ffe52ada7cdfadfb7a25f05d491
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339286"
---
# <a name="eap-peer-method-registry-values"></a><span data-ttu-id="f33ec-104">Valori del registro di sistema del metodo peer EAP</span><span class="sxs-lookup"><span data-stu-id="f33ec-104">EAP Peer Method Registry Values</span></span>

<span data-ttu-id="f33ec-105">Per i metodi peer EAP sono necessari valori specifici del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f33ec-105">Specific registry values are required for EAP peer methods.</span></span>

## <a name="eap-peer-method-dll-paths"></a><span data-ttu-id="f33ec-106">Percorsi DLL del metodo peer EAP</span><span class="sxs-lookup"><span data-stu-id="f33ec-106">EAP Peer Method DLL Paths</span></span>

<span data-ttu-id="f33ec-107">Il percorso seguente specifica il percorso del registro di sistema per le DLL regolari del metodo peer EAP.</span><span class="sxs-lookup"><span data-stu-id="f33ec-107">The following path specifies the registry location for regular EAP peer method DLLs.</span></span>

<span data-ttu-id="f33ec-108">**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ metodi \\ *&lt; autorizzati &gt;* \\ \* &lt; EapTypeId&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="f33ec-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="f33ec-109">Un percorso di registrazione per l'installazione di un metodo EAP, ad esempio, dato un **autorizzazione** di "311" (che indica che "Microsoft" è l'autore) e un **EapTypeId** di "40", viene visualizzato come segue.</span><span class="sxs-lookup"><span data-stu-id="f33ec-109">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="f33ec-110">**HKLM \\ System \\ CCS \\ Services \\ ( \\ metodi EAPHost) \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="f33ec-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="f33ec-111">Il percorso seguente specifica il percorso del registro di sistema per le dll del metodo EAP estese.</span><span class="sxs-lookup"><span data-stu-id="f33ec-111">The following path specifies the registry location for extended EAP method DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="f33ec-112">Le DLL dei metodi EAP estesi sono supportate in Windows Vista con Service Pack 1 (SP1) o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f33ec-112">Extended EAP method DLLs are supported in Windows Vista with Service Pack 1 (SP1) or later.</span></span>

 

<span data-ttu-id="f33ec-113">**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; autorizzato &gt;* \\ 254 \\ *&lt; VendorID &gt;* \\ \* &lt; EapTypeId&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="f33ec-113">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="f33ec-114">Un percorso di registrazione per l'installazione di un metodo EAP, ad esempio, dato un oggetto **autorizzato** di "311" (che indica che "Microsoft" è l'autore), un **VendorId** di "311" e un **EapTypeId** di "40" viene visualizzato come segue.</span><span class="sxs-lookup"><span data-stu-id="f33ec-114">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="f33ec-115">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ methods \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="f33ec-115">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="f33ec-116">Per ulteriori informazioni sull'allocazione dei tipi di metodo EAP, vedere la sezione 6,2 della [specifica RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span><span class="sxs-lookup"><span data-stu-id="f33ec-116">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="f33ec-117">Valori del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f33ec-117">Registry Values</span></span>

<span data-ttu-id="f33ec-118">Sono necessari i seguenti valori del registro di sistema del peer EAPHost.</span><span class="sxs-lookup"><span data-stu-id="f33ec-118">The following EAPHost peer method registry values are required.</span></span>

-   [<span data-ttu-id="f33ec-119">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="f33ec-119">PeerDllPath</span></span>](#peerdllpath)
-   [<span data-ttu-id="f33ec-120">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f33ec-120">PeerFriendlyName</span></span>](#peerfriendlyname)
-   [<span data-ttu-id="f33ec-121">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="f33ec-121">PeerInvokePasswordDialog</span></span>](#peerinvokepassworddialog)
-   [<span data-ttu-id="f33ec-122">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="f33ec-122">PeerInvokeUsernameDialog</span></span>](#peerinvokeusernamedialog)

<span data-ttu-id="f33ec-123">Sono consigliati i seguenti valori del registro di sistema del peer di AP.</span><span class="sxs-lookup"><span data-stu-id="f33ec-123">The following AP peer method registry values are recommended.</span></span>

-   [<span data-ttu-id="f33ec-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f33ec-124">Properties</span></span>](#properties)

<span data-ttu-id="f33ec-125">I valori del registro di sistema del peer AP seguenti sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="f33ec-125">The following AP peer method registry values are optional.</span></span>

-   [<span data-ttu-id="f33ec-126">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="f33ec-126">PeerConfigUIPath</span></span>](#peerconfiguipath)
-   [<span data-ttu-id="f33ec-127">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="f33ec-127">PeerIdentityPath</span></span>](#peeridentitypath)
-   [<span data-ttu-id="f33ec-128">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="f33ec-128">PeerInteractiveUIPath</span></span>](#peerinteractiveuipath)
-   [<span data-ttu-id="f33ec-129">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="f33ec-129">PeerRequireConfigUI</span></span>](#peerrequireconfigui)

### <a name="peerconfiguipath"></a><span data-ttu-id="f33ec-130">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="f33ec-130">PeerConfigUIPath</span></span>



| <span data-ttu-id="f33ec-131">Constant Value</span><span class="sxs-lookup"><span data-stu-id="f33ec-131">Constant Value</span></span> | <span data-ttu-id="f33ec-132">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="f33ec-132">PeerConfigUIPath</span></span>                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f33ec-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="f33ec-133">Type</span></span>           | <span data-ttu-id="f33ec-134">REG \_ Espandi \_ SZ</span><span class="sxs-lookup"><span data-stu-id="f33ec-134">REG\_EXPAND\_SZ</span></span>                                                                                                                                        |
| <span data-ttu-id="f33ec-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f33ec-135">Description</span></span>    | <span data-ttu-id="f33ec-136">Percorso della DLL che contiene l'implementazione della finestra di dialogo di configurazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f33ec-136">The path to the DLL that contains the implementation of the user configuration dialog.</span></span> <span data-ttu-id="f33ec-137">Ad esempio,% SystemRoot% \\ system32 \\ &lt; nome \_ di \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="f33ec-137">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerdllpath"></a><span data-ttu-id="f33ec-138">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="f33ec-138">PeerDllPath</span></span>



| <span data-ttu-id="f33ec-139">Constant Value</span><span class="sxs-lookup"><span data-stu-id="f33ec-139">Constant Value</span></span> | <span data-ttu-id="f33ec-140">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="f33ec-140">PeerDllPath</span></span>                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f33ec-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="f33ec-141">Type</span></span>           | <span data-ttu-id="f33ec-142">REG \_ Espandi \_ SZ</span><span class="sxs-lookup"><span data-stu-id="f33ec-142">REG\_EXPAND\_SZ</span></span>                                                                                 |
| <span data-ttu-id="f33ec-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f33ec-143">Description</span></span>    | <span data-ttu-id="f33ec-144">Percorso della DLL del metodo EAP.</span><span class="sxs-lookup"><span data-stu-id="f33ec-144">The path to the EAP method DLL.</span></span> <span data-ttu-id="f33ec-145">Ad esempio,% SystemRoot% \\ system32 \\ &lt; nome \_ di \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="f33ec-145">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerfriendlyname"></a><span data-ttu-id="f33ec-146">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f33ec-146">PeerFriendlyName</span></span>



| <span data-ttu-id="f33ec-147">Constant Value</span><span class="sxs-lookup"><span data-stu-id="f33ec-147">Constant Value</span></span> | <span data-ttu-id="f33ec-148">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f33ec-148">PeerFriendlyName</span></span>                                                     |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="f33ec-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="f33ec-149">Type</span></span>           | <span data-ttu-id="f33ec-150">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="f33ec-150">REG\_SZ</span></span>                                                              |
| <span data-ttu-id="f33ec-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f33ec-151">Description</span></span>    | <span data-ttu-id="f33ec-152">Stringa che contiene il nome descrittivo (visualizzazione) per il metodo EAP.</span><span class="sxs-lookup"><span data-stu-id="f33ec-152">String that contains the friendly (display) name for the EAP method.</span></span> |



 

### <a name="peeridentitypath"></a><span data-ttu-id="f33ec-153">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="f33ec-153">PeerIdentityPath</span></span>



| <span data-ttu-id="f33ec-154">Constant Value</span><span class="sxs-lookup"><span data-stu-id="f33ec-154">Constant Value</span></span> | <span data-ttu-id="f33ec-155">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="f33ec-155">PeerIdentityPath</span></span>                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f33ec-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="f33ec-156">Type</span></span>           | <span data-ttu-id="f33ec-157">REG \_ Espandi \_ SZ</span><span class="sxs-lookup"><span data-stu-id="f33ec-157">REG\_EXPAND\_SZ</span></span>                                                                                                                                      |
| <span data-ttu-id="f33ec-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f33ec-158">Description</span></span>    | <span data-ttu-id="f33ec-159">Percorso della DLL che contiene l'implementazione delle funzioni di identità utente.</span><span class="sxs-lookup"><span data-stu-id="f33ec-159">The path to the DLL that contains the implementation of the user identity functions.</span></span> <span data-ttu-id="f33ec-160">Ad esempio,% SystemRoot% \\ system32 \\ &lt; nome \_ di \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="f33ec-160">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinteractiveuipath"></a><span data-ttu-id="f33ec-161">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="f33ec-161">PeerInteractiveUIPath</span></span>



| <span data-ttu-id="f33ec-162">Constant Value</span><span class="sxs-lookup"><span data-stu-id="f33ec-162">Constant Value</span></span> | <span data-ttu-id="f33ec-163">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="f33ec-163">PeerInteractiveUIPath</span></span>                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f33ec-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="f33ec-164">Type</span></span>           | <span data-ttu-id="f33ec-165">REG \_ Espandi \_ SZ</span><span class="sxs-lookup"><span data-stu-id="f33ec-165">REG\_EXPAND\_SZ</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="f33ec-166">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f33ec-166">Description</span></span>    | <span data-ttu-id="f33ec-167">Percorso della DLL che contiene l'implementazione dell'interfaccia utente interattiva utilizzata per ottenere informazioni sull'utente durante l'esecuzione del metodo EAP.</span><span class="sxs-lookup"><span data-stu-id="f33ec-167">The path to the DLL that contains the implementation of the interactive user interface used to obtain user information during execution of the EAP method.</span></span> <span data-ttu-id="f33ec-168">Ad esempio,% SystemRoot% \\ system32 \\ &lt; nome \_ di \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="f33ec-168">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinvokepassworddialog"></a><span data-ttu-id="f33ec-169">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="f33ec-169">PeerInvokePasswordDialog</span></span>



| <span data-ttu-id="f33ec-170">Constant Value</span><span class="sxs-lookup"><span data-stu-id="f33ec-170">Constant Value</span></span> | <span data-ttu-id="f33ec-171">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="f33ec-171">PeerInvokePasswordDialog</span></span>                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f33ec-172">Tipo</span><span class="sxs-lookup"><span data-stu-id="f33ec-172">Type</span></span>           | <span data-ttu-id="f33ec-173">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="f33ec-173">REG\_DWORD</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="f33ec-174">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f33ec-174">Description</span></span>    | <span data-ttu-id="f33ec-175">1-per ottenere le credenziali tramite la finestra di dialogo Generic EAPHost password and Domain.</span><span class="sxs-lookup"><span data-stu-id="f33ec-175">1- to get credentials using the generic EAPHost password and domain dialog box.</span></span> <span data-ttu-id="f33ec-176">0: per utilizzare una finestra di dialogo personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f33ec-176">0 - to use a custom dialog box.</span></span> <span data-ttu-id="f33ec-177">Se viene utilizzata la finestra di dialogo generica, le credenziali vengono impostate dal metodo [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) .</span><span class="sxs-lookup"><span data-stu-id="f33ec-177">If the generic dialog box is used, credentials are set by the [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span> |



 

### <a name="peerinvokeusernamedialog"></a><span data-ttu-id="f33ec-178">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="f33ec-178">PeerInvokeUsernameDialog</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f33ec-179">Constant Value</span><span class="sxs-lookup"><span data-stu-id="f33ec-179">Constant Value</span></span></th>
<th><span data-ttu-id="f33ec-180">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="f33ec-180">PeerInvokeUsernameDialog</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f33ec-181">Tipo</span><span class="sxs-lookup"><span data-stu-id="f33ec-181">Type</span></span></td>
<td><span data-ttu-id="f33ec-182">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="f33ec-182">REG_DWORD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f33ec-183">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f33ec-183">Description</span></span></td>
<td><ul>
<li><span data-ttu-id="f33ec-184">1-per ottenere le credenziali utilizzando la finestra di dialogo nome utente generico EAPHost.</span><span class="sxs-lookup"><span data-stu-id="f33ec-184">1 - to get credentials using the generic EAPHost user name dialog box.</span></span></li>
<li><span data-ttu-id="f33ec-185">0: per utilizzare una finestra di dialogo personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f33ec-185">0- to use a custom dialog box.</span></span></li>
</ul>
<span data-ttu-id="f33ec-186">Se viene utilizzata la finestra di dialogo generica, le credenziali vengono impostate dal metodo [<strong>EapPeerSetCredentials</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetcredentials).</span><span class="sxs-lookup"><span data-stu-id="f33ec-186">If the generic dialog box is used, credentials are set by the [<strong>EapPeerSetCredentials</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="peerrequireconfigui"></a><span data-ttu-id="f33ec-187">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="f33ec-187">PeerRequireConfigUI</span></span>



| <span data-ttu-id="f33ec-188">Constant Value</span><span class="sxs-lookup"><span data-stu-id="f33ec-188">Constant Value</span></span> | <span data-ttu-id="f33ec-189">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="f33ec-189">PeerRequireConfigUI</span></span>                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f33ec-190">Tipo</span><span class="sxs-lookup"><span data-stu-id="f33ec-190">Type</span></span>           | <span data-ttu-id="f33ec-191">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="f33ec-191">REG\_DWORD</span></span>                                                                                 |
| <span data-ttu-id="f33ec-192">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f33ec-192">Description</span></span>    | <span data-ttu-id="f33ec-193">0 se viene implementata una finestra di dialogo dell'interfaccia utente di configurazione per questo metodo; 1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f33ec-193">0 if a configuration user interface dialog is implemented for this method; 1 if it is not.</span></span> |



 

### <a name="properties"></a><span data-ttu-id="f33ec-194">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f33ec-194">Properties</span></span>



| <span data-ttu-id="f33ec-195">Constant Value</span><span class="sxs-lookup"><span data-stu-id="f33ec-195">Constant Value</span></span> | <span data-ttu-id="f33ec-196">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f33ec-196">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f33ec-197">Tipo</span><span class="sxs-lookup"><span data-stu-id="f33ec-197">Type</span></span>           | <span data-ttu-id="f33ec-198">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="f33ec-198">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="f33ec-199">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f33ec-199">Description</span></span>    | <span data-ttu-id="f33ec-200">I bit in DWORD sono impostati per indicare il supporto per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="f33ec-200">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="f33ec-201">Per un elenco dei valori supportati, vedere [**proprietà del metodo EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f33ec-201">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f33ec-202">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f33ec-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f33ec-203">Chiavi del registro di sistema EAP Authenticator</span><span class="sxs-lookup"><span data-stu-id="f33ec-203">EAP Authenticator Method Registry Keys</span></span>](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="f33ec-204">Configurazione del registro di sistema per i tipi EAP espansi</span><span class="sxs-lookup"><span data-stu-id="f33ec-204">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="f33ec-205">Uso di EAPHost</span><span class="sxs-lookup"><span data-stu-id="f33ec-205">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="f33ec-206">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="f33ec-206">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 