---
title: Panoramica dell'architettura dei servizi di Accodamento messaggi
description: I servizi di Accodamento messaggi (MSMQ) utilizzano un modello di sito/organizzazione. In genere, un sito è una posizione fisica, ad esempio un edificio. Un'azienda è costituita da uno o più siti e rappresenta un'organizzazione.
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2226c185d32cb628529b34ba33d5569bd51ac28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331367"
---
# <a name="overview-of-message-queuing-services-architecture"></a>Panoramica dell'architettura dei servizi di Accodamento messaggi

I servizi di Accodamento messaggi (MSMQ) utilizzano un modello di sito/organizzazione. In genere, un sito è una posizione fisica, ad esempio un edificio. Un'azienda è costituita da uno o più siti e rappresenta un'organizzazione.

Nel diagramma seguente viene illustrata l'architettura del servizio MSMQ.

![architettura MSMQ](images/msmq.png)

Il nucleo di MSMQ è il database Message Queue Information Service (MQIS), che viene eseguito sopra SQL Server. Un'azienda ha un singolo MQIS Master, denominato controller Enterprise primario. Ogni sito dispone di un proprio MQIS, denominato *controller del sito primario* e zero o più *controller del sito di backup*. Infine, vi sono i singoli computer client, ognuno dei quali ha un proprio gestore code, implementato come servizio. Il controller Enterprise primario può anche essere un controller del sito primario e qualsiasi controller può essere anche un client.

Le code di messaggi possono essere pubbliche o private. Le code pubbliche sono registrate in Active Directory e sono accessibili attraverso la rete. I messaggi in una coda pubblica vengono instradati in tutta l'organizzazione, sotto il controllo di MSMQ. I messaggi dell'applicazione client passano dal gestore delle code del client alla coda di destinazione, viaggiando tra i gestori delle code dei controller del sito.

Le code private vengono gestite dal gestore delle code locali e non sono registrate in Active Directory. L'ambito dei messaggi della coda privata è limitato al computer in cui si trovano.

 

 




