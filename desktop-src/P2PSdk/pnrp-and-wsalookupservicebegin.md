---
description: PNRP usa la funzione WSALookupServiceBegin per avviare il processo che consente a un'applicazione di eseguire le operazioni seguenti.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP e WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a90bee9e2979f80464b05a3f2891cc7d3cc8e1fa10fe33faefb7319940e321f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553401"
---
# <a name="pnrp-and-wsalookupservicebegin"></a>PNRP e WSALookupServiceBegin

PNRP usa la [**funzione WSALookupServiceBegin**](winsock-nsp-reference-links.md) per avviare il processo che consente a un'applicazione di eseguire le operazioni seguenti:

-   [Risoluzione di un nome](#resolving-a-name)
-   [Enumerazione dei cloud di rete](#enumerating-network-clouds)

I client che tentano di eseguire una delle funzioni usano le funzioni [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext** e **WSALookupServiceEnd.**

Tramite [**WSANSPIoctl**](winsock-nsp-reference-links.md), il servizio di ricerca può essere utilizzato in modo asincrono. Per informazioni sull'uso delle funzioni del servizio di ricerca in modo asincrono, vedere [PNRP e WSANSPIoctl.](pnrp-and-wsanspioctl.md)

Il processo per l'uso dei nomi di peer è diverso dall'uso dei cloud. Ogni processo viene descritto separatamente in questo argomento.

## <a name="resolving-a-name"></a>Risoluzione di un nome

Un'applicazione [**usa WSALookupServiceBegin**](winsock-nsp-reference-links.md) per ottenere l'indirizzo IP, la porta e il protocollo per un servizio peer registrato in un altro computer. La **funzione WSALookupServiceBegin** viene usata per avviare il processo di risoluzione dei nomi e configurare i parametri e le restrizioni. Viene restituito un handle e deve essere utilizzato quando si chiama **WSALookupServiceNext** e **WSANSPIoctl**.

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Quando si risolve un nome peer, la struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a cui fa riferimento il parametro *lpqsRestrictions* deve contenere i valori seguenti:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Specifica le dimensioni della struttura .

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Specifica un nome peer da risolvere.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Deve essere **SVCID \_ PNRPNAME**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Riservato, deve essere **NULL.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Riservato, deve essere **NULL.**

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Deve essere **NS \_ PNRPNAME** o **NS \_ ALL.**

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Deve essere **NS \_ PROVIDER \_ PNRPNAME** o **NULL.**

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Deve essere un nome cloud, una stringa vuota o **NULL.** Se questo valore è **NULL** o una stringa vuota, viene usato il cloud predefinito \_ "Global". In caso contrario, deve puntare a un nome di cloud valido.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Riservato, deve essere zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Riservato, deve essere **NULL.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Riservato, deve essere zero (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Riservato, deve essere **NULL.**

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Riservato, deve essere zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Deve essere un puntatore a una [**struttura BLOB**](winsock-nsp-reference-links.md) o **NULL.** Se è **NULL,** vengono usati i valori predefiniti. Se è impostato, **lpBlob** punta a una [**struttura PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) ed è necessario impostare parametri specifici nella **struttura PNRPINFO.** Per altre informazioni, vedere le descrizioni seguenti per la struttura PNRPINFO.

</dd> </dl>

Struttura PNRPINFO

Se il **membro lpBlob** della struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) è impostato, è necessario impostare i membri seguenti della [**struttura PNRPINFO:**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Specifica le dimensioni della struttura .

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

Riservato, deve essere **NULL.**

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

Specifica il numero richiesto di risoluzioni.

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**
</dt> <dd>

Specifica il periodo di timeout richiesto per l'attesa delle risposte. Il valore predefinito è 30 secondi. Il valore massimo è 600 secondi (10 minuti).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

Riservato, deve essere zero (0).

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

Deve essere uno dei valori consentiti. Il valore predefinito è **PNRP \_ RESOLVE CRITERIA NON CURRENT PROCESS PEER \_ \_ \_ \_ \_ \_ NAME**. I valori validi vengono specificati da [**PNRP \_ RESOLVE \_ CRITERIA.**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**Dwflags**
</dt> <dd>

Deve essere zero (0) o **PNRPINFO \_ HINT**. Il valore predefinito è zero (0).

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**
</dt> <dd>

Specifica l'indirizzo IP per l'hint. L'hint viene usato quando si tenta di trovare il nome peer più vicino. Il formato dell'hint è un indirizzo IPv6. Se **saHint** non viene specificato durante la ricerca del nome peer più vicino, viene invece usato un indirizzo IPv6 del computer locale. Questo membro viene ignorato **se dwFlags** non è impostato.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**
</dt> <dd>

Riservato, deve essere zero (0).

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

I flag LUP \_ RETURN seguenti sono supportati da \_ \* PNRP:



| Valore                | Descrizione                                |
|----------------------|--------------------------------------------|
| NOME \_ RESTITUITO \_ LUP    | Restituisce un nome e un contesto.                |
| COMMENTO \_ RESTITUITO \_ LUP | Restituisce un commento associato a un nome.  |
| LUP \_ RETURN \_ ADDR    | Restituisce un indirizzo associato a un nome. |



 

## <a name="enumerating-network-clouds"></a>Enumerazione dei cloud di rete

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Durante l'enumerazione dei cloud, la struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a cui fa riferimento il parametro *lpqsRestrictions* deve contenere i valori seguenti:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Specifica le dimensioni della struttura .

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Deve essere **NULL.**

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Deve essere **SVCID \_ PNRPCLOUD.**

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Riservato, deve essere **NULL.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Riservato, deve essere **NULL.**

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Deve essere **NS \_ PNRPCLOUD.**

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Deve essere **provider NS \_ \_ PNRPCLOUD** o **NULL.**

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Riservato, deve essere **NULL.**

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Riservato, deve essere zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Riservato, deve essere **NULL.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Riservato, deve essere zero (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Riservato, deve essere **NULL.**

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Riservato, deve essere zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Puntatore a [**una struttura BLOB**](winsock-nsp-reference-links.md) che punta a una struttura [**PNRPCLOUDINFO.**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) Se **lpBlob** è **NULL,** vengono enumerati tutti i cloud.

</dd> </dl>

Struttura PNRPCLOUDINFO

Quando si enumerano i cloud, è necessario impostare i membri seguenti [**della struttura PNRPCLOUDINFO:**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Specifica le dimensioni della struttura .

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**
</dt> <dd>

Punta a una struttura che specifica i criteri che è possibile usare per filtrare i risultati della ricerca. Il **membro Cloud.Scope** può essere **PNRP \_ SCOPE \_ ANY,** **PNRP \_ GLOBAL \_ SCOPE,** **PNRP \_ SITE LOCAL \_ \_ SCOPE** o **PNRP \_ LINK LOCAL \_ \_ SCOPE.** Se **si specifica \_ PNRP SCOPE \_ ANY,** vengono restituiti tutti i cloud. In caso contrario, vengono restituiti solo i cloud **che corrispondono a Cloud.Scope.**

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**
</dt> <dd>

Riservato, deve essere zero (0).

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

I flag LUP \_ RETURN seguenti sono supportati da \_ \* PNRP:



| Valore             | Descrizione                                                       |
|-------------------|-------------------------------------------------------------------|
| NOME \_ RESTITUITO \_ LUP | Restituisce un nome e un contesto.                                       |
| BLOB \_ RESTITUITO LUP \_ | Restituisce il [BLOB](pnrp-and-blob.md) associato a questo cloud. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[PNRP e BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP e WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
</dt> <dt>

[PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md)
</dt> <dt>

[PNRP e WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[Codici di errore NSP PNRP](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 



