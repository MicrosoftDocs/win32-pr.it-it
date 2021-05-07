---
title: add sslcert
description: Aggiunge un nuovo Secure Sockets Layer certificato server (SSL) e i criteri del certificato client corrispondenti per un indirizzo IP e una porta.
ms.assetid: 4ba3d2cb-050f-46e3-81f9-5f7e360b19fb
keywords:
- add sslcert HTTP
topic_type:
- apiref
api_name:
- add sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309050be35748f39eefc8b40b8e590f8f6889fde
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644193"
---
# <a name="add-sslcert"></a><span data-ttu-id="d7104-104">add sslcert</span><span class="sxs-lookup"><span data-stu-id="d7104-104">add sslcert</span></span>

<span data-ttu-id="d7104-105">Aggiunge un nuovo Secure Sockets Layer certificato server (SSL) e i criteri del certificato client corrispondenti per un indirizzo IP e una porta.</span><span class="sxs-lookup"><span data-stu-id="d7104-105">Adds a new Secure Sockets Layer (SSL) server certificate binding and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
add sslcert [ipport=]IP Address:port
            [certhash=]string
            [appid=]GUID
            [certstorename=]string
            [verifyclientcertrevocation={enable|disable}]
            [verifyrevocationwithcachedclientcertonly={enable|disable}]
            [usagecheck={enable|disable}]
            [revocationfreshnesstime=]u-int
            [urlretrievaltimeout=]u-int
            [sslctlidentifier=]string
            [sslctlstorename=]string
            [dsmapperusage={enable|disable}]
            [clientcertnegotiation={enable|disable}]

 
