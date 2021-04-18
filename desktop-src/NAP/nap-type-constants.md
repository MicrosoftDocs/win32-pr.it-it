---
title: Costanti di tipo NAP (NapTypes. h)
description: Sono definite le costanti NAP seguenti.
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85692a7ccc9cbb602a34da714a5eeb488ea5c4a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302255"
---
# <a name="nap-type-constants"></a><span data-ttu-id="321d3-103">Costanti di tipo NAP</span><span class="sxs-lookup"><span data-stu-id="321d3-103">NAP Type Constants</span></span>

> [!Note]  
> <span data-ttu-id="321d3-104">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="321d3-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="321d3-105">Sono definite le costanti NAP seguenti.</span><span class="sxs-lookup"><span data-stu-id="321d3-105">The following NAP constants are defined.</span></span>

<span data-ttu-id="321d3-106">Le costanti NAP seguenti sono definite in NapTypes. h:</span><span class="sxs-lookup"><span data-stu-id="321d3-106">The following NAP constants are defined in NapTypes.h:</span></span>

<dl> <dt>

<span data-ttu-id="321d3-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**</span><span class="sxs-lookup"><span data-stu-id="321d3-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-108">0x64</span><span class="sxs-lookup"><span data-stu-id="321d3-108">0x64</span></span>
</dt> <dt>



