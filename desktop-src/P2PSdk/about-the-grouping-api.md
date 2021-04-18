---
description: L'API di raggruppamento peer combina la tecnologia dell'API del provider di spazio dei nomi PNRP e l'API Graphing.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: Informazioni sull'API di raggruppamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0c14e2731dd133afac32f2cd21905fa7e0c5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312305"
---
# <a name="about-the-grouping-api"></a>Informazioni sull'API di raggruppamento

L'API di raggruppamento peer combina la tecnologia dell' [API del provider di spazio dei nomi PNRP](pnrp-namespace-provider-api.md) e l' [API Graphing](graphing-api.md). Il raggruppamento aggiunge le due seguenti tecnologie:

-   Livello di multiplexing che consente a più applicazioni di utilizzare un grafo, una porta e un database di record.
-   Sicurezza che garantisce che solo i peer invitati a un gruppo possano entrare e connettersi per tutta la durata di un gruppo.

Il raggruppamento offre un approccio semplice e accessibile alla rete peer a causa del semplice flusso di chiamate e della messaggistica sicura. Questa API USA PNRP per l'individuazione del gruppo e un provider di sicurezza standard basato su PKI anziché richiedere a uno sviluppatore di implementarne uno. Tuttavia, se l'applicazione richiede una maggiore flessibilità in termini di opzioni di sicurezza, provare a usare l' [API Graphing](about-the-graphing-api.md).

La tabella seguente identifica gli argomenti in questa sezione relativa all'API di raggruppamento:

| Argomento                                                                | Descrizione                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Come lavorare con i gruppi](how-to-work-with-groups.md)               | Descrive il flusso di chiamate in un'applicazione di raggruppamento peer dall'avvio all'arresto.         |
| [Funzionamento della sicurezza del gruppo](how-group-security-works.md)             | Viene descritto come proteggere l'appartenenza al gruppo peer e gli scambi di dati.                      |
| [Invito di un peer a un gruppo](inviting-a-peer-to-a-group.md)         | Descrive il processo mediante il quale i peer vengono invitati e aggiunti a un gruppo peer.              |
| [Come connettersi a un gruppo peer](how-to-connect-to-a-peer-group.md) | Viene descritto il modo in cui un peer si connette e interagisce con un gruppo peer.                        |
| [Gestione dei record di gruppo](managing-group-records.md)                 | Vengono descritti i record del gruppo peer e viene illustrato come gestirli come membri e come amministratori. |



 

> [!Note]  
> Le applicazioni che usano l'API di raggruppamento in un ambiente con un firewall richiedono gruppi di eccezioni che coprono la porta specifica per l'applicazione, nonché la porta "3587-TCP" per l'API di raggruppamento e la porta "3540-UDP" per PNRP. Questi gruppi di eccezioni devono essere abilitati ogni volta che l'applicazione è in esecuzione.

 

 

 



