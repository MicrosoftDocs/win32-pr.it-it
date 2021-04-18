---
description: Distribuzione per una comunicazione più veloce
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Distribuzione per una comunicazione più veloce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305326"
---
# <a name="deploying-for-faster-communication"></a>Distribuzione per una comunicazione più veloce

Le prestazioni sono un fattore fondamentale quando si distribuisce un'applicazione COM+ e il percorso del componente è la chiave per ottenere le migliori prestazioni da un'applicazione progettata correttamente.

Una volta diffusa questa situazione con le architetture di applicazioni scalabili, è possibile risolvere le prestazioni semplicemente spostando i componenti principali dell'applicazione in un hardware più rapido. Questa operazione si è rivelata non vera. I problemi di prestazioni non si verificano dalle prestazioni dei singoli componenti ma dai collegamenti che connettono i componenti.

Il fattore principale per il successo è la posizione. La vicinanza o la posizione fisica, il tempo, la capacità e lo scopo sono aspetti distinti della località che si applicano alla distribuzione di un'applicazione COM+, che influiscono sulle prestazioni.

Le prestazioni migliori si verificano quando i componenti e le risorse dell'applicazione vengono progettati e distribuiti in base alle richieste poste dal carico di lavoro dell'applicazione.

In generale, è consigliabile distribuire i componenti per ridurre al minimo le comunicazioni tra processi e in particolare tra computer e tra i componenti. Se la progettazione dell'applicazione è efficiente, le classi all'interno di un componente vengono raggruppate per utilizzo e funzione per ottimizzare le comunicazioni all'interno dei componenti. Per la distribuzione dei componenti, è necessario assicurarsi che i componenti si trovino logicamente per utilizzare le relazioni tra i componenti e per ridurre la quantità di messaggi di messaggistica tra i componenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione per la distribuzione](designing-for-deployment.md)
</dt> </dl>

 

 