<span data-ttu-id="321d3-109">Numero massimo di oggetti di tipo [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) -Length-Value (TLV) associati a un pacchetto [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="321d3-109">The maximum number of [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) type-length-value (TLV) objects associated with an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**</span><span class="sxs-lookup"><span data-stu-id="321d3-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-111">0xFA0</span><span class="sxs-lookup"><span data-stu-id="321d3-111">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="321d3-112">Dimensione massima, in byte, di un oggetto [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) associato a un pacchetto di rapporto di integrità ([**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh)).</span><span class="sxs-lookup"><span data-stu-id="321d3-112">The maximum size, in bytes, of a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) object associated with a statement of health ([**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**</span><span class="sxs-lookup"><span data-stu-id="321d3-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-114">0xC</span><span class="sxs-lookup"><span data-stu-id="321d3-114">0xC</span></span>
</dt> <dt>



<span data-ttu-id="321d3-115">Dimensioni minime, in byte, di un pacchetto di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="321d3-115">The minimum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**</span><span class="sxs-lookup"><span data-stu-id="321d3-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-117">0xFA0</span><span class="sxs-lookup"><span data-stu-id="321d3-117">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="321d3-118">Dimensione massima, in byte, di un pacchetto di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="321d3-118">The maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="321d3-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-120">maxSoHAttributeSize/sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="321d3-120">maxSoHAttributeSize / sizeof(DWORD)</span></span>
</dt> <dt>



<span data-ttu-id="321d3-121">Numero massimo di valori DWORD associati a un [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="321d3-121">The maximum number of DWORD values associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="321d3-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-123">maxSoHAttributeSize/0x4</span><span class="sxs-lookup"><span data-stu-id="321d3-123">maxSoHAttributeSize / 0x4</span></span>
</dt> <dt>



<span data-ttu-id="321d3-124">Numero massimo di indirizzi IPv4 associati a un [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="321d3-124">The maximum number of IPv4 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="321d3-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-126">maxSoHAttributeSize/0x10</span><span class="sxs-lookup"><span data-stu-id="321d3-126">maxSoHAttributeSize / 0x10</span></span>
</dt> <dt>



<span data-ttu-id="321d3-127">Numero massimo di indirizzi IPv6 associati a un [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="321d3-127">The maximum number of IPv6 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**</span><span class="sxs-lookup"><span data-stu-id="321d3-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-129">0x400</span><span class="sxs-lookup"><span data-stu-id="321d3-129">0x400</span></span>
</dt> <dt>



<span data-ttu-id="321d3-130">Lunghezza massima di una stringa specificata dalla struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="321d3-130">The maximum length of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**</span><span class="sxs-lookup"><span data-stu-id="321d3-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-132">(maxStringLength + 1) \* sizeof (WCHAR)</span><span class="sxs-lookup"><span data-stu-id="321d3-132">(maxStringLength + 1) \* sizeof(WCHAR)</span></span>
</dt> <dt>



<span data-ttu-id="321d3-133">Lunghezza massima, in byte, di una stringa specificata dalla struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="321d3-133">The maximum length, in bytes, of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="321d3-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-135">0x14</span><span class="sxs-lookup"><span data-stu-id="321d3-135">0x14</span></span>
</dt> <dt>



<span data-ttu-id="321d3-136">Numero massimo di entità di integrità del sistema, ad esempio SHV e SHAs.</span><span class="sxs-lookup"><span data-stu-id="321d3-136">The maximum number of system health entities, such as SHVs and SHAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="321d3-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-138">\[intervallo (0, maxSystemHealthEntityCount)\]</span><span class="sxs-lookup"><span data-stu-id="321d3-138">\[range(0, maxSystemHealthEntityCount)\]</span></span> 
</dt> <dt>



<span data-ttu-id="321d3-139">Intervallo di valori possibili per il numero di entità di integrità del sistema.</span><span class="sxs-lookup"><span data-stu-id="321d3-139">The range of possible values for the number of system health entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**</span><span class="sxs-lookup"><span data-stu-id="321d3-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-141">0x14</span><span class="sxs-lookup"><span data-stu-id="321d3-141">0x14</span></span>
</dt> <dt>



<span data-ttu-id="321d3-142">Numero massimo di entità di imposizione, ad esempio QeC.</span><span class="sxs-lookup"><span data-stu-id="321d3-142">The maximum number of enforcement entities, such as QECs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**</span><span class="sxs-lookup"><span data-stu-id="321d3-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-144">\[intervallo (0, maxEnforcerCount)\]</span><span class="sxs-lookup"><span data-stu-id="321d3-144">\[range(0, maxEnforcerCount)\]</span></span>
</dt> <dt>



<span data-ttu-id="321d3-145">Intervallo di valori possibili per il numero di entità di imposizione.</span><span class="sxs-lookup"><span data-stu-id="321d3-145">The range of possible values for the number of enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**</span><span class="sxs-lookup"><span data-stu-id="321d3-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-147">0xC8</span><span class="sxs-lookup"><span data-stu-id="321d3-147">0xC8</span></span>
</dt> <dt>



<span data-ttu-id="321d3-148">Dimensione massima, in byte, di una struttura [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) .</span><span class="sxs-lookup"><span data-stu-id="321d3-148">The maximum size, in bytes, of a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**</span><span class="sxs-lookup"><span data-stu-id="321d3-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-150">0x14</span><span class="sxs-lookup"><span data-stu-id="321d3-150">0x14</span></span>
</dt> <dt>



<span data-ttu-id="321d3-151">Numero massimo di oggetti [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) associati a un'entità di imposizione.</span><span class="sxs-lookup"><span data-stu-id="321d3-151">The maximum number of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) objects associated with an enforcement entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**</span><span class="sxs-lookup"><span data-stu-id="321d3-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-153">maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer</span><span class="sxs-lookup"><span data-stu-id="321d3-153">maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer</span></span>
</dt> <dt>



<span data-ttu-id="321d3-154">Numero massimo di connessioni a rapporto di integrità memorizzato nella cache per tutte le entità integrità sistema e imposizione.</span><span class="sxs-lookup"><span data-stu-id="321d3-154">The maximum number of cached SoH connections for all system health and enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="321d3-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-156">0x1</span><span class="sxs-lookup"><span data-stu-id="321d3-156">0x1</span></span>
</dt> <dt>



<span data-ttu-id="321d3-157">Specifica che un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)è dovuto a una nuova richiesta, non a una richiesta memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="321d3-157">Specifies that an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)is due to a new request, not a cached request.</span></span> <span data-ttu-id="321d3-158">Questo flag viene utilizzato dall'agente NAP su un oggetto [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="321d3-158">This flag is used by the NAP agent on an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**</span><span class="sxs-lookup"><span data-stu-id="321d3-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-160">0x1</span><span class="sxs-lookup"><span data-stu-id="321d3-160">0x1</span></span>
</dt> <dt>



<span data-ttu-id="321d3-161">Specifica che la correzione è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="321d3-161">Specifies that fix-up is required.</span></span> <span data-ttu-id="321d3-162">Questo flag viene usato da un SHA.</span><span class="sxs-lookup"><span data-stu-id="321d3-162">This flag is used by a SHA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**</span><span class="sxs-lookup"><span data-stu-id="321d3-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-164">0x5</span><span class="sxs-lookup"><span data-stu-id="321d3-164">0x5</span></span>
</dt> <dt>



<span data-ttu-id="321d3-165">Numero di categorie di errore contenute all'interno di una struttura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .</span><span class="sxs-lookup"><span data-stu-id="321d3-165">The number of failure categories contained within a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**</span><span class="sxs-lookup"><span data-stu-id="321d3-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-167">0x1</span><span class="sxs-lookup"><span data-stu-id="321d3-167">0x1</span></span>
</dt> <dt>



<span data-ttu-id="321d3-168">Il componente è un client di imposizione della quarantena (QEC) che invia un pacchetto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) in banda durante l'autenticazione della connessione.</span><span class="sxs-lookup"><span data-stu-id="321d3-168">The component is a quarantine enforcement client (QEC) that sends an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet in-band during connection authentication.</span></span>

> [!Note]  
> <span data-ttu-id="321d3-169">Questo valore non viene usato da SHAs e SHV.</span><span class="sxs-lookup"><span data-stu-id="321d3-169">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**</span><span class="sxs-lookup"><span data-stu-id="321d3-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-171">0x2</span><span class="sxs-lookup"><span data-stu-id="321d3-171">0x2</span></span>
</dt> <dt>



<span data-ttu-id="321d3-172">Il componente è un QEC che implementa [**INapCertRelyingParty**](inapcertrelyingparty.md) e deve interagire con il server dei certificati di integrità (HCS) per ottenere un certificato di integrità.</span><span class="sxs-lookup"><span data-stu-id="321d3-172">The component is a QEC that implements [**INapCertRelyingParty**](inapcertrelyingparty.md) and must interact with the Health Certificate Server (HCS) in order to obtain a health certificate.</span></span>

> [!Note]  
> <span data-ttu-id="321d3-173">Questo valore non viene usato da SHAs e SHV.</span><span class="sxs-lookup"><span data-stu-id="321d3-173">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> </dl>

<span data-ttu-id="321d3-174">Le costanti NAP seguenti sono definite in NapEnforcementClient. h.</span><span class="sxs-lookup"><span data-stu-id="321d3-174">The following NAP constants are defined in NapEnforcementClient.h.</span></span>

<dl> <dt>

<span data-ttu-id="321d3-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="321d3-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-176">0x0FA0</span><span class="sxs-lookup"><span data-stu-id="321d3-176">0x0FA0</span></span>
</dt> <dt>



<span data-ttu-id="321d3-177">Dimensione massima predefinita, in byte, di un pacchetto di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="321d3-177">The default maximum size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="321d3-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-179">0xFFFF</span><span class="sxs-lookup"><span data-stu-id="321d3-179">0xFFFF</span></span>
</dt> <dt>



<span data-ttu-id="321d3-180">Dimensione massima possibile, in byte, di un pacchetto di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="321d3-180">The maximum possible size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="321d3-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-182">0x012C</span><span class="sxs-lookup"><span data-stu-id="321d3-182">0x012C</span></span>
</dt> <dt>



<span data-ttu-id="321d3-183">Dimensione massima minima possibile, in byte, di un pacchetto di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="321d3-183">The smallest possible maximum size, in bytes, of an SoH packet.</span></span> <span data-ttu-id="321d3-184">Le dimensioni effettive del pacchetto di rapporto di integrità possono essere inferiori a **minProtocolMaxSize**.</span><span class="sxs-lookup"><span data-stu-id="321d3-184">The actual size of the SoH packet may be smaller than **minProtocolMaxSize**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="321d3-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="321d3-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="321d3-186">intervallo (minProtocolMaxSize, maxProtocolMaxSize)</span><span class="sxs-lookup"><span data-stu-id="321d3-186">range(minProtocolMaxSize, maxProtocolMaxSize)</span></span>
</dt> <dt>



<span data-ttu-id="321d3-187">Intervallo di valori possibili per la dimensione massima di un pacchetto di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="321d3-187">The range of possible values for the maximum size of a SoH packet.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="321d3-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="321d3-188">Requirements</span></span>



| <span data-ttu-id="321d3-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="321d3-189">Requirement</span></span> | <span data-ttu-id="321d3-190">Valore</span><span class="sxs-lookup"><span data-stu-id="321d3-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="321d3-191">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="321d3-191">Minimum supported client</span></span><br/> | <span data-ttu-id="321d3-192">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="321d3-192">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="321d3-193">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="321d3-193">Minimum supported server</span></span><br/> | <span data-ttu-id="321d3-194">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="321d3-194">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="321d3-195">Intestazione</span><span class="sxs-lookup"><span data-stu-id="321d3-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="321d3-196"><dt>NapTypes. h; </dt> <dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="321d3-196"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="321d3-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="321d3-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321d3-198">**Costanti NAP**</span><span class="sxs-lookup"><span data-stu-id="321d3-198">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 





