---
description: Istruzioni per l'utilizzo dell'API di gestione autorizzazioni per creare un archivio criteri di autorizzazione nello script.
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: Creazione di un archivio criteri di autorizzazione nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0cb35e8e998f95e99193d1dc5e8a74838b7efc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130655"
---
# <a name="creating-an-authorization-policy-store-in-script"></a>Creazione di un archivio criteri di autorizzazione nello script

Creare un criterio di autorizzazione prima o durante l'installazione di un'applicazione.

Quando si usa l'API di gestione autorizzazioni per creare un criterio di autorizzazione, seguire le istruzioni fornite negli argomenti seguenti.



| Argomento                                                                                                                  | Descrizione                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creazione di un oggetto archivio criteri di autorizzazione nello script](creating-an-authorization-policy-store-object-in-script.md) | Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di sicurezza di un'applicazione o di un gruppo di applicazioni.                                                                                                                                       |
| [Creazione di un oggetto applicazione nello script](creating-an-application-object-in-script.md)                               | Per ogni applicazione che usa un archivio criteri di autorizzazione, è necessario creare un oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) e salvarlo in un archivio criteri.                                                                                                |
| [Definizione di operazioni nello script](defining-operations-in-script.md)                                                     | Un'operazione è una funzione o un metodo di basso livello di un'applicazione.                                                                                                                                                                                              |
| [Raggruppamento di operazioni in attività nello script](grouping-operations-into-tasks-in-script.md)                               | Un'attività è un'azione di alto livello che gli utenti di un'applicazione devono completare. Le attività sono costituite da operazioni, ovvero funzioni di basso livello e metodi dell'applicazione.                                                                                    |
| [Raggruppamento di attività in ruoli nello script](grouping-tasks-into-roles-in-script.md)                                         | Un ruolo rappresenta una categoria di utenti e le attività che gli utenti sono autorizzati a eseguire.                                                                                                                                                                     |
| [Definizione di gruppi di utenti nello script](defining-groups-of-users-in-script.md)                                           | Un oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) rappresenta un gruppo di utenti. I ruoli possono quindi essere assegnati a questo gruppo di utenti collettivamente. Un oggetto **IAzApplicationGroup** può includere anche altri oggetti **IAzApplicationGroup** come membri. |
| [Aggiunta di utenti a un gruppo di applicazioni nello script](adding-users-to-an-application-group-in-script.md)                   | Un gruppo di applicazioni è un gruppo di utenti e gruppi di utenti. Un gruppo di applicazioni può contenere altri gruppi di applicazioni, quindi i gruppi di utenti possono essere annidati. Un gruppo di applicazioni è rappresentato da un oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .    |



 

 

 



