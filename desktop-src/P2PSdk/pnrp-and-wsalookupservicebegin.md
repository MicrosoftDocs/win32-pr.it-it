---
description: PNRP utilizza la funzione WSALookupServiceBegin per avviare il processo che consente a un'applicazione di eseguire le operazioni seguenti.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP e WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78efd0ee28284cb41866795aea8a2a8d5f17e871
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322025"
---
# <a name="pnrp-and-wsalookupservicebegin"></a><span data-ttu-id="42927-103">PNRP e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="42927-103">PNRP and WSALookupServiceBegin</span></span>

<span data-ttu-id="42927-104">PNRP utilizza la funzione [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) per avviare il processo che consente a un'applicazione di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="42927-104">PNRP uses the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function to start the process that allows an application to do the following:</span></span>

-   [<span data-ttu-id="42927-105">Risoluzione di un nome</span><span class="sxs-lookup"><span data-stu-id="42927-105">Resolving a name</span></span>](#resolving-a-name)
-   [<span data-ttu-id="42927-106">Enumerazione dei cloud di rete</span><span class="sxs-lookup"><span data-stu-id="42927-106">Enumerating network clouds</span></span>](#enumerating-network-clouds)

<span data-ttu-id="42927-107">I client che tentano di eseguire una delle funzioni utilizzano le funzioni [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext** e **WSALookupServiceEnd** .</span><span class="sxs-lookup"><span data-stu-id="42927-107">Clients that attempt to perform one of the functions use the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span>

<span data-ttu-id="42927-108">Utilizzando [**WSANSPIoctl**](winsock-nsp-reference-links.md), il servizio di ricerca può essere utilizzato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="42927-108">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="42927-109">Per informazioni sull'uso asincrono delle funzioni del servizio di ricerca, vedere [PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md).</span><span class="sxs-lookup"><span data-stu-id="42927-109">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="42927-110">Il processo di utilizzo dei nomi di peer è diverso dall'utilizzo di cloud.</span><span class="sxs-lookup"><span data-stu-id="42927-110">The process for working with peer names is different from working with clouds.</span></span> <span data-ttu-id="42927-111">Ogni processo è descritto separatamente in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="42927-111">Each process is described separately in this topic.</span></span>

## <a name="resolving-a-name"></a><span data-ttu-id="42927-112">Risoluzione di un nome</span><span class="sxs-lookup"><span data-stu-id="42927-112">Resolving a Name</span></span>

<span data-ttu-id="42927-113">Un'applicazione utilizza [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) per ottenere l'indirizzo IP, la porta e il protocollo per un servizio peer registrato in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="42927-113">An application uses [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) to obtain the IP address, port, and protocol for a peer service that is registered on another computer.</span></span> <span data-ttu-id="42927-114">La funzione **WSALookupServiceBegin** viene usata per avviare il processo di risoluzione dei nomi e impostare i parametri e le restrizioni.</span><span class="sxs-lookup"><span data-stu-id="42927-114">The **WSALookupServiceBegin** function is used to start the name resolution process, and set up the parameters and restrictions.</span></span> <span data-ttu-id="42927-115">Viene restituito un handle e deve essere usato per chiamare **WSALookupServiceNext** e **WSANSPIoctl**.</span><span class="sxs-lookup"><span data-stu-id="42927-115">A handle is returned, and must be used when calling **WSALookupServiceNext** and **WSANSPIoctl**.</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="42927-116">lpqsRestrictions</span><span class="sxs-lookup"><span data-stu-id="42927-116">lpqsRestrictions</span></span>

<span data-ttu-id="42927-117">Quando si risolve un nome peer, la struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a cui fa riferimento il parametro *lpqsRestrictions* deve contenere i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="42927-117">When resolving a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="42927-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="42927-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="42927-119">Specifica le dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="42927-119">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="42927-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="42927-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="42927-121">Specifica un nome peer da risolvere.</span><span class="sxs-lookup"><span data-stu-id="42927-121">Specifies a peer name to resolve.</span></span>

</dd> <dt>

<span data-ttu-id="42927-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="42927-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="42927-123">Deve essere **SVCID \_ pnrpname**.</span><span class="sxs-lookup"><span data-stu-id="42927-123">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="42927-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="42927-125">Riservato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-125">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="42927-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="42927-127">Riservato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-127">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="42927-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="42927-129">Deve essere **NS \_ pnrpname** o **NS \_ All**.</span><span class="sxs-lookup"><span data-stu-id="42927-129">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="42927-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="42927-131">Deve essere il **\_ provider NS \_ pnrpname** o **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-131">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="42927-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="42927-133">Deve essere un nome di cloud, una stringa vuota o **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-133">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="42927-134">Se questo valore è **null** o una stringa vuota, viene utilizzato il cloud predefinito, \_ ovvero "Global".</span><span class="sxs-lookup"><span data-stu-id="42927-134">If this value is **NULL** or an empty string, the default cloud, "Global\_" is used.</span></span> <span data-ttu-id="42927-135">In caso contrario, deve puntare a un nome di cloud valido.</span><span class="sxs-lookup"><span data-stu-id="42927-135">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="42927-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="42927-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="42927-137">Riservato, deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="42927-137">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="42927-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="42927-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="42927-139">Riservato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-139">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="42927-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="42927-141">Riservato, deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="42927-141">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="42927-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="42927-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="42927-143">Riservato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-143">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="42927-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="42927-145">Riservato, deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="42927-145">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="42927-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="42927-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="42927-147">Deve essere un puntatore a una struttura [**BLOB**](winsock-nsp-reference-links.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-147">Must be either a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure or **NULL**.</span></span> <span data-ttu-id="42927-148">Se è **null**, vengono usati i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="42927-148">If it is **NULL**, default values are used.</span></span> <span data-ttu-id="42927-149">Se è impostato, **lpBlob** punta a una struttura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) ed è necessario impostare parametri specifici nella struttura **PNRPINFO** .</span><span class="sxs-lookup"><span data-stu-id="42927-149">If it is set, **lpBlob** points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure, and specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="42927-150">Per ulteriori informazioni, vedere le descrizioni seguenti per la struttura PNRPINFO.</span><span class="sxs-lookup"><span data-stu-id="42927-150">For more information, see the following descriptions for the PNRPINFO Structure.</span></span>

</dd> </dl>

<span data-ttu-id="42927-151">Struttura PNRPINFO</span><span class="sxs-lookup"><span data-stu-id="42927-151">PNRPINFO Structure</span></span>

<span data-ttu-id="42927-152">Se il membro **lpBlob** della struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) è impostato, è necessario impostare i membri seguenti della struttura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) :</span><span class="sxs-lookup"><span data-stu-id="42927-152">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="42927-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="42927-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="42927-154">Specifica le dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="42927-154">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="42927-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span><span class="sxs-lookup"><span data-stu-id="42927-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="42927-156">Riservato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-156">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span><span class="sxs-lookup"><span data-stu-id="42927-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="42927-158">Specifica il numero richiesto di risoluzioni.</span><span class="sxs-lookup"><span data-stu-id="42927-158">Specifies the requested number of resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="42927-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span><span class="sxs-lookup"><span data-stu-id="42927-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="42927-160">Specifica il periodo di timeout richiesto per l'attesa delle risposte.</span><span class="sxs-lookup"><span data-stu-id="42927-160">Specifies the requested timeout period to wait for responses.</span></span> <span data-ttu-id="42927-161">Il valore predefinito è 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="42927-161">The default is 30 seconds.</span></span> <span data-ttu-id="42927-162">Il valore massimo è 600 secondi (10 minuti).</span><span class="sxs-lookup"><span data-stu-id="42927-162">The maximum is 600 seconds (10 minutes).</span></span>

