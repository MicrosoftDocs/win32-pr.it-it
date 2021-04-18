---
description: PNRP utilizza la funzione WSALookupServiceNext per trovare la corrispondenza con le query specificate in una precedente chiamata a WSALookupServiceBegin.
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP e WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398beca2f16e4920ab7fbe43bb648cbc22d9f336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312237"
---
# <a name="pnrp-and-wsalookupservicenext"></a><span data-ttu-id="189e6-103">PNRP e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="189e6-103">PNRP and WSALookupServiceNext</span></span>

<span data-ttu-id="189e6-104">PNRP utilizza la funzione [**WSALookupServiceNext**](winsock-nsp-reference-links.md) per trovare la corrispondenza con le query specificate in una precedente chiamata a **WSALookupServiceBegin**.</span><span class="sxs-lookup"><span data-stu-id="189e6-104">PNRP uses the [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function to match queries specified in a previous call to **WSALookupServiceBegin**.</span></span> <span data-ttu-id="189e6-105">I risultati della funzione **WSALookupServiceNext** sono determinati dalle impostazioni nella struttura **WSAQUERYSET** passata nella chiamata di funzione **WSALookupServiceBegin** iniziale.</span><span class="sxs-lookup"><span data-stu-id="189e6-105">The results of the **WSALookupServiceNext** function are determined by settings in the **WSAQUERYSET** structure passed in the initial **WSALookupServiceBegin** function call.</span></span> <span data-ttu-id="189e6-106">Questa funzione viene utilizzata per eseguire le due funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="189e6-106">This function is used to perform the following two functions:</span></span>

-   <span data-ttu-id="189e6-107">Risoluzione di un nome peer in un elenco di indirizzi</span><span class="sxs-lookup"><span data-stu-id="189e6-107">Resolving a peer name to a list of addresses</span></span>
-   <span data-ttu-id="189e6-108">Enumerazione dei cloud di rete</span><span class="sxs-lookup"><span data-stu-id="189e6-108">Enumerating network clouds</span></span>

<span data-ttu-id="189e6-109">Utilizzando [**WSANSPIoctl**](winsock-nsp-reference-links.md), il servizio di ricerca può essere utilizzato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="189e6-109">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="189e6-110">Per informazioni sull'uso asincrono delle funzioni del servizio di ricerca, vedere [PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md).</span><span class="sxs-lookup"><span data-stu-id="189e6-110">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="189e6-111">La funzione [**WSALookupServiceNext**](winsock-nsp-reference-links.md) si blocca anche se viene chiamato **WSANSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="189e6-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="189e6-112">Prima di chiamare **WSALookupServiceNext**, un'applicazione deve attendere fino a quando non riceve una notifica, se il blocco è un problema.</span><span class="sxs-lookup"><span data-stu-id="189e6-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a><span data-ttu-id="189e6-113">Risoluzione di un nome peer in un elenco di indirizzi</span><span class="sxs-lookup"><span data-stu-id="189e6-113">Resolving a Peer Name to a List of Addresses</span></span>

<span data-ttu-id="189e6-114">Quando si risolve un nome peer in un elenco di indirizzi, la struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) restituita nel parametro *lpqsResults* contiene i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="189e6-114">When resolving a peer name to a list of addresses, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="189e6-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="189e6-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-116">Restituisce la dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="189e6-116">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="189e6-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-118">Restituisce un nome peer: se **LUP restituisce il \_ \_ nome**, **LUP \_ restituisce \_ All** o **null** sono specificati.</span><span class="sxs-lookup"><span data-stu-id="189e6-118">Returns a peer name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="189e6-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-120">Restituisce **SVCID \_ pnrpname**.</span><span class="sxs-lookup"><span data-stu-id="189e6-120">Returns **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="189e6-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-122">Restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="189e6-122">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="189e6-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-124">Restituisce un commento, se **LUP \_ restituisce \_ Comment**, **LUP \_ restituisce \_ All** o **null** .</span><span class="sxs-lookup"><span data-stu-id="189e6-124">Returns a comment—if **LUP\_RETURN\_COMMENT**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="189e6-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-126">Restituisce **NS \_ pnrpname**.</span><span class="sxs-lookup"><span data-stu-id="189e6-126">Returns **NS\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="189e6-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-128">Restituisce **il \_ provider NS \_ pnrpname**.</span><span class="sxs-lookup"><span data-stu-id="189e6-128">Returns **NS\_PROVIDER\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="189e6-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-130">Restituisce il nome del cloud se viene specificato il **\_ \_ nome restituito LUP**, **LUP \_ return \_ All** o **null** .</span><span class="sxs-lookup"><span data-stu-id="189e6-130">Returns the cloud name if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="189e6-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-132">Restituisce zero (0).</span><span class="sxs-lookup"><span data-stu-id="189e6-132">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="189e6-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="189e6-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-134">Restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="189e6-134">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="189e6-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-136">Restituisce il numero di voci nella matrice di \_ informazioni CSADDR se **LUP \_ restituisce \_ addr**, **LUP \_ restituisce \_ All** o **null** .</span><span class="sxs-lookup"><span data-stu-id="189e6-136">Returns the number of entries in the CSADDR\_INFO array if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="189e6-137">Questo valore e le informazioni in **lpcsaBuffer** sono i bit chiave delle informazioni restituite nella struttura.</span><span class="sxs-lookup"><span data-stu-id="189e6-137">This value and the information in **lpcsaBuffer** are the key bits of information returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="189e6-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-139">Restituisce un puntatore a una matrice di \_ strutture di informazioni CSADDR se **LUP \_ restituisce \_ addr**, **LUP \_ restituisce \_ All** o **null** .</span><span class="sxs-lookup"><span data-stu-id="189e6-139">Returns a pointer to an array of CSADDR\_INFO structures if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="189e6-140">Questo buffer e il valore in **dwNumberOfCsAddrs** sono i bit di informazioni chiave restituiti in questa struttura.</span><span class="sxs-lookup"><span data-stu-id="189e6-140">This buffer and the value in **dwNumberOfCsAddrs** are the key information bits returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="189e6-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-142">Restituisce zero (0).</span><span class="sxs-lookup"><span data-stu-id="189e6-142">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="189e6-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="189e6-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-144">Restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="189e6-144">Returns **NULL**.</span></span>

