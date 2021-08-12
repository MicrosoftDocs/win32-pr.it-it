---
title: Linee guida relative alle prestazioni
description: Linee guida per lo sviluppo di applicazioni con prestazioni molto Servizi Desktop remoto ambiente.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97a8211f12e4a89c5dfb309bb4e3c0f998159738b46185aeb5dcee7a5cd29f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605313"
---
# <a name="performance-guidelines"></a>Linee guida relative alle prestazioni

Le sezioni seguenti forniscono linee guida per lo sviluppo di applicazioni con prestazioni Servizi Desktop remoto ambiente.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Effetti grafici](graphic-effects.md)
</dt> <dd>

Elenco di funzionalità che devono essere disabilitate durante l'esecuzione come sessione remota in un Servizi Desktop remoto locale.

</dd> <dt>

[Linee guida per le attività in background in Servizi Desktop remoto](background-tasks.md)
</dt> <dd>

Per ottimizzare la disponibilità della CPU per tutti gli utenti, disabilitare le attività in background durante l'esecuzione in un ambiente Servizi Desktop remoto o creare attività in background efficienti che non richiedono un uso intensivo delle risorse.

</dd> <dt>

[Utilizzo di thread](thread-usage.md)
</dt> <dd>

È consigliabile ottimizzare e bilanciare l'utilizzo dei thread dell'applicazione per un ambiente multiutente Servizi Desktop remoto multiprocessore.

</dd> <dt>

[Rilevamento dell'Servizi Desktop remoto locale](detecting-the-terminal-services-environment.md)
</dt> <dd>

Per ottimizzare le prestazioni, è consigliabile che le applicazioni rilevino se sono in esecuzione in una Servizi Desktop remoto client.

</dd> </dl>

Controllare la presenza di perdite di memoria nell'applicazione e risolvere eventuali problemi. Naturalmente si tratta di un buon consiglio per qualsiasi applicazione, ma in un ambiente Servizi Desktop remoto un'applicazione può essere eseguita più volte da più utenti, in modo da ingrandire rapidamente l'effetto di una perdita di memoria.

Le animazioni, le immagini di grandi dimensioni, l'audio e altri servizi a elevato utilizzo di larghezza di banda devono essere configurabili. Quando questi servizi non sono la funzione primaria, possono essere disattivati per impostazione predefinita per le sessioni remote, ma abilitati quando una sessione è in esecuzione in locale o su una connessione a larghezza di banda elevata. Se lo scopo di un'applicazione è fornire servizi a larghezza di banda elevata, ad esempio trasmissioni video in streaming, il servizio non deve essere disattivato per impostazione predefinita.

 

 




