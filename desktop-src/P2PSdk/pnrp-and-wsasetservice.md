---
description: PNRP usa la funzione WSASetService per registrare o rimuovere i nomi dei peer.
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP e WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a04251a8b038c5895ae5dfafd65be9263edfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312230"
---
# <a name="pnrp-and-wsasetservice"></a><span data-ttu-id="33328-103">PNRP e WSASetService</span><span class="sxs-lookup"><span data-stu-id="33328-103">PNRP and WSASetService</span></span>

<span data-ttu-id="33328-104">PNRP usa la funzione [**WSASetService**](winsock-nsp-reference-links.md) per registrare o rimuovere [i nomi dei peer](peer-names.md).</span><span class="sxs-lookup"><span data-stu-id="33328-104">PNRP uses the [**WSASetService**](winsock-nsp-reference-links.md) function to register or remove [peer names](peer-names.md).</span></span>

## <a name="registering-a-name"></a><span data-ttu-id="33328-105">Registrazione di un nome</span><span class="sxs-lookup"><span data-stu-id="33328-105">Registering a Name</span></span>

<span data-ttu-id="33328-106">La registrazione include un nome peer e un set di endpoint in cui è possibile contattare un servizio.</span><span class="sxs-lookup"><span data-stu-id="33328-106">Registration includes a peer name and set of endpoints where a service can be contacted.</span></span> <span data-ttu-id="33328-107">Una registrazione è specifica di un Cloud PNRP.</span><span class="sxs-lookup"><span data-stu-id="33328-107">A registration is specific to a PNRP cloud.</span></span> <span data-ttu-id="33328-108">Dopo la registrazione di un peer, si verifica un ritardo tra la registrazione e la propagazione delle informazioni di registrazione ad altri nodi.</span><span class="sxs-lookup"><span data-stu-id="33328-108">After a peer is registered, there is a delay between the registration and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="33328-109">Durante questo periodo, gli altri nodi potrebbero non essere in grado di risolvere un peer appena registrato.</span><span class="sxs-lookup"><span data-stu-id="33328-109">During this time, other nodes may not be able to resolve a newly registered peer.</span></span>

<span data-ttu-id="33328-110">La registrazione del servizio non è persistente.</span><span class="sxs-lookup"><span data-stu-id="33328-110">Service registration is not persistent.</span></span>

-   <span data-ttu-id="33328-111">Se un processo client che registra un nome peer viene chiuso o chiama [**WSACleanup**](winsock-nsp-reference-links.md), viene annullata la registrazione del nome peer.</span><span class="sxs-lookup"><span data-stu-id="33328-111">If a client process that registers a peer name exits or calls [**WSACleanup**](winsock-nsp-reference-links.md), then the peer name is unregistered.</span></span>
-   <span data-ttu-id="33328-112">Se un nome peer specificato è già registrato nello stesso cloud dal processo corrente, viene sostituito con i nuovi valori di registrazione.</span><span class="sxs-lookup"><span data-stu-id="33328-112">If a specified peer name is already registered in the same cloud by the current process, it is replaced with new registration values.</span></span>

<span data-ttu-id="33328-113">Quando si registra un nome peer, è necessario indicare i valori di parametro seguenti:</span><span class="sxs-lookup"><span data-stu-id="33328-113">When registering a peer name, the following parameter values must be indicated:</span></span>

-   <span data-ttu-id="33328-114">il valore del parametro *essOperation* deve essere **RNRSERVICE \_ Register**.</span><span class="sxs-lookup"><span data-stu-id="33328-114">*essOperation* parameter must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="33328-115">il parametro *dwControlFlags* deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="33328-115">*dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="33328-116">Quando si registra un nome peer, la struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a cui fa riferimento il parametro *lpqsRegInfo* deve contenere i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="33328-116">When registering a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure referenced by the *lpqsRegInfo* parameter must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="33328-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="33328-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="33328-118">Specifica le dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="33328-118">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="33328-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="33328-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="33328-120">Specifica un nome peer da registrare.</span><span class="sxs-lookup"><span data-stu-id="33328-120">Specifies a peer name to register.</span></span> <span data-ttu-id="33328-121">Se il [nome peer](peer-names.md) non è protetto, l'identità è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="33328-121">If the [peer name](peer-names.md) is unsecured, then the identity is optional.</span></span> <span data-ttu-id="33328-122">Se l'identità viene specificata come **null**, PNRP usa l'identità locale del computer, per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="33328-122">If the identity is specified as **NULL**, PNRP uses the machine local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="33328-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="33328-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="33328-124">Deve essere SVCID \_ pnrpname.</span><span class="sxs-lookup"><span data-stu-id="33328-124">Must be SVCID\_PNRPNAME.</span></span>