</dd> </dl>

## <a name="enumerating-network-clouds"></a><span data-ttu-id="189e6-145">Enumerazione dei cloud di rete</span><span class="sxs-lookup"><span data-stu-id="189e6-145">Enumerating Network Clouds</span></span>

<span data-ttu-id="189e6-146">Quando si enumerano i cloud, la struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) restituita nel parametro *lpqsResults* contiene i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="189e6-146">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="189e6-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="189e6-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-148">Restituisce la dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="189e6-148">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="189e6-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-150">Restituisce un nome cloud: se **LUP restituisce il \_ \_ nome**, **LUP \_ restituisce \_ All** o **null** sono specificati.</span><span class="sxs-lookup"><span data-stu-id="189e6-150">Returns a cloud name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="189e6-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-152">Restituisce **SVCID \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="189e6-152">Returns **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="189e6-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-154">Restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="189e6-154">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="189e6-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-156">Restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="189e6-156">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="189e6-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-158">Restituisce **NS \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="189e6-158">Returns **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="189e6-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-160">Restituisce **\_ \_ PNRPCLOUD del provider NS**.</span><span class="sxs-lookup"><span data-stu-id="189e6-160">Returns **NS\_PROVIDER\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="189e6-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-162">Restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="189e6-162">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="189e6-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-164">Restituisce zero (0).</span><span class="sxs-lookup"><span data-stu-id="189e6-164">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="189e6-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="189e6-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-166">Restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="189e6-166">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="189e6-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-168">Restituisce zero (0).</span><span class="sxs-lookup"><span data-stu-id="189e6-168">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="189e6-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="189e6-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-170">Restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="189e6-170">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="189e6-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-172">Restituisce zero (0).</span><span class="sxs-lookup"><span data-stu-id="189e6-172">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="189e6-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="189e6-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-174">Restituisce un puntatore a una struttura [**BLOB**](winsock-nsp-reference-links.md) che punta a una struttura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) , se **LUP \_ restituisce \_ BLOB**, **LUP \_ restituisce \_ All** o **null** .</span><span class="sxs-lookup"><span data-stu-id="189e6-174">Returns a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure—if **LUP\_RETURN\_BLOB**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a><span data-ttu-id="189e6-175">Struttura PNRPCLOUDINFO</span><span class="sxs-lookup"><span data-stu-id="189e6-175">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="189e6-176">Quando si enumerano i nomi cloud, nella struttura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) vengono restituiti i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="189e6-176">When enumerating cloud names, the following values are returned in the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure:</span></span>

