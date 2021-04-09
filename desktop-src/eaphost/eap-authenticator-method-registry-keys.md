---
title: Valori del registro di sistema del metodo di autenticazione EAP
description: Informazioni sui valori del registro di sistema del metodo EAP Authenticator. Questi valori specifici del registro di sistema sono necessari per i metodi di autenticazione EAP.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a710ca6f09914c8d111c42a8323a9c39c51f898
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963469"
---
# <a name="eap-authenticator-method-registry-values"></a><span data-ttu-id="ed612-104">Valori del registro di sistema del metodo di autenticazione EAP</span><span class="sxs-lookup"><span data-stu-id="ed612-104">EAP Authenticator Method Registry Values</span></span>

<span data-ttu-id="ed612-105">Per i metodi di autenticazione EAP sono necessari valori specifici del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ed612-105">Specific registry values are required for EAP authenticator methods.</span></span>

## <a name="eap-authenticator-method-dll-paths"></a><span data-ttu-id="ed612-106">Percorsi DLL del metodo di autenticazione EAP</span><span class="sxs-lookup"><span data-stu-id="ed612-106">EAP Authenticator Method DLL Paths</span></span>

<span data-ttu-id="ed612-107">Il percorso seguente specifica il percorso del registro di sistema per le dll normali del metodo di autenticazione EAP.</span><span class="sxs-lookup"><span data-stu-id="ed612-107">The following path specifies the registry location for regular EAP authenticator method DLLs.</span></span>

<span data-ttu-id="ed612-108">**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ metodi \\ *&lt; autorizzati &gt;* \\ \* &lt; EapTypeId&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="ed612-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="ed612-109">Ad esempio, un percorso di registrazione per l'installazione di un metodo di autenticazione EAP, dato un **autorizzazione** di "311" (che indica che "Microsoft" è l'autore) e un **EapTypeId** di "40", viene visualizzato come segue.</span><span class="sxs-lookup"><span data-stu-id="ed612-109">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="ed612-110">**HKLM \\ System \\ CCS \\ Services \\ ( \\ metodi EAPHost) \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="ed612-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="ed612-111">Il percorso seguente specifica il percorso del registro di sistema per le DLL dei metodi di autenticazione EAP estese.</span><span class="sxs-lookup"><span data-stu-id="ed612-111">The following path specifies the registry location for extended EAP authenticator method DLLs.</span></span>

<span data-ttu-id="ed612-112">**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; autorizzato &gt;* \\ 254 \\ *&lt; VendorID &gt;* \\ \* &lt; VendorType&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="ed612-112">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;VendorType&gt;**\*</span></span>

<span data-ttu-id="ed612-113">Ad esempio, un percorso di registrazione per l'installazione di un metodo di autenticazione EAP, dato un **autorizzazione** di "311" (che indica che "Microsoft" è l'autore), un **VendorId** di "311" e un **EapTypeId** di "40", viene visualizzato come segue.</span><span class="sxs-lookup"><span data-stu-id="ed612-113">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="ed612-114">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ methods \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="ed612-114">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="ed612-115">Per ulteriori informazioni sull'allocazione dei tipi di metodo EAP, vedere la sezione 6,2 della [specifica RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span><span class="sxs-lookup"><span data-stu-id="ed612-115">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="ed612-116">Valori del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ed612-116">Registry Values</span></span>

<span data-ttu-id="ed612-117">Sono necessari i seguenti valori del registro di sistema del metodo Authenticator.</span><span class="sxs-lookup"><span data-stu-id="ed612-117">The following authenticator method registry values are required.</span></span>