</dd> <dt>

<span data-ttu-id="33328-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="33328-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="33328-126">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-126">Ignored.</span></span> <span data-ttu-id="33328-127">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="33328-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="33328-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="33328-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="33328-129">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-129">Ignored.</span></span> <span data-ttu-id="33328-130">Tuttavia, la stringa deve essere ancora inferiore a 40 caratteri, incluso il terminatore **null** .</span><span class="sxs-lookup"><span data-stu-id="33328-130">However, the string is still required to be fewer than 40 characters, including the **NULL** terminator.</span></span>

</dd> <dt>

<span data-ttu-id="33328-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="33328-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="33328-132">Deve essere **NS \_ pnrpname** o **NS \_ All**.</span><span class="sxs-lookup"><span data-stu-id="33328-132">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="33328-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="33328-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="33328-134">Deve essere il **\_ provider NS \_ pnrpname** o **null**.</span><span class="sxs-lookup"><span data-stu-id="33328-134">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="33328-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="33328-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="33328-136">Deve essere un nome di cloud, una stringa vuota o **null**.</span><span class="sxs-lookup"><span data-stu-id="33328-136">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="33328-137">Se questo valore è **null** o una stringa vuota, viene utilizzato il cloud predefinito, ovvero "Global".</span><span class="sxs-lookup"><span data-stu-id="33328-137">If this value is **NULL** or an empty string, the default cloud, "Global", is used.</span></span> <span data-ttu-id="33328-138">In caso contrario, deve puntare a un nome di cloud valido.</span><span class="sxs-lookup"><span data-stu-id="33328-138">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="33328-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="33328-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="33328-140">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-140">Ignored.</span></span> <span data-ttu-id="33328-141">Impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="33328-141">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="33328-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="33328-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="33328-143">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-143">Ignored.</span></span> <span data-ttu-id="33328-144">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="33328-144">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="33328-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="33328-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="33328-146">Specifica il numero di indirizzi registrati da un servizio.</span><span class="sxs-lookup"><span data-stu-id="33328-146">Specifies the number of addresses registered by a service.</span></span> <span data-ttu-id="33328-147">Il numero massimo di indirizzi che è possibile registrare per un singolo nome è 10.</span><span class="sxs-lookup"><span data-stu-id="33328-147">The maximum number of addresses that can be registered for a single name is 10.</span></span>

</dd> <dt>

<span data-ttu-id="33328-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="33328-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="33328-149">Puntatore a un elenco di indirizzi da registrare.</span><span class="sxs-lookup"><span data-stu-id="33328-149">Pointer to a list of addresses to register.</span></span>

</dd> <dt>

<span data-ttu-id="33328-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="33328-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="33328-151">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-151">Ignored.</span></span> <span data-ttu-id="33328-152">Impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="33328-152">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="33328-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="33328-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="33328-154">Puntatore a una struttura [**BLOB**](winsock-nsp-reference-links.md) che punta a una struttura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="33328-154">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="33328-155">È necessario impostare parametri specifici nella struttura **PNRPINFO** .</span><span class="sxs-lookup"><span data-stu-id="33328-155">Specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="33328-156">Per ulteriori informazioni, vedere la sezione struttura **PNRPINFO** seguente.</span><span class="sxs-lookup"><span data-stu-id="33328-156">For more information, see the following **PNRPINFO** structure section.</span></span>

</dd> </dl>

## <a name="pnrpinfo-structure"></a><span data-ttu-id="33328-157">Struttura PNRPINFO</span><span class="sxs-lookup"><span data-stu-id="33328-157">PNRPINFO Structure</span></span>