</dd> <dt>

<span data-ttu-id="42927-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span><span class="sxs-lookup"><span data-stu-id="42927-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="42927-164">Riservato, deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="42927-164">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="42927-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span><span class="sxs-lookup"><span data-stu-id="42927-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="42927-166">Deve essere uno dei valori consentiti.</span><span class="sxs-lookup"><span data-stu-id="42927-166">Must be one of the allowed values.</span></span> <span data-ttu-id="42927-167">Il valore predefinito è il **\_ \_ \_ \_ \_ \_ \_ nome peer del processo non corrente dei criteri di risoluzione PNRP**.</span><span class="sxs-lookup"><span data-stu-id="42927-167">The default is **PNRP\_RESOLVE\_CRITERIA\_NON\_CURRENT\_PROCESS\_PEER\_NAME**.</span></span> <span data-ttu-id="42927-168">I valori validi sono specificati [**dai \_ \_ criteri di risoluzione PNRP**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).</span><span class="sxs-lookup"><span data-stu-id="42927-168">Valid values are specified by [**PNRP\_RESOLVE\_CRITERIA**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).</span></span>

</dd> <dt>

<span data-ttu-id="42927-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="42927-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="42927-170">Deve essere zero (0) o un **\_ hint PNRPINFO**.</span><span class="sxs-lookup"><span data-stu-id="42927-170">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="42927-171">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="42927-171">The default is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="42927-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**selvat**</span><span class="sxs-lookup"><span data-stu-id="42927-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="42927-173">Specifica l'indirizzo IP per l'hint.</span><span class="sxs-lookup"><span data-stu-id="42927-173">Specifies the IP address for the hint.</span></span> <span data-ttu-id="42927-174">L'hint viene utilizzato quando si tenta di trovare il nome peer più vicino.</span><span class="sxs-lookup"><span data-stu-id="42927-174">The hint is used when attempting to find the nearest peer name.</span></span> <span data-ttu-id="42927-175">Il formato dell'hint è un indirizzo IPv6.</span><span class="sxs-lookup"><span data-stu-id="42927-175">The format of the hint is an IPv6 address.</span></span> <span data-ttu-id="42927-176">Se non si specifica il nome del peer più vicino **, viene invece** utilizzato un indirizzo IPv6 del computer locale.</span><span class="sxs-lookup"><span data-stu-id="42927-176">If **saHint** is not specified when finding the closest peer name, then an IPv6 address of the local computer is used instead.</span></span> <span data-ttu-id="42927-177">Questo membro viene ignorato se **dwFlags** non è impostato.</span><span class="sxs-lookup"><span data-stu-id="42927-177">This member is ignored if **dwFlags** is not set.</span></span>