<dl> <dt>

<span data-ttu-id="189e6-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="189e6-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-178">Dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="189e6-178">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span><span class="sxs-lookup"><span data-stu-id="189e6-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-180">Valore effettivo del cloud.</span><span class="sxs-lookup"><span data-stu-id="189e6-180">The actual cloud value.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span><span class="sxs-lookup"><span data-stu-id="189e6-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-182">Stato corrente di un cloud.</span><span class="sxs-lookup"><span data-stu-id="189e6-182">The current state of a cloud.</span></span> <span data-ttu-id="189e6-183">[**PNRP \_ \_Stato cloud**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) specifica i valori validi.</span><span class="sxs-lookup"><span data-stu-id="189e6-183">[**PNRP\_CLOUD\_STATE**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) specifies the valid values.</span></span>

</dd> <dt>

<span data-ttu-id="189e6-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**</span><span class="sxs-lookup"><span data-stu-id="189e6-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**</span></span>
</dt> <dd>

<span data-ttu-id="189e6-185">Indica che un nome cloud è valido in una rete o è valido solo in un computer corrente.</span><span class="sxs-lookup"><span data-stu-id="189e6-185">Indicates that a cloud name is valid on a network, or only valid on a current computer.</span></span> <span data-ttu-id="189e6-186">[**PNRP \_ \_Flag cloud**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) specifica i valori validi.</span><span class="sxs-lookup"><span data-stu-id="189e6-186">[**PNRP\_CLOUD\_FLAGS**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) specifies the valid values.</span></span> <span data-ttu-id="189e6-187">Alcuni nomi cloud sono validi in tutti i computer della stessa rete.</span><span class="sxs-lookup"><span data-stu-id="189e6-187">Some cloud names are valid on any computer on the same network.</span></span> <span data-ttu-id="189e6-188">Altri nomi di cloud sono validi solo in un computer corrente e possono essere validi solo per un periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="189e6-188">Other cloud names are valid only on a current computer, and may be valid only for a period of time.</span></span>

-   <span data-ttu-id="189e6-189">Se **enCloudFlags** è impostato sul **\_ nome cloud \_ PNRP \_ locale,** il nome è valido solo localmente.</span><span class="sxs-lookup"><span data-stu-id="189e6-189">If **enCloudFlags** is set to **PNRP\_CLOUD\_NAME\_LOCAL,** the name is only valid locally.</span></span>
-   <span data-ttu-id="189e6-190">Se **enCloudFlags** non è impostato, il nome del cloud può essere trasferito ad altri computer.</span><span class="sxs-lookup"><span data-stu-id="189e6-190">If **enCloudFlags** is not set, then the cloud name can be transferred to other computers.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="189e6-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="189e6-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="189e6-192">PNRP e BLOB</span><span class="sxs-lookup"><span data-stu-id="189e6-192">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="189e6-193">PNRP e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="189e6-193">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="189e6-194">PNRP e WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="189e6-194">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="189e6-195">PNRP e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="189e6-195">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="189e6-196">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="189e6-196">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="189e6-197">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="189e6-197">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="189e6-198">Codici di errore PNRP NSP</span><span class="sxs-lookup"><span data-stu-id="189e6-198">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="189e6-199">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="189e6-199">**WSALookupServiceBegin**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