```

## <a name="parameters"></a><span data-ttu-id="d7104-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7104-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7104-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport=INDIRIZZO IP:porta\]**</span><span class="sxs-lookup"><span data-stu-id="d7104-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport=IP Address:port\]**</span></span>
</dt> <dd>

<span data-ttu-id="d7104-108">Specifica l'indirizzo IP e la porta per il binding.</span><span class="sxs-lookup"><span data-stu-id="d7104-108">Specifies the IP address and port for the binding.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash=string\]**</span><span class="sxs-lookup"><span data-stu-id="d7104-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="d7104-110">Specifica l'hash SHA del certificato.</span><span class="sxs-lookup"><span data-stu-id="d7104-110">Specifies the SHA hash of the certificate.</span></span> <span data-ttu-id="d7104-111">Questo hash ha una lunghezza di 20 byte e viene specificato come stringa esadecimale.</span><span class="sxs-lookup"><span data-stu-id="d7104-111">This hash is 20 bytes long and specified as a hexadecimal string.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid=GUID\]**</span><span class="sxs-lookup"><span data-stu-id="d7104-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid=GUID\]**</span></span>
</dt> <dd>

<span data-ttu-id="d7104-113">Specifica il GUID per identificare l'applicazione proprietaria.</span><span class="sxs-lookup"><span data-stu-id="d7104-113">Specifies the GUID to identify the owning application.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename=string\]**</span><span class="sxs-lookup"><span data-stu-id="d7104-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="d7104-115">Specifica il nome dell'archivio per il certificato.</span><span class="sxs-lookup"><span data-stu-id="d7104-115">Specifies the store name for the certificate.</span></span> <span data-ttu-id="d7104-116">L'impostazione predefinita è MY.</span><span class="sxs-lookup"><span data-stu-id="d7104-116">Defaults to MY.</span></span> <span data-ttu-id="d7104-117">Il certificato deve essere archiviato nel contesto del computer locale.</span><span class="sxs-lookup"><span data-stu-id="d7104-117">Certificate must be stored in the local computer context.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="d7104-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="d7104-119">Attiva o disattiva la verifica della revoca dei certificati client.</span><span class="sxs-lookup"><span data-stu-id="d7104-119">Turns on or turnsoff verification of revocation of client certificates.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="d7104-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="d7104-121">Attiva o disattiva l'utilizzo del solo certificato client memorizzato nella cache per il controllo delle revoche.</span><span class="sxs-lookup"><span data-stu-id="d7104-121">Turns on or turns off usage of only cached client certificate for revocation checking.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="d7104-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="d7104-123">Attiva o disattiva il controllo dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="d7104-123">Turns on or turns off usage check.</span></span> <span data-ttu-id="d7104-124">L'impostazione predefinita corrisponde all'abilitazione.</span><span class="sxs-lookup"><span data-stu-id="d7104-124">Default is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime=u-int\]**</span><span class="sxs-lookup"><span data-stu-id="d7104-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime=u-int\]**</span></span>
</dt> <dd>

<span data-ttu-id="d7104-126">Specifica l'intervallo di tempo in cui verificare la presenza di un elenco di revoche di certificati (CRL) aggiornato.</span><span class="sxs-lookup"><span data-stu-id="d7104-126">Specifies the time interval to check for an updated certificate revocation list (CRL).</span></span> <span data-ttu-id="d7104-127">Se questo valore è 0, il nuovo CRL viene aggiornato solo se quello precedente scade (in secondi).</span><span class="sxs-lookup"><span data-stu-id="d7104-127">If this value is 0, then the new CRL is updated only if the previous one expires (in seconds).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout=u-int\]**</span><span class="sxs-lookup"><span data-stu-id="d7104-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout=u-int\]**</span></span>
</dt> <dd>

<span data-ttu-id="d7104-129">Specifica l'intervallo di timeout per i tentativi di recupero dell'elenco di revoche di certificati per l'URL remoto (in millisecondi).</span><span class="sxs-lookup"><span data-stu-id="d7104-129">Specifies the timeout interval on attempts to retrieve the certificate revocation list for the remote URL (in milliseconds).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier=string\]**</span><span class="sxs-lookup"><span data-stu-id="d7104-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="d7104-131">Elenca le autorità di certificazione che possono essere attendibili.</span><span class="sxs-lookup"><span data-stu-id="d7104-131">Lists the certificate issuers that can be trusted.</span></span> <span data-ttu-id="d7104-132">Questo elenco può essere un sottoinsieme delle autorità di certificazione considerate attendibili dal computer.</span><span class="sxs-lookup"><span data-stu-id="d7104-132">This list can be a subset of the certificate issuers that are trusted by the computer.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename=string\]**</span><span class="sxs-lookup"><span data-stu-id="d7104-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="d7104-134">Specifica il nome dell'archivio in LOCAL \_ MACHINE in cui è archiviato SslCtlIdentifier.</span><span class="sxs-lookup"><span data-stu-id="d7104-134">Specifies the store name under LOCAL\_MACHINE where SslCtlIdentifier is stored.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="d7104-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="d7104-136">Attiva o disattiva i mapping DS.</span><span class="sxs-lookup"><span data-stu-id="d7104-136">Turns on or turns off DS mappers.</span></span> <span data-ttu-id="d7104-137">L'impostazione predefinita corrisponde alla disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="d7104-137">Default is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="d7104-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="d7104-139">Attiva o disattiva la negoziazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="d7104-139">Turns on or turns off negotiation of certificate.</span></span> <span data-ttu-id="d7104-140">L'impostazione predefinita corrisponde alla disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="d7104-140">Default is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d7104-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="d7104-141">Examples</span></span>

<span data-ttu-id="d7104-142">**aggiungere sslcert ipport=1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="d7104-142">**add sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="d7104-143">**certhash=0102030405060708090A0B0C0D0E0F101121314**</span><span class="sxs-lookup"><span data-stu-id="d7104-143">**certhash=0102030405060708090A0B0C0D0E0F1011121314**</span></span>

<span data-ttu-id="d7104-144">**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**</span><span class="sxs-lookup"><span data-stu-id="d7104-144">**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**</span></span>

 

 




