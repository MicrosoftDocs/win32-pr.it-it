---
title: Linee guida relative alle prestazioni
description: Linee guida per lo sviluppo di applicazioni che offrono prestazioni ottimali in un ambiente Servizi Desktop remoto.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea7ada6ee2b51943d47f39446d0b1bb3b7d6718
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396819"
---
# <a name="performance-guidelines"></a>Linee guida relative alle prestazioni

Nelle sezioni seguenti vengono fornite le linee guida per lo sviluppo di applicazioni con prestazioni ottimali in un ambiente Servizi Desktop remoto.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Effetti grafici](graphic-effects.md)
</dt> <dd>

Elenco di funzionalità che devono essere disabilitate durante l'esecuzione come sessione remota in un ambiente Servizi Desktop remoto.

</dd> <dt>

[Linee guida per le attività in background in Servizi Desktop remoto](background-tasks.md)
</dt> <dd>

Per ottimizzare la disponibilità della CPU per tutti gli utenti, disabilitare le attività in background durante l'esecuzione in un ambiente Servizi Desktop remoto o creare attività in background efficienti che non richiedono un uso intensivo delle risorse.

</dd> <dt>

[Utilizzo di thread](thread-usage.md)
</dt> <dd>

È consigliabile ottimizzare e bilanciare l'utilizzo dei thread dell'applicazione per un ambiente multiutente Servizi Desktop remoto multiprocessore.

</dd> <dt>

[Rilevamento dell'ambiente Servizi Desktop remoto](detecting-the-terminal-services-environment.md)
</dt> <dd>

Per ottimizzare le prestazioni, è consigliabile che le applicazioni rilevino se sono in esecuzione in una sessione client Servizi Desktop remoto.

</dd> </dl>

Verificare la presenza di perdite di memoria nell'applicazione e risolvere eventuali problemi. Naturalmente, questo è un valido Consiglio per qualsiasi applicazione, ma in un ambiente Servizi Desktop remoto un'applicazione può essere eseguita più volte da più utenti, in modo da ingrandire rapidamente l'effetto di una perdita di memoria.

È necessario configurare animazioni, immagini di grandi dimensioni, audio e altri servizi con utilizzo intensivo della larghezza di banda. Quando questi servizi non sono la funzione primaria, possono essere disattivati per impostazione predefinita per le sessioni remote, ma abilitati quando una sessione viene eseguita localmente o tramite una connessione a larghezza di banda elevata. Se lo scopo di un'applicazione è fornire servizi a larghezza di banda elevata, ad esempio trasmissioni video di streaming, non è necessario che il servizio sia disattivato per impostazione predefinita.

 

 




