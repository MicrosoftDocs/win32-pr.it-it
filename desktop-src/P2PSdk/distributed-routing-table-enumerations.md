---
description: Le enumerazioni seguenti supportano l'API DRT (Distributed routing table).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Enumerazioni tabella di routing distribuita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c432b156a9299a9f70026a394a6fd97f06528a25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312287"
---
# <a name="distributed-routing-table-enumerations"></a>Enumerazioni tabella di routing distribuita

Le enumerazioni seguenti supportano l'API DRT (Distributed routing table).



| Enumerazione                                                            | Descrizione                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ambito DRT**](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | Definisce il set di ambiti IPv6 in cui DRT funzionerà quando si utilizza il trasporto UDP IPv6 creato da [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport). |
| [**\_flag indirizzi \_ DRT**](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | Definisce il set di risposte che possono essere restituite da un nodo intermedio durante l'esecuzione di una ricerca di una chiave.                                                         |
| [**\_stato DRT**](/windows/desktop/api/drt/ne-drt-drt_status)                                      | Definisce i possibili stati di connettività e di errore di un nodo locale.                                                                                                   |
| [**\_tipo di corrispondenza DRT \_**](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | Definisce l'esattezza dei risultati restituiti quando viene eseguita una ricerca.                                                                                                 |
| [**\_tipo di \_ modifica della chiave LEAFSET \_ di DRT \_**](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | Definisce il set di tipi di modifiche che possono essere eseguiti su un nodo set foglia locale nella cache DRT locale.                                                                |
| [**\_tipo di evento DRT \_**](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | Definisce il set di eventi che possono essere generati da DRT.                                                                                                              |
| [**\_modalità di sicurezza DRT \_**](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | Definisce le modalità di sicurezza possibili di DRT. Questa enumerazione è un campo della struttura [**delle \_ Impostazioni DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .                                   |
| [**\_stato di registrazione DRT \_**](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | Definisce lo stato di una chiave registrata.                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strutture della tabella di routing distribuita](distributed-routing-table-structures.md)
</dt> <dt>

[Funzioni della tabella di routing distribuita](distributed-routing-table-functions.md)
</dt> <dt>

[Riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



