---
description: PNRP usa la funzione WSALookupServiceNext per trovare la corrispondenza con le query specificate in una chiamata precedente a WSALookupServiceBegin.
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP e WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ec10c8021a2f13be1a1ffe228ca73a07c8af10dfc8714bef14f0bddeb0952aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553321"
---
# <a name="pnrp-and-wsalookupservicenext"></a>PNRP e WSALookupServiceNext

PNRP usa la [**funzione WSALookupServiceNext**](winsock-nsp-reference-links.md) per trovare la corrispondenza con le query specificate in una chiamata precedente a **WSALookupServiceBegin**. I risultati della **funzione WSALookupServiceNext** sono determinati dalle impostazioni nella struttura **WSAQUERYSET** passata nella chiamata di funzione **WSALookupServiceBegin** iniziale. Questa funzione viene usata per eseguire le due funzioni seguenti:

-   Risoluzione di un nome peer in un elenco di indirizzi
-   Enumerazione dei cloud di rete

Tramite [**WSANSPIoctl,**](winsock-nsp-reference-links.md)il servizio di ricerca può essere usato in modo asincrono. Per informazioni sull'uso delle funzioni del servizio di ricerca in modo asincrono, vedere [PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md).

La [**funzione WSALookupServiceNext**](winsock-nsp-reference-links.md) si blocca anche se **viene chiamato WSANSPIoctl.** Prima di **chiamare WSALookupServiceNext,** un'applicazione deve attendere fino a quando non riceve una notifica, se il blocco è un problema.

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a>Risoluzione di un nome peer in un elenco di indirizzi

Quando si risolve un nome peer in un elenco di indirizzi, la struttura [**LPWSAQUERYSET restituita**](pnrp-and-wsaqueryset.md) nel parametro *lpqsResults* contiene i valori seguenti:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Restituisce le dimensioni della struttura .

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Restituisce un nome peer, se **vengono specificati LUP \_ RETURN \_ NAME,** **LUP RETURN \_ \_ ALL** o **NULL.**

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Restituisce **SVCID \_ PNRPNAME**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Restituisce **NULL.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Restituisce un commento, se **vengono specificati LUP \_ RETURN \_ COMMENT,** **LUP RETURN \_ \_ ALL** o **NULL.**

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Restituisce **NS \_ PNRPNAME**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Restituisce **NS \_ PROVIDER \_ PNRPNAME**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Restituisce il nome del cloud **se vengono specificati LUP RETURN \_ \_ NAME,** **LUP RETURN \_ \_ ALL** o **NULL.**

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Restituisce zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Restituisce **NULL.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Restituisce il numero di voci nella matrice CSADDR INFO se vengono specificati \_ **LUP \_ RETURN \_ ADDR,** **LUP \_ RETURN \_ ALL** o **NULL.** Questo valore e le informazioni in **lpcsaBuffer** sono i bit chiave delle informazioni restituite in questa struttura.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Restituisce un puntatore a una matrice di strutture CSADDR INFO se si specifica \_ **LUP \_ RETURN \_ ADDR,** **LUP \_ RETURN \_ ALL** o **NULL.** Questo buffer e il valore in **dwNumberOfCsAddrs** sono i bit di informazioni chiave restituiti in questa struttura.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Restituisce zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Restituisce **NULL.**

</dd> </dl>

## <a name="enumerating-network-clouds"></a>Enumerazione dei cloud di rete

Durante l'enumerazione dei cloud, la struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) restituita nel parametro *lpqsResults* contiene i valori seguenti:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Restituisce le dimensioni della struttura .

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Restituisce un nome cloud, se **vengono specificati LUP \_ RETURN \_ NAME,** **LUP RETURN \_ \_ ALL** o **NULL.**

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Restituisce **SVCID \_ PNRPCLOUD.**

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Restituisce **NULL.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Restituisce **NULL.**

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Restituisce **NS \_ PNRPCLOUD.**

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Restituisce **NS \_ PROVIDER \_ PNRPCLOUD.**

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Restituisce **NULL.**

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Restituisce zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Restituisce **NULL.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Restituisce zero (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Restituisce **NULL.**

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Restituisce zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Restituisce un puntatore a una struttura [**BLOB**](winsock-nsp-reference-links.md) che punta a una struttura [**PNRPCLOUDINFO,**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) se vengono specificati **LUP \_ RETURN \_ BLOB,** **LUP RETURN \_ \_ ALL** o **NULL.**

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a>Struttura PNRPCLOUDINFO

Quando si enumerano i nomi del cloud, nella struttura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) vengono restituiti i valori seguenti:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Dimensione della struttura.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**
</dt> <dd>

Valore effettivo del cloud.

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**
</dt> <dd>

Stato corrente di un cloud. [**PNRP \_ CLOUD \_ STATE**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) specifica i valori validi.

</dd> <dt>

<span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**
</dt> <dd>

Indica che un nome cloud è valido in una rete o solo in un computer corrente. [**PNRP \_ CLOUD \_ FLAGS**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) specifica i valori validi. Alcuni nomi di cloud sono validi in qualsiasi computer nella stessa rete. Altri nomi cloud sono validi solo in un computer corrente e possono essere validi solo per un periodo di tempo.

-   Se **enCloudFlags** è impostato su **PNRP \_ CLOUD NAME \_ \_ LOCAL,** il nome è valido solo in locale.
-   Se **enCloudFlags** non è impostato, il nome del cloud può essere trasferito ad altri computer.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[PNRP e BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md)
</dt> <dt>

[PNRP e WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[Codici di errore PNRP NSP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSALookupServiceBegin**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