<span data-ttu-id="33328-158">Se il membro **lpBlob** della struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) è impostato, è necessario impostare i membri seguenti della struttura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) :</span><span class="sxs-lookup"><span data-stu-id="33328-158">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="33328-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="33328-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="33328-160">Specifica le dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="33328-160">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="33328-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span><span class="sxs-lookup"><span data-stu-id="33328-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="33328-162">Specifica l'identità del nome peer creato tramite [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span><span class="sxs-lookup"><span data-stu-id="33328-162">Specifies the identity of the peer name that is created by using [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span> <span data-ttu-id="33328-163">Se un nome peer non è protetto, l'identità è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="33328-163">If a peer name is unsecured, then the identity is optional.</span></span> <span data-ttu-id="33328-164">Se l'identità viene specificata come **null**, PNRP utilizza l'identità locale del computer, per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="33328-164">If the identity is specified as **NULL**, PNRP uses the computer local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="33328-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span><span class="sxs-lookup"><span data-stu-id="33328-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="33328-166">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-166">Ignored.</span></span> <span data-ttu-id="33328-167">Impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="33328-167">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="33328-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span><span class="sxs-lookup"><span data-stu-id="33328-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="33328-169">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-169">Ignored.</span></span> <span data-ttu-id="33328-170">Impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="33328-170">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="33328-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span><span class="sxs-lookup"><span data-stu-id="33328-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="33328-172">Specifica il numero di secondi tra le operazioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="33328-172">Specifies the number of seconds between refresh operations.</span></span>

</dd> <dt>

<span data-ttu-id="33328-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span><span class="sxs-lookup"><span data-stu-id="33328-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="33328-174">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-174">Ignored.</span></span> <span data-ttu-id="33328-175">Impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="33328-175">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="33328-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="33328-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="33328-177">Deve essere zero (0) o un **\_ hint PNRPINFO**.</span><span class="sxs-lookup"><span data-stu-id="33328-177">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="33328-178">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="33328-178">The default is zero (0).</span></span> <span data-ttu-id="33328-179">Ciò significa che la parte relativa alla posizione del servizio dell'ID PNRP viene compilata usando l'indirizzo IP in **selvat**.</span><span class="sxs-lookup"><span data-stu-id="33328-179">This means that the service location portion of the PNRP ID is built by using the IP address in **saHint**.</span></span> <span data-ttu-id="33328-180">In caso contrario, la posizione del servizio viene compilata utilizzando il primo indirizzo IP nella prima voce IPv6 del membro **lpcsaBuffer** .</span><span class="sxs-lookup"><span data-stu-id="33328-180">Otherwise, the service location is built by using the first IP address in the first IPv6 entry of the **lpcsaBuffer** member.</span></span>

</dd> <dt>

<span data-ttu-id="33328-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**selvat**</span><span class="sxs-lookup"><span data-stu-id="33328-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="33328-182">Specifica l'indirizzo IPv6 per l'hint.</span><span class="sxs-lookup"><span data-stu-id="33328-182">Specifies the IPv6 address for the hint.</span></span>

</dd> <dt>

<span data-ttu-id="33328-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span><span class="sxs-lookup"><span data-stu-id="33328-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="33328-184">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-184">Ignored.</span></span> <span data-ttu-id="33328-185">Impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="33328-185">Set to zero (0).</span></span>

</dd> </dl>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="33328-186">Annullamento della registrazione di un nome peer</span><span class="sxs-lookup"><span data-stu-id="33328-186">Unregistering a Peer Name</span></span>

<span data-ttu-id="33328-187">Nell'elenco seguente vengono identificate le informazioni importanti sull'annullamento della registrazione di un nome peer.</span><span class="sxs-lookup"><span data-stu-id="33328-187">The following list identifies the important information about unregistering a peer name.</span></span>

-   <span data-ttu-id="33328-188">Solo un'applicazione che registra un nome peer può annullarne la registrazione.</span><span class="sxs-lookup"><span data-stu-id="33328-188">Only an application that registers a peer name can unregister it.</span></span>
-   <span data-ttu-id="33328-189">Se viene chiamato [**WSACleanup**](winsock-nsp-reference-links.md) , viene annullata la registrazione automatica di un nome peer.</span><span class="sxs-lookup"><span data-stu-id="33328-189">A peer name is unregistered automatically if [**WSACleanup**](winsock-nsp-reference-links.md) is called.</span></span>
-   <span data-ttu-id="33328-190">PNRP rimuove sempre l'intera registrazione del nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="33328-190">PNRP always removes the entire service name registration.</span></span> <span data-ttu-id="33328-191">Non consente la rimozione di singoli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="33328-191">It does not allow removal of individual addresses.</span></span>
-   <span data-ttu-id="33328-192">Quando si annulla la registrazione di un nome, il parametro *essOperation* deve avere il valore **RNRSERVICE \_ Delete**.</span><span class="sxs-lookup"><span data-stu-id="33328-192">When unregistering a name, the *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="33328-193">PNRP non supporta il valore **RNRSERVICE \_ deregister**.</span><span class="sxs-lookup"><span data-stu-id="33328-193">PNRP does not support the value **RNRSERVICE\_DEREGISTER**.</span></span>
-   <span data-ttu-id="33328-194">Il parametro *dwControlFlags* deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="33328-194">The *dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="33328-195">Quando si annulla la registrazione di un nome, la struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a cui fa riferimento il parametro *lpqsRegInfo* deve contenere i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="33328-195">When unregistering a name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRegInfo* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="33328-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="33328-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="33328-197">Specifica le dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="33328-197">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="33328-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="33328-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="33328-199">Specifica un nome peer di cui annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="33328-199">Specifies a peer name to unregister.</span></span>

