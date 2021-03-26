---
description: Gestione sincronizzazione fornisce una tecnologia standard centralizzata per la sincronizzazione dei file per l'utilizzo offline in un computer portatile o in un computer connesso a una rete locale.
title: Gestione sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6cdac7e5-8985-407a-98bb-936bb20ed069
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbOrient
ms.openlocfilehash: 2fc56b2afec4fdedf98fe213437a27f2592ce72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994784"
---
# <a name="synchronization-manager"></a>Gestione sincronizzazione

## <a name="purpose"></a>Scopo

Gestione sincronizzazione fornisce una tecnologia standard centralizzata per la sincronizzazione dei file per l'utilizzo offline in un computer portatile o in un computer connesso a una rete locale. Con le funzioni di connettività, le notifiche (servizio di notifica degli eventi di sistema) e la memorizzazione nella cache sul lato client, Gestione sincronizzazione fornisce un'infrastruttura per il supporto del calcolo mobile. Anziché ogni applicazione che implementa la propria tecnologia per memorizzare nella cache e sincronizzare le risorse di rete per l'utilizzo locale, il sistema operativo fornisce un modello integrato che può essere utilizzato da tutte le applicazioni. I file sono sincronizzati indipendentemente dal protocollo. Un programma di posta elettronica, ad esempio, può trasferire i messaggi utilizzando SMTP, NMTP o POP3, mentre un browser può utilizzare HTTP e un database può utilizzare RPC (Remote Procedure Call). Gli sviluppatori possono utilizzare l'interfaccia comune di gestione sincronizzazione nelle proprie applicazioni per sincronizzare i file tra il computer locale dell'utente e l'archiviazione di rete.

## <a name="where-applicable"></a>Se applicabile

Gestione sincronizzazione è progettato per le applicazioni che vengono eseguite principalmente sui computer portatili. Anche le applicazioni in esecuzione su computer connessi a reti locali a latenza elevata possono trarre vantaggio dall'utilizzo di gestione sincronizzazione.

## <a name="developer-audience"></a>Sviluppatori

Questo documento è destinato agli sviluppatori di software che sviluppano applicazioni per il mobile computing e le reti locali a latenza elevata. Questo documento fornisce un riferimento completo di tutte le parti del gestore della sincronizzazione, inclusi i metodi e le interfacce per la gestione della sincronizzazione.

## <a name="run-time-requirements"></a>Requisiti di runtime

Richiede Windows Server 2003, Windows XP, Windows 2000 o Windows Millennium Edition (Windows Me). Disponibile anche come ridistribuibile per Microsoft Windows NT 4,0, Windows 98 e Windows 95.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                       | Descrizione                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni su Gestione sincronizzazione](syncmgr-about.md)<br/>                               | Gestione sincronizzazione fornisce una tecnologia standard centralizzata per la sincronizzazione dei file per l'utilizzo offline in un computer locale.<br/>     |
| [Configurazioni di mobile computing](syncmgr-mobile-computing-configs.md)<br/>          | Le applicazioni possono utilizzare sincronizzazione Manager per gestire i file e le risorse memorizzati nella cache in locale e sincronizzati nei computer desktop e portatili.<br/> |
| [Scenari applicativi](syncmgr-app-scenarios.md)<br/>                               | Applicazioni e servizi che possono usare Gestione sincronizzazione.<br/>                                                                          |
| [Architettura di gestione sincronizzazione](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [Utilizzo di gestione sincronizzazione da un programma](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [Informazioni di riferimento su Gestione sincronizzazione](syncmgr-reference.md)<br/>                       | Gli elementi di programmazione seguenti costituiscono l'API per Gestione sincronizzazione.<br/>                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul servizio di notifica eventi di sistema](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 
