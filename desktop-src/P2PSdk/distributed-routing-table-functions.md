---
description: L'API DRT (Distributed Routing Table) usa le funzioni seguenti.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Funzioni delle tabelle di routing distribuito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00501a1a04a3acba23fe55f90acfbf7ca8fee7427c36ea1d36d8800fb8787321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776351"
---
# <a name="distributed-routing-table-functions"></a>Funzioni delle tabelle di routing distribuito

L'API DRT (Distributed Routing Table) usa le funzioni seguenti.

## <a name="lifetime-management-functions"></a>Funzioni di gestione della durata



| Funzione                                           | Descrizione                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen)                         | Crea un'istanza DRT locale usando i criteri specificati dalla [**struttura DRT \_ SETTINGS.**](/windows/desktop/api/drt/ns-drt-drt_settings)  |
| [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose)                       | Chiude e rimuove l'istanza locale di DRT.                                                              |
| [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | Recupera i dati dell'evento associati a un evento segnalato.                                                         |
| [**DrtGetEventDataSize**](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | Restituisce le dimensioni della struttura [**DRT \_ EVENT \_ DATA**](/windows/desktop/api/drt/ns-drt-drt_event_data) associata a un evento segnalato. |



 

## <a name="module-management-functions"></a>Funzioni di gestione dei moduli



| Funzione                                                                           | Descrizione                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtCreatePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | Crea un sistema di risoluzione bootstrap basato sul protocollo PNRP.                                                                              |
| [**DrtDeletePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | Elimina un sistema di risoluzione bootstrap basato sul protocollo PNRP.                                                                              |
| [**DrtCreateDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | Crea un provider bootstrap che contatta un host noto in base al nome.                                                             |
| [**DrtDeleteDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | Elimina un provider bootstrap che contatta un host noto in base al nome.                                                             |
| [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | Crea un trasporto basato sul protocollo UDP IPv6.                                                                                   |
| [**DrtDeleteIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | Elimina un trasporto in base al protocollo UDP IPv6.                                                                                   |
| [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | Crea un provider di sicurezza delle chiavi derivato per DRT.                                                                                  |
| [**DrtCreateDerivedKey**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | Crea una chiave che può essere utilizzata da [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) quando DRT usa un provider di sicurezza delle chiavi derivato. |
| [**DrtDeleteDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | Elimina un provider di sicurezza delle chiavi derivato per DRT.                                                                                  |
| [**DrtCreateNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | Crea un provider di sicurezza Null. Questo provider di sicurezza non richiede nodi per autenticare le chiavi.                                 |
| [**DrtDeleteNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | Elimina un provider di sicurezza Null.                                                                                                     |



 

## <a name="registration-functions"></a>Funzioni di registrazione



| Funzione                                     | Descrizione                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | Registra una chiave in DRT.                                    |
| [**DrtUpdateKey**](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | Aggiorna i dati dell'applicazione associati a una chiave registrata. |
| [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | Annulla la registrazione di una chiave da DRT.                                |



 

## <a name="search-functions"></a>Funzioni di ricerca



| Funzione                                                 | Descrizione                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | Cerca una chiave in DRT usando i criteri specificati nella struttura [**DRT \_ SEARCH \_ INFO.**](/windows/desktop/api/drt/ns-drt-drt_search_info)                                                                                                      |
| [**DrtContinueSearch**](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | Continua una ricerca DRT \_ SEARCH RETURN PATH per una chiave in \_ \_ DRT. Questa funzione viene usata solo quando il flag **fIterative** è impostato su **TRUE** nella struttura [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) associata. |
| [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | Recupera i risultati della ricerca.                                                                                                                                                                                         |
| [**DrtGetSearchResultSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | Restituisce le dimensioni del successivo risultato della ricerca disponibile.                                                                                                                                                                   |
| [**DrtGetSearchPath**](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | Restituisce un elenco di nodi contattati durante l'operazione di ricerca.                                                                                                                                                          |
| [**DrtGetSearchPathSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | Restituisce le dimensioni del percorso di ricerca, che rappresenta il numero di nodi utilizzati nell'operazione di ricerca.                                                                                                             |
| [**DrtEndSearch**](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | Annulla una ricerca di una chiave in una DRT e, di conseguenza, la restituzione dei risultati tramite [**DRT \_ SEARCH \_ RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) viene arrestata. Questa API può essere chiamata in qualsiasi momento dopo l'emissione di una ricerca.              |



 

## <a name="instance-name-functions"></a>Funzioni del nome dell'istanza



| Funzione                                                 | Descrizione                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**DrtGetInstanceName**](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | Ottiene il nome associato a un'istanza DRT.                    |
| [**DrtGetInstanceNameSize**](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | Restituisce le dimensioni del nome dell'istanza della tabella di routing distribuito. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazioni di tabelle di routing distribuito](distributed-routing-table-enumerations.md)
</dt> <dt>

[Strutture di tabelle di routing distribuito](distributed-routing-table-structures.md)
</dt> <dt>

[Informazioni di riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



