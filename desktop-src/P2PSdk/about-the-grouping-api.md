---
description: L'API di raggruppamento peer combina la tecnologia dell'API del provider di spazi dei nomi PNRP e dell'API Graphing.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: Informazioni sull'API di raggruppamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b4cd1b2783d7605f9198e3c8171177e70b531944a8f2f707def5750dd6d985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612795"
---
# <a name="about-the-grouping-api"></a>Informazioni sull'API di raggruppamento

L'API di raggruppamento peer combina la tecnologia dell'API provider dello spazio dei nomi [PNRP](pnrp-namespace-provider-api.md) e [dell'API Graphing.](graphing-api.md) Il raggruppamento aggiunge i due tipi di tecnologia seguenti:

-   Livello di multiplexing che consente a più applicazioni di usare un grafo, una porta e un database di record.
-   Sicurezza che garantisce che solo i peer invitati a un gruppo possano essere uniti e connettersi per tutta la durata di un gruppo.

Il raggruppamento offre un approccio semplice e accessibile alla rete peer grazie al flusso di chiamate semplice e alla messaggistica sicura. Questa API usa PNRP per l'individuazione dei gruppi e un provider di sicurezza standard basato su PKI anziché richiedere a uno sviluppatore di implementarne uno. Tuttavia, se l'applicazione richiede una maggiore flessibilità in termini di opzioni di sicurezza, è consigliabile usare [l'API Graphing.](about-the-graphing-api.md)

La tabella seguente identifica gli argomenti di questa sezione dell'API di raggruppamento:

| Argomento                                                                | Descrizione                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Come usare i gruppi](how-to-work-with-groups.md)               | Descrive il flusso di chiamata in un'applicazione di raggruppamento di peer dall'avvio all'arresto.         |
| [Funzionamento della sicurezza dei gruppi](how-group-security-works.md)             | Viene descritto come vengono protetti l'appartenenza a gruppi peer e gli scambi di dati.                      |
| [Invito di un peer a un gruppo](inviting-a-peer-to-a-group.md)         | Descrive il processo con cui i peer vengono invitati e aggiunti a un gruppo di peer.              |
| [Come eseguire Connessione a un gruppo di peer](how-to-connect-to-a-peer-group.md) | Viene descritto il modo in cui un peer si connette e interagisce con un gruppo di peer.                        |
| [Gestione dei record di gruppo](managing-group-records.md)                 | Descrive i record del gruppo peer e come gestirli come membri e come amministratore. |



 

> [!Note]  
> Le applicazioni che usano l'API di raggruppamento in un ambiente con un firewall richiedono gruppi di eccezioni che coprono la porta specifica dell'applicazione, nonché la porta "3587-TCP" per l'API di raggruppamento e la porta "3540-UDP" per PNRP. Questi gruppi di eccezioni devono essere abilitati ogni volta che l'applicazione è in esecuzione.

 

 

 



