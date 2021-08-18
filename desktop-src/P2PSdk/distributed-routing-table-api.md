---
description: L'API DRT (Distributed Routing Table) consente alle applicazioni di pubblicare e risolvere chiavi numeriche in una rete peer.
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: Routing distribuito API Tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adabac4e2e885a7ac635daf5de2dfbacc94dafd4972a6b35f1f4649c3428e92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011609"
---
# <a name="distributed-routing-table-api"></a>Routing distribuito API Tabella

L'API DRT (Distributed Routing Table) consente alle applicazioni di pubblicare e risolvere chiavi numeriche in una rete peer.

Un'applicazione che usa DRT può eseguire le operazioni seguenti:

-   Creare tabelle di routing distribuito specifiche dell'applicazione.
-   Registrare le chiavi e associarle agli indirizzi IP e ai dati dell'applicazione.
-   Cercare le chiavi e recuperare gli indirizzi IP e i dati dell'applicazione associati. Questa funzionalità può essere usata per costruire DHT (Distributed Hash Table), sistemi di risoluzione dei nomi serverless e reti mesh sovrapposte di molte topologie.

> [!Note]  
> Gli amministratori e gli utenti delle applicazioni abilitate per DRT devono rendere noti agli utenti finali delle proprie applicazioni le informazioni pubblicate. I server Microsoft non vengono utilizzati da questa tecnologia e le informazioni non vengono inviate a Microsoft.

 

La documentazione fornita per questa API è suddivisa in tre sezioni.



| Sezione                                                                                | Descrizione                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Informazioni sulle tabelle di routing distribuito](about-distributed-routing-tables.md)               | Informazioni che dettaglino il ciclo di vita e le modifiche di stato dell'API DRT.<br/>                                    |
| [Uso del routing distribuito API Tabella](using-the-distributed-routing-table-api.md) | Informazioni che dettaglino l'utilizzo generale dell'API DRT.<br/>                                                   |
| [Informazioni di riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md) | Informazioni dettagliate sulle funzioni, le strutture di dati e le costanti enumerate che costituiscono l'API DRT.<br/> |



 

 

 