</dd> <dt>

<span data-ttu-id="33328-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="33328-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="33328-201">Deve essere **SVCID \_ pnrpname**.</span><span class="sxs-lookup"><span data-stu-id="33328-201">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="33328-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="33328-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="33328-203">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-203">Ignored.</span></span> <span data-ttu-id="33328-204">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="33328-204">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="33328-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="33328-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="33328-206">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-206">Ignored.</span></span> <span data-ttu-id="33328-207">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="33328-207">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="33328-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="33328-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="33328-209">Deve essere **NS \_ pnrpname** o **NS \_ All**.</span><span class="sxs-lookup"><span data-stu-id="33328-209">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="33328-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="33328-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="33328-211">Deve essere il **\_ provider NS \_ pnrpname** o **null**.</span><span class="sxs-lookup"><span data-stu-id="33328-211">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="33328-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="33328-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="33328-213">Deve essere un nome di cloud, una stringa vuota o **null**.</span><span class="sxs-lookup"><span data-stu-id="33328-213">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="33328-214">Se questo valore è **null** o una stringa vuota, viene utilizzato il cloud predefinito, ovvero "Global".</span><span class="sxs-lookup"><span data-stu-id="33328-214">If this value is **NULL** or an empty string, the default cloud, "Global" is used.</span></span> <span data-ttu-id="33328-215">In caso contrario, deve puntare a un nome di cloud valido.</span><span class="sxs-lookup"><span data-stu-id="33328-215">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="33328-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="33328-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="33328-217">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-217">Ignored.</span></span> <span data-ttu-id="33328-218">Impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="33328-218">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="33328-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="33328-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="33328-220">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-220">Ignored.</span></span> <span data-ttu-id="33328-221">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="33328-221">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="33328-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="33328-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="33328-223">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-223">Ignored.</span></span> <span data-ttu-id="33328-224">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="33328-224">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="33328-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="33328-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="33328-226">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-226">Ignored.</span></span> <span data-ttu-id="33328-227">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="33328-227">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="33328-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="33328-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="33328-229">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="33328-229">Ignored.</span></span> <span data-ttu-id="33328-230">Impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="33328-230">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="33328-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="33328-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="33328-232">Puntatore a una struttura [**BLOB**](winsock-nsp-reference-links.md) che punta a una struttura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="33328-232">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="33328-233">Il membro **lpszIdentity** della struttura **lpBlob** identifica il nome dell'identità utilizzata per registrare un nome peer.</span><span class="sxs-lookup"><span data-stu-id="33328-233">The **lpszIdentity** member of the **lpBlob** structure identifies the name of the identity that is used to register a peer name.</span></span> <span data-ttu-id="33328-234">I membri rimanenti devono essere impostati sugli stessi valori utilizzati per la registrazione di un nome.</span><span class="sxs-lookup"><span data-stu-id="33328-234">The remaining members must be set to the same values that are used when registering a name.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="33328-235">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33328-235">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33328-236">PNRP e BLOB</span><span class="sxs-lookup"><span data-stu-id="33328-236">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="33328-237">PNRP e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="33328-237">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="33328-238">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="33328-238">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="33328-239">Codici di errore PNRP NSP</span><span class="sxs-lookup"><span data-stu-id="33328-239">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="33328-240">**WSACleanup**</span><span class="sxs-lookup"><span data-stu-id="33328-240">**WSACleanup**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="33328-241">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="33328-241">**WSASetService**</span></span>
</dt> </dl>

 

 



