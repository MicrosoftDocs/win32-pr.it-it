---
description: L'API DRT (Distributed routing table) consente alle applicazioni di pubblicare e risolvere chiavi numeriche in una rete peer.
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: API Tabella di routing distribuito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f8c2b435e1c0c813fb279c40b9bbfa9afb6b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050025"
---
# <a name="distributed-routing-table-api"></a>API Tabella di routing distribuito

L'API DRT (Distributed routing table) consente alle applicazioni di pubblicare e risolvere chiavi numeriche in una rete peer.

Un'applicazione che utilizza DRT può eseguire le operazioni seguenti:

-   Creazione di tabelle di routing distribuite specifiche dell'applicazione.
-   Registrare le chiavi e associarle agli indirizzi IP e ai dati dell'applicazione.
-   Cercare le chiavi e recuperare gli indirizzi IP e i dati dell'applicazione associati. Questa funzionalità può essere utilizzata per costruire tabelle hash distribuite (DHT), sistemi di risoluzione dei nomi senza server e reti mesh sovrapposte di molte topologie.

> [!Note]  
> Gli amministratori e gli utenti di applicazioni abilitate per DRT devono fare in modo che gli utenti finali delle proprie applicazioni riconoscano le informazioni pubblicate. I server Microsoft non sono utilizzati da questa tecnologia e le informazioni non vengono inviate a Microsoft.

 

La documentazione fornita per questa API è divisa in tre sezioni.



| Sezione                                                                                | Descrizione                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Informazioni sulle tabelle di routing distribuite](about-distributed-routing-tables.md)               | Informazioni che descrivono in dettaglio il ciclo di vita e le modifiche di stato dell'API DRT.<br/>                                    |
| [Uso del API Tabella di routing distribuito](using-the-distributed-routing-table-api.md) | Informazioni che descrivono in dettaglio l'utilizzo generale dell'API DRT.<br/>                                                   |
| [Riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md) | Informazioni che descrivono in dettaglio le funzioni, le strutture di dati e le costanti enumerate che comprendono l'API DRT.<br/> |



 

 

 




