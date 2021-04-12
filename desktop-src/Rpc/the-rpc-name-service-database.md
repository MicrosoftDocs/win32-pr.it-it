---
title: Il database del servizio nome RPC
description: Un servizio nome è un servizio che esegue il mapping dei nomi agli oggetti e in genere mantiene le coppie (nome, oggetto) in un database.
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- RPC (Remote Procedure Call), descritto, nome del database del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471422"
---
# <a name="the-rpc-name-service-database"></a>Il database del servizio nome RPC

Un servizio nome è un servizio che esegue il mapping dei nomi agli oggetti e in genere mantiene le coppie (nome, oggetto) in un database. In genere, il nome è un nome logico che è facile per gli utenti ricordare e usare. Ad esempio, un servizio nome consente a un utente di utilizzare il nome logico "condivisione StampanteLaser". Il servizio nome esegue il mapping di questo nome al nome specifico della rete utilizzato dal server di stampa.

Per utilizzare una spiegazione semplificata, il servizio nome RPC esegue il mapping di un nome a un handle di associazione e mantiene i mapping (nome, handle di associazione) nel database del servizio del nome RPC. Il servizio nome RPC consente alle applicazioni client di utilizzare un nome logico anziché una sequenza di protocollo e un indirizzo di rete specifici. L'utilizzo del nome logico consente agli amministratori di rete di installare e configurare l'applicazione distribuita in modo più semplice.

Una voce del database del servizio nome RPC ha uno dei seguenti attributi: **Server**, **gruppo** o **profilo**. Nell'implementazione Microsoft, le voci possono avere un solo attributo, pertanto queste voci sono note anche come voci del server, voci di gruppo e voci del profilo.

La voce server è costituita da UUID di interfaccia, UUID di oggetti (necessario quando il server implementa più punti di ingresso), indirizzo di rete, sequenza di protocollo ed eventuali informazioni sull'endpoint associate a endpoint noti. Quando viene utilizzato un endpoint dinamico, le informazioni sull'endpoint vengono mantenute nel database della mappa endpoint anziché nel database del servizio dei nomi e l'endpoint viene risolto in modo analogo a qualsiasi altro endpoint dinamico. Le voci del server sono gestite da funzioni che iniziano con il prefisso "RpcNsBinding".

La voce di gruppo può contenere voci del server o altre voci di gruppo. Le voci di gruppo sono gestite da funzioni che iniziano con il prefisso "RpcNsGroup".

La voce del profilo può contenere voci di profilo, gruppo o server. Le voci del profilo sono gestite dalle funzioni che iniziano con il prefisso "RpcNsProfile".

In questa sezione viene presentata una panoramica del nome del database del servizio negli argomenti seguenti:

-   [Linee guida sull'applicazione di servizio nome](name-service-application-guidelines.md)
-   [Panoramica dell'immissione del nome del servizio](an-overview-of-the-name-service-entry.md)
-   [Criteri per le voci del servizio dei nomi](criteria-for-name-service-entries.md)
-   [Pulizia voce servizio nome](name-service-entry-cleanup.md)
-   [Cosa accade durante una query](what-happens-during-a-query.md)
-   [Uso di Microsoft Locator](using-microsoft-locator.md)
-   [Uso del servizio directory delle celle (CDS)](using-the-cell-directory-service-cds-.md)
-   [Sintassi del nome](name-syntax.md)

 

 