</dd> <dt>

<span data-ttu-id="42927-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span><span class="sxs-lookup"><span data-stu-id="42927-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="42927-179">Riservato, deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="42927-179">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="42927-180">dwControlFlags</span><span class="sxs-lookup"><span data-stu-id="42927-180">dwControlFlags</span></span>

<span data-ttu-id="42927-181">I \_ flag restituiti LUP seguenti \_ \* sono supportati da PNRP:</span><span class="sxs-lookup"><span data-stu-id="42927-181">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="42927-182">Valore</span><span class="sxs-lookup"><span data-stu-id="42927-182">Value</span></span>                | <span data-ttu-id="42927-183">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42927-183">Description</span></span>                                |
|----------------------|--------------------------------------------|
| <span data-ttu-id="42927-184">\_nome restituito \_ LUP</span><span class="sxs-lookup"><span data-stu-id="42927-184">LUP\_RETURN\_NAME</span></span>    | <span data-ttu-id="42927-185">Restituisce un nome e un contesto.</span><span class="sxs-lookup"><span data-stu-id="42927-185">Returns a name and context.</span></span>                |
| <span data-ttu-id="42927-186">LUP \_ \_ Commento restituito</span><span class="sxs-lookup"><span data-stu-id="42927-186">LUP\_RETURN\_COMMENT</span></span> | <span data-ttu-id="42927-187">Restituisce un commento associato a un nome.</span><span class="sxs-lookup"><span data-stu-id="42927-187">Returns a comment associated with a name.</span></span>  |
| <span data-ttu-id="42927-188">LUP \_ restituire \_ addr</span><span class="sxs-lookup"><span data-stu-id="42927-188">LUP\_RETURN\_ADDR</span></span>    | <span data-ttu-id="42927-189">Restituisce un indirizzo associato a un nome.</span><span class="sxs-lookup"><span data-stu-id="42927-189">Returns an address associated with a name.</span></span> |



 

## <a name="enumerating-network-clouds"></a><span data-ttu-id="42927-190">Enumerazione dei cloud di rete</span><span class="sxs-lookup"><span data-stu-id="42927-190">Enumerating Network Clouds</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="42927-191">lpqsRestrictions</span><span class="sxs-lookup"><span data-stu-id="42927-191">lpqsRestrictions</span></span>

<span data-ttu-id="42927-192">Quando si enumerano i cloud, la struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a cui fa riferimento il parametro *lpqsRestrictions* deve contenere i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="42927-192">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="42927-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="42927-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="42927-194">Specifica le dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="42927-194">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="42927-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="42927-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="42927-196">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-196">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="42927-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="42927-198">Deve essere **SVCID \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="42927-198">Must be **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="42927-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="42927-200">Riservato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-200">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="42927-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="42927-202">Riservato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-202">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="42927-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="42927-204">Deve essere **NS \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="42927-204">Must be **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="42927-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="42927-206">Deve essere PNRPCLOUD o **null** del **\_ provider \_ NS** .</span><span class="sxs-lookup"><span data-stu-id="42927-206">Must be either **NS\_PROVIDER\_PNRPCLOUD** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="42927-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="42927-208">Riservato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-208">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="42927-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="42927-210">Riservato, deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="42927-210">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="42927-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="42927-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="42927-212">Riservato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-212">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="42927-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="42927-214">Riservato, deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="42927-214">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="42927-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="42927-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="42927-216">Riservato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="42927-216">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42927-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="42927-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="42927-218">Riservato, deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="42927-218">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="42927-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="42927-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="42927-220">Puntatore a una struttura [**BLOB**](winsock-nsp-reference-links.md) che punta a una struttura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) .</span><span class="sxs-lookup"><span data-stu-id="42927-220">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure.</span></span> <span data-ttu-id="42927-221">Se **lpBlob** è **null**, vengono enumerati tutti i cloud.</span><span class="sxs-lookup"><span data-stu-id="42927-221">If **lpBlob** is **NULL**, all clouds are enumerated.</span></span>

