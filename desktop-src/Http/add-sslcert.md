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
# <a name="add-sslcert"></a>add sslcert

Aggiunge un nuovo Secure Sockets Layer certificato server (SSL) e i criteri del certificato client corrispondenti per un indirizzo IP e una porta.

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

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport=INDIRIZZO IP:porta\]**
</dt> <dd>

Specifica l'indirizzo IP e la porta per il binding.

</dd> <dt>

<span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash=string\]**
</dt> <dd>

Specifica l'hash SHA del certificato. Questo hash ha una lunghezza di 20 byte e viene specificato come stringa esadecimale.

</dd> <dt>

<span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid=GUID\]**
</dt> <dd>

Specifica il GUID per identificare l'applicazione proprietaria.

</dd> <dt>

<span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename=string\]**
</dt> <dd>

Specifica il nome dell'archivio per il certificato. L'impostazione predefinita è MY. Il certificato deve essere archiviato nel contesto del computer locale.

</dd> <dt>

<span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable \| disable}\]**
</dt> <dd>

Attiva o disattiva la verifica della revoca dei certificati client.

</dd> <dt>

<span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable \| disable}\]**
</dt> <dd>

Attiva o disattiva l'utilizzo del solo certificato client memorizzato nella cache per il controllo delle revoche.

</dd> <dt>

<span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable \| disable}\]**
</dt> <dd>

Attiva o disattiva il controllo dell'utilizzo. L'impostazione predefinita corrisponde all'abilitazione.

</dd> <dt>

<span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime=u-int\]**
</dt> <dd>

Specifica l'intervallo di tempo in cui verificare la presenza di un elenco di revoche di certificati (CRL) aggiornato. Se questo valore è 0, il nuovo CRL viene aggiornato solo se quello precedente scade (in secondi).

</dd> <dt>

<span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout=u-int\]**
</dt> <dd>

Specifica l'intervallo di timeout per i tentativi di recupero dell'elenco di revoche di certificati per l'URL remoto (in millisecondi).

</dd> <dt>

<span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier=string\]**
</dt> <dd>

Elenca le autorità di certificazione che possono essere attendibili. Questo elenco può essere un sottoinsieme delle autorità di certificazione considerate attendibili dal computer.

</dd> <dt>

<span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename=string\]**
</dt> <dd>

Specifica il nome dell'archivio in LOCAL \_ MACHINE in cui è archiviato SslCtlIdentifier.

</dd> <dt>

<span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable \| disable}\]**
</dt> <dd>

Attiva o disattiva i mapping DS. L'impostazione predefinita corrisponde alla disabilitazione.

</dd> <dt>

<span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable \| disable}\]**
</dt> <dd>

Attiva o disattiva la negoziazione del certificato. L'impostazione predefinita corrisponde alla disabilitazione.

</dd> </dl>

## <a name="examples"></a>Esempio

**aggiungere sslcert ipport=1.1.1.1:443**

**certhash=0102030405060708090A0B0C0D0E0F101121314**

**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**

 

 




