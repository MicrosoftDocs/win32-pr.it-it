---
description: L'API DRT (Distributed routing table) utilizza le funzioni seguenti.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Funzioni della tabella di routing distribuita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312286"
---
# <a name="distributed-routing-table-functions"></a>Funzioni della tabella di routing distribuita

L'API DRT (Distributed routing table) utilizza le funzioni seguenti.

## <a name="lifetime-management-functions"></a>Funzioni di gestione della durata



| Funzione                                           | Descrizione                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen)                         | Crea un'istanza di DRT locale usando i criteri specificati dalla struttura [**\_ delle impostazioni di DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .  |
| [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose)                       | Chiude e rimuove l'istanza locale di DRT.                                                              |
| [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | Recupera i dati dell'evento associati a un evento segnalato.                                                         |
| [**DrtGetEventDataSize**](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | Restituisce la dimensione della struttura [**di \_ \_ dati dell'evento DRT**](/windows/desktop/api/drt/ns-drt-drt_event_data) associata a un evento segnalato. |



 

## <a name="module-management-functions"></a>Funzioni di gestione dei moduli



| Funzione                                                                           | Descrizione                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtCreatePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | Crea un resolver bootstrap basato sul protocollo PNRP.                                                                              |
| [**DrtDeletePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | Elimina un resolver bootstrap basato sul protocollo PNRP.                                                                              |
| [**DrtCreateDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | Crea un provider bootstrap che contatterà un host noto in base al nome.                                                             |
| [**DrtDeleteDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | Elimina un provider bootstrap che contatterà un host noto in base al nome.                                                             |
| [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | Crea un trasporto basato sul protocollo UDP IPv6.                                                                                   |
| [**DrtDeleteIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | Elimina un trasporto basato sul protocollo UDP IPv6.                                                                                   |
| [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | Crea un provider di sicurezza delle chiavi derivato per DRT.                                                                                  |
| [**DrtCreateDerivedKey**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | Crea una chiave che può essere utilizzata da [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) quando DRT utilizza un provider di sicurezza della chiave derivata. |
| [**DrtDeleteDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | Elimina un provider di sicurezza della chiave derivata per DRT.                                                                                  |
| [**DrtCreateNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | Crea un provider di sicurezza null. Questo provider di sicurezza non richiede nodi per l'autenticazione delle chiavi.                                 |
| [**DrtDeleteNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | Elimina un provider di sicurezza null.                                                                                                     |



 

## <a name="registration-functions"></a>Funzioni di registrazione



| Funzione                                     | Descrizione                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | Registra una chiave in DRT.                                    |
| [**DrtUpdateKey**](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | Aggiorna i dati dell'applicazione associati a una chiave registrata. |
| [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | Annulla la registrazione di una chiave dal DRT.                                |



 

## <a name="search-functions"></a>Funzioni di ricerca



| Funzione                                                 | Descrizione                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | Cerca una chiave in DRT usando i criteri specificati nella struttura [**delle \_ \_ informazioni di ricerca DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .                                                                                                      |
| [**DrtContinueSearch**](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | Continua una ricerca \_ \_ \_ di un percorso di DRT di ricerca di una chiave in DRT. Questa funzione viene usata solo quando il flag **fIterative** è impostato su **true** nella struttura associata [**di \_ \_ informazioni di ricerca DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) . |
| [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | Recupera i risultati della ricerca.                                                                                                                                                                                         |
| [**DrtGetSearchResultSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | Restituisce la dimensione del successivo risultato della ricerca disponibile.                                                                                                                                                                   |
| [**DrtGetSearchPath**](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | Restituisce un elenco di nodi contattati durante l'operazione di ricerca.                                                                                                                                                          |
| [**DrtGetSearchPathSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | Restituisce la dimensione del percorso di ricerca che rappresenta il numero di nodi utilizzati nell'operazione di ricerca.                                                                                                             |
| [**DrtEndSearch**](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | Annulla la ricerca di una chiave in un DRT e, di conseguenza, la restituzione dei risultati tramite il [**\_ \_ risultato della ricerca DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) viene arrestata. Questa API può essere chiamata in qualsiasi momento dopo l'emissione di una ricerca.              |



 

## <a name="instance-name-functions"></a>Funzioni nome istanza



| Funzione                                                 | Descrizione                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**DrtGetInstanceName**](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | Ottiene il nome associato a un'istanza di DRT.                    |
| [**DrtGetInstanceNameSize**](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | Restituisce le dimensioni del nome dell'istanza della tabella di routing distribuita. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazioni tabella di routing distribuita](distributed-routing-table-enumerations.md)
</dt> <dt>

[Strutture della tabella di routing distribuita](distributed-routing-table-structures.md)
</dt> <dt>

[Riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



