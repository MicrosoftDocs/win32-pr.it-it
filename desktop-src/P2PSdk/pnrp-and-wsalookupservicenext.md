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
# <a name="pnrp-and-wsalookupservicenext"></a>PNRP e WSALookupServiceNext

PNRP utilizza la funzione [**WSALookupServiceNext**](winsock-nsp-reference-links.md) per trovare la corrispondenza con le query specificate in una precedente chiamata a **WSALookupServiceBegin**. I risultati della funzione **WSALookupServiceNext** sono determinati dalle impostazioni nella struttura **WSAQUERYSET** passata nella chiamata di funzione **WSALookupServiceBegin** iniziale. Questa funzione viene utilizzata per eseguire le due funzioni seguenti:

-   Risoluzione di un nome peer in un elenco di indirizzi
-   Enumerazione dei cloud di rete

Utilizzando [**WSANSPIoctl**](winsock-nsp-reference-links.md), il servizio di ricerca può essere utilizzato in modo asincrono. Per informazioni sull'uso asincrono delle funzioni del servizio di ricerca, vedere [PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md).

La funzione [**WSALookupServiceNext**](winsock-nsp-reference-links.md) si blocca anche se viene chiamato **WSANSPIoctl** . Prima di chiamare **WSALookupServiceNext**, un'applicazione deve attendere fino a quando non riceve una notifica, se il blocco è un problema.

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a>Risoluzione di un nome peer in un elenco di indirizzi

Quando si risolve un nome peer in un elenco di indirizzi, la struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) restituita nel parametro *lpqsResults* contiene i valori seguenti:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Restituisce la dimensione della struttura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Restituisce un nome peer: se **LUP restituisce il \_ \_ nome**, **LUP \_ restituisce \_ All** o **null** sono specificati.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Restituisce **SVCID \_ pnrpname**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Restituisce **null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Restituisce un commento, se **LUP \_ restituisce \_ Comment**, **LUP \_ restituisce \_ All** o **null** .

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Restituisce **NS \_ pnrpname**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Restituisce **il \_ provider NS \_ pnrpname**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Restituisce il nome del cloud se viene specificato il **\_ \_ nome restituito LUP**, **LUP \_ return \_ All** o **null** .

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Restituisce zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Restituisce **null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Restituisce il numero di voci nella matrice di \_ informazioni CSADDR se **LUP \_ restituisce \_ addr**, **LUP \_ restituisce \_ All** o **null** . Questo valore e le informazioni in **lpcsaBuffer** sono i bit chiave delle informazioni restituite nella struttura.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Restituisce un puntatore a una matrice di \_ strutture di informazioni CSADDR se **LUP \_ restituisce \_ addr**, **LUP \_ restituisce \_ All** o **null** . Questo buffer e il valore in **dwNumberOfCsAddrs** sono i bit di informazioni chiave restituiti in questa struttura.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Restituisce zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Restituisce **null**.

</dd> </dl>

## <a name="enumerating-network-clouds"></a>Enumerazione dei cloud di rete

Quando si enumerano i cloud, la struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) restituita nel parametro *lpqsResults* contiene i valori seguenti:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Restituisce la dimensione della struttura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Restituisce un nome cloud: se **LUP restituisce il \_ \_ nome**, **LUP \_ restituisce \_ All** o **null** sono specificati.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Restituisce **SVCID \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Restituisce **null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Restituisce **null**.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Restituisce **NS \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Restituisce **\_ \_ PNRPCLOUD del provider NS**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Restituisce **null**.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Restituisce zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Restituisce **null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Restituisce zero (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Restituisce **null**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Restituisce zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Restituisce un puntatore a una struttura [**BLOB**](winsock-nsp-reference-links.md) che punta a una struttura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) , se **LUP \_ restituisce \_ BLOB**, **LUP \_ restituisce \_ All** o **null** .

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a>Struttura PNRPCLOUDINFO

Quando si enumerano i nomi cloud, nella struttura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) vengono restituiti i valori seguenti:

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

Stato corrente di un cloud. [**PNRP \_ \_Stato cloud**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) specifica i valori validi.

</dd> <dt>

<span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**
</dt> <dd>

Indica che un nome cloud è valido in una rete o è valido solo in un computer corrente. [**PNRP \_ \_Flag cloud**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) specifica i valori validi. Alcuni nomi cloud sono validi in tutti i computer della stessa rete. Altri nomi di cloud sono validi solo in un computer corrente e possono essere validi solo per un periodo di tempo.

-   Se **enCloudFlags** è impostato sul **\_ nome cloud \_ PNRP \_ locale,** il nome è valido solo localmente.
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

 

 



