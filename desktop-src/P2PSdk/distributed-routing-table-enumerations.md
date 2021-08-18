---
description: Le enumerazioni seguenti supportano l'API DRT (Distributed Routing Table).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Enumerazioni di tabelle di routing distribuito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ff0a955aed8d6ed6cdf14f3d0e7f6ac2605960123f8008c831dbef5be2da98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011599"
---
# <a name="distributed-routing-table-enumerations"></a>Enumerazioni di tabelle di routing distribuito

Le enumerazioni seguenti supportano l'API DRT (Distributed Routing Table).



| Enumerazione                                                            | Descrizione                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AMBITO \_ DRT**](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | Definisce il set di ambiti IPv6 in cui DRT funzionerà quando si usa il trasporto UDP IPv6 creato da [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport). |
| [**FLAG DI \_ INDIRIZZO DRT \_**](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | Definisce il set di risposte che possono essere restituite da un nodo intermedio quando si esegue una ricerca di una chiave.                                                         |
| [**STATO \_ DRT**](/windows/desktop/api/drt/ne-drt-drt_status)                                      | Definisce i possibili stati di connettività ed errore di un nodo locale.                                                                                                   |
| [**TIPO DI \_ CORRISPONDENZA \_ DRT**](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | Definisce l'esattezza dei risultati restituiti quando viene eseguita una ricerca.                                                                                                 |
| [**DRT \_ LEAFSET \_ KEY \_ CHANGE \_ TYPE**](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | Definisce il set di tipi di modifica che possono essere eseguiti in un nodo del set foglia locale nella cache DRT locale.                                                                |
| [**TIPO DI \_ EVENTO \_ DRT**](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | Definisce il set di eventi che possono essere generati da DRT.                                                                                                              |
| [**MODALITÀ DI \_ SICUREZZA \_ DRT**](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | Definisce le possibili modalità di sicurezza di DRT. Questa enumerazione è un campo della [**struttura DRT \_ SETTINGS.**](/windows/desktop/api/drt/ns-drt-drt_settings)                                   |
| [**STATO DI \_ REGISTRAZIONE \_ DRT**](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | Definisce lo stato di una chiave registrata.                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strutture di tabelle di routing distribuito](distributed-routing-table-structures.md)
</dt> <dt>

[Funzioni delle tabelle di routing distribuito](distributed-routing-table-functions.md)
</dt> <dt>

[Informazioni di riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