</dd> </dl>

<span data-ttu-id="42927-222">Struttura PNRPCLOUDINFO</span><span class="sxs-lookup"><span data-stu-id="42927-222">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="42927-223">Quando si enumerano i cloud, è necessario impostare i seguenti membri della struttura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) :</span><span class="sxs-lookup"><span data-stu-id="42927-223">When enumerating clouds, the following members of the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="42927-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="42927-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="42927-225">Specifica le dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="42927-225">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="42927-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span><span class="sxs-lookup"><span data-stu-id="42927-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="42927-227">Punta a una struttura che specifica i criteri che è possibile usare per filtrare i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="42927-227">Points to a structure that specifies criteria that you can use to filter search results.</span></span> <span data-ttu-id="42927-228">Il membro **cloud. Scope** può essere **un ambito PNRP \_ \_ qualsiasi**, **\_ \_ ambito globale PNRP**, **\_ \_ \_ ambito locale del sito PNRP** o **\_ \_ \_ ambito locale collegamento PNRP**.</span><span class="sxs-lookup"><span data-stu-id="42927-228">The **Cloud.Scope** member can be **PNRP\_SCOPE\_ANY**, **PNRP\_GLOBAL\_SCOPE**, **PNRP\_SITE\_LOCAL\_SCOPE**, or **PNRP\_LINK\_LOCAL\_SCOPE**.</span></span> <span data-ttu-id="42927-229">Se viene specificato **\_ \_ un ambito PNRP** , vengono restituiti tutti i cloud.</span><span class="sxs-lookup"><span data-stu-id="42927-229">If **PNRP\_SCOPE\_ANY** is specified, all clouds are returned.</span></span> <span data-ttu-id="42927-230">In caso contrario, vengono restituiti solo i cloud che corrispondono al **cloud. Scope** .</span><span class="sxs-lookup"><span data-stu-id="42927-230">Otherwise, only clouds that match the **Cloud.Scope** are returned.</span></span>

</dd> <dt>

<span data-ttu-id="42927-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span><span class="sxs-lookup"><span data-stu-id="42927-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="42927-232">Riservato, deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="42927-232">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="42927-233">dwControlFlags</span><span class="sxs-lookup"><span data-stu-id="42927-233">dwControlFlags</span></span>

<span data-ttu-id="42927-234">I \_ flag restituiti LUP seguenti \_ \* sono supportati da PNRP:</span><span class="sxs-lookup"><span data-stu-id="42927-234">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="42927-235">Valore</span><span class="sxs-lookup"><span data-stu-id="42927-235">Value</span></span>             | <span data-ttu-id="42927-236">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42927-236">Description</span></span>                                                       |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="42927-237">\_nome restituito \_ LUP</span><span class="sxs-lookup"><span data-stu-id="42927-237">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="42927-238">Restituisce un nome e un contesto.</span><span class="sxs-lookup"><span data-stu-id="42927-238">Returns a name and context.</span></span>                                       |
| <span data-ttu-id="42927-239">\_BLOB restituito \_ LUP</span><span class="sxs-lookup"><span data-stu-id="42927-239">LUP\_RETURN\_BLOB</span></span> | <span data-ttu-id="42927-240">Restituisce il [BLOB](pnrp-and-blob.md) associato a questo cloud.</span><span class="sxs-lookup"><span data-stu-id="42927-240">Returns the [BLOB](pnrp-and-blob.md) associated with this cloud.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="42927-241">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="42927-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42927-242">PNRP e BLOB</span><span class="sxs-lookup"><span data-stu-id="42927-242">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="42927-243">PNRP e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="42927-243">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="42927-244">PNRP e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="42927-244">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="42927-245">PNRP e WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="42927-245">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="42927-246">PNRP e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="42927-246">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="42927-247">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="42927-247">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="42927-248">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="42927-248">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="42927-249">Codici di errore PNRP NSP</span><span class="sxs-lookup"><span data-stu-id="42927-249">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 