-   [<span data-ttu-id="ed612-118">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="ed612-118">AuthenticatorDllPath</span></span>](#authenticatordllpath)
-   [<span data-ttu-id="ed612-119">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ed612-119">AuthenticatorFriendlyName</span></span>](#authenticatorfriendlyname)

<span data-ttu-id="ed612-120">Oltre ai valori del registro di sistema indicati di seguito, è consigliato il seguente valore del registro di sistema del metodo Authenticator.</span><span class="sxs-lookup"><span data-stu-id="ed612-120">Besides the above registry values, the following authenticator method registry value is recommended.</span></span>

-   [<span data-ttu-id="ed612-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ed612-121">Properties</span></span>](#properties)

<span data-ttu-id="ed612-122">I valori del registro di sistema del metodo Authenticator rimanenti sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="ed612-122">The remaining authenticator method registry values are optional.</span></span>

-   [<span data-ttu-id="ed612-123">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="ed612-123">ConfigCLSID</span></span>](#configclsid)
-   [<span data-ttu-id="ed612-124">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="ed612-124">StandaloneSupported</span></span>](#standalonesupported)

## <a name="authenticatordllpath"></a><span data-ttu-id="ed612-125">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="ed612-125">AuthenticatorDllPath</span></span>



| <span data-ttu-id="ed612-126">Constant Value</span><span class="sxs-lookup"><span data-stu-id="ed612-126">Constant Value</span></span> | <span data-ttu-id="ed612-127">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="ed612-127">AuthenticatorDllPath</span></span>                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed612-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed612-128">Type</span></span>           | <span data-ttu-id="ed612-129">REG \_ Espandi \_ SZ</span><span class="sxs-lookup"><span data-stu-id="ed612-129">REG\_EXPAND\_SZ</span></span>                                                                                               |
| <span data-ttu-id="ed612-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed612-130">Description</span></span>    | <span data-ttu-id="ed612-131">Percorso della DLL del metodo di autenticazione EAP.</span><span class="sxs-lookup"><span data-stu-id="ed612-131">The path to the EAP authenticator method DLL.</span></span> <span data-ttu-id="ed612-132">Ad esempio,% SystemRoot% \\ system32 \\ &lt; nome \_ di \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="ed612-132">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

## <a name="authenticatorfriendlyname"></a><span data-ttu-id="ed612-133">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ed612-133">AuthenticatorFriendlyName</span></span>



| <span data-ttu-id="ed612-134">Constant Value</span><span class="sxs-lookup"><span data-stu-id="ed612-134">Constant Value</span></span> | <span data-ttu-id="ed612-135">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ed612-135">AuthenticatorFriendlyName</span></span>                                                          |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed612-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed612-136">Type</span></span>           | <span data-ttu-id="ed612-137">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="ed612-137">REG\_SZ</span></span>                                                                            |
| <span data-ttu-id="ed612-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed612-138">Description</span></span>    | <span data-ttu-id="ed612-139">Stringa che contiene il nome descrittivo (visualizzazione) per il metodo di autenticazione EAP.</span><span class="sxs-lookup"><span data-stu-id="ed612-139">String that contains the friendly (display) name for the EAP authenticator method.</span></span> |



 

## <a name="configclsid"></a><span data-ttu-id="ed612-140">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="ed612-140">ConfigCLSID</span></span>



| <span data-ttu-id="ed612-141">Constant Value</span><span class="sxs-lookup"><span data-stu-id="ed612-141">Constant Value</span></span> | <span data-ttu-id="ed612-142">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="ed612-142">ConfigCLSID</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed612-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed612-143">Type</span></span>           | <span data-ttu-id="ed612-144">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="ed612-144">REG\_SZ</span></span>                                                                                                                               |
| <span data-ttu-id="ed612-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed612-145">Description</span></span>    | <span data-ttu-id="ed612-146">Stringa che contiene il GUID della classe di configurazione per questo metodo di autenticazione, nel formato {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="ed612-146">String that contains the configuration class GUID for this authenticator method, in the format {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span></span> |



 

## <a name="properties"></a><span data-ttu-id="ed612-147">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ed612-147">Properties</span></span>



| <span data-ttu-id="ed612-148">Constant Value</span><span class="sxs-lookup"><span data-stu-id="ed612-148">Constant Value</span></span> | <span data-ttu-id="ed612-149">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ed612-149">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed612-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed612-150">Type</span></span>           | <span data-ttu-id="ed612-151">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="ed612-151">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="ed612-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed612-152">Description</span></span>    | <span data-ttu-id="ed612-153">I bit in DWORD sono impostati per indicare il supporto per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="ed612-153">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="ed612-154">Per un elenco dei valori supportati, vedere [**proprietà del metodo EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ed612-154">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="standalonesupported"></a><span data-ttu-id="ed612-155">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="ed612-155">StandaloneSupported</span></span>



| <span data-ttu-id="ed612-156">Constant Value</span><span class="sxs-lookup"><span data-stu-id="ed612-156">Constant Value</span></span> | <span data-ttu-id="ed612-157">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="ed612-157">StandaloneSupported</span></span>                                             |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="ed612-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed612-158">Type</span></span>           | <span data-ttu-id="ed612-159">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="ed612-159">REG\_DWORD</span></span>                                                      |
| <span data-ttu-id="ed612-160">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed612-160">Description</span></span>    | <span data-ttu-id="ed612-161">0 se si tratta di un metodo di autenticazione autonomo; 1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ed612-161">0 if this is a standalone authenticator method; 1 if it is not.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ed612-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ed612-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed612-163">Chiavi del registro di sistema del peer EAP</span><span class="sxs-lookup"><span data-stu-id="ed612-163">EAP Peer Method Registry Keys</span></span>](eap-peer-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="ed612-164">Configurazione del registro di sistema per i tipi EAP espansi</span><span class="sxs-lookup"><span data-stu-id="ed612-164">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="ed612-165">Uso di EAPHost</span><span class="sxs-lookup"><span data-stu-id="ed612-165">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="ed612-166">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="ed612-166">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




