---
description: Istruzioni per l'uso dell'API di gestione autorizzazioni per creare un archivio criteri di autorizzazione in C++.
ms.assetid: a350f25a-7cda-4879-82d1-151a3da7d8ec
title: Creazione di un archivio criteri di autorizzazione in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdff3ba26457510440c8d0e603bc993a4878281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130254"
---
# <a name="creating-an-authorization-policy-store-in-c"></a>Creazione di un archivio criteri di autorizzazione in C++

Creare un criterio di autorizzazione prima o durante l'installazione di un'applicazione.

Quando si usa l'API di gestione autorizzazioni per creare un criterio di autorizzazione, seguire le istruzioni fornite negli argomenti seguenti.



| Argomento                                                                                                            | Descrizione                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creazione di un oggetto archivio criteri di autorizzazione in C++](creating-an-authorization-policy-store-object-in-c--.md) | Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di sicurezza di un'applicazione o di un gruppo di applicazioni. Le informazioni includono le applicazioni, le operazioni, le attività, gli utenti e i gruppi di utenti associati allo Store.              |
| [Creazione di un oggetto applicazione in C++](creating-an-application-object-in-c--.md)                               | Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di autorizzazione per una o più applicazioni. Per ogni applicazione che usa l'archivio criteri, è necessario creare un oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) e salvarlo in un archivio criteri. |
| [Definizione di operazioni in C++](defining-operations-in-c--.md)                                                     | In Gestione autorizzazioni un'operazione è una funzione o un metodo di basso livello di un'applicazione.                                                                                                                                                               |
| [Raggruppamento di operazioni in attività in C++](grouping-operations-into-tasks-in-c--.md)                               | In Gestione autorizzazioni un'attività è un'azione di alto livello che gli utenti di un'applicazione devono completare. Le attività sono costituite da operazioni, ovvero funzioni di basso livello e metodi dell'applicazione.                                                     |
| [Raggruppamento di attività in ruoli in C++](grouping-tasks-into-roles-in-c--.md)                                         | In Gestione autorizzazioni, un ruolo rappresenta una categoria di utenti e le attività che gli utenti sono autorizzati a eseguire.                                                                                                                                      |
| [Definizione di gruppi di utenti in C++](defining-groups-of-users-in-c--.md)                                           | In Gestione autorizzazioni, un oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) rappresenta un gruppo di utenti. I ruoli possono quindi essere assegnati a questo gruppo di utenti collettivamente.                                                                       |
| [Aggiunta di utenti a un gruppo di applicazioni in C++](adding-users-to-an-application-group-in-c--.md)                   | In Gestione autorizzazioni, un gruppo di applicazioni è costituito da un gruppo di utenti e gruppi di utenti. Un gruppo di applicazioni può contenere altri gruppi di applicazioni, quindi i gruppi di utenti possono essere annidati.                                                                          |



 

 

 



