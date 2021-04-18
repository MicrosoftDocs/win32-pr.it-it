---
description: Concetti relativi ai componenti in coda COM+
ms.assetid: ff11e251-311f-4612-8f0d-a4cbc5b4d872
title: Concetti relativi ai componenti in coda COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d1a8983e84d817e402454392ce95fc2b07a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304637"
---
# <a name="com-queued-components-concepts"></a>Concetti relativi ai componenti in coda COM+

In base ai servizi di [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) , il servizio componenti in coda com+ fornisce un modo semplice per richiamare ed eseguire i componenti in modo asincrono. L'elaborazione può verificarsi senza considerare la disponibilità o l'accessibilità del mittente o del destinatario.

In termini COM, una *coda* è un'area di archiviazione che consente di salvare i messaggi per un successivo recupero. L'accodamento fornisce un meccanismo per la comunicazione senza connessione. Ovvero il mittente e il destinatario non sono connessi direttamente e comunicano solo tramite le code. L'accodamento consente di mantenere le informazioni finché il ricevitore non è pronto per ottenerlo. Il mittente e il destinatario comunicano indirettamente in modo che ciascuno possa funzionare in modo indipendente, non interessato dall'altro.

In passato, una conoscenza approfondita del marshalling era necessaria per accodare, inviare e ricevere messaggi asincroni. Ora, usando le chiamate ai metodi facilmente comprensibili e usate dagli sviluppatori di componenti, il servizio componenti accodati COM+ esegue automaticamente il marshalling dei dati sotto forma di messaggio di Accodamento messaggi. Poiché il servizio componenti in coda offre supporto incorporato per le transazioni, uno stato incoerente non può compromettere i dati se si verifica un errore del server.

Negli argomenti seguenti di questa sezione sono contenute informazioni di base sulla progettazione e la scrittura di componenti in coda.



| Argomento                                                                           | Descrizione                                                                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Vantaggi dell'elaborazione in coda](benefits-of-queued-processing.md)<br/>   | Vengono descritti i vantaggi della programmazione con i componenti in coda COM+.<br/>                                         |
| [Architettura dei componenti in coda](queued-components-architecture.md)<br/> | Descrive l'architettura del servizio COM+ Queued Components.<br/>                                          |
| [Accodamento messaggi transazionale](transactional-message-queuing.md)<br/>   | Viene descritto il modo in cui le transazioni vengono gestite dal servizio componenti in coda COM+.<br/>                              |
| [Sicurezza dei componenti in coda](queued-components-security.md)<br/>         | Descrive le opzioni dei criteri per l'autenticazione dei messaggi client e le relative implicazioni.<br/>                 |
| [Sviluppo di componenti in coda](developing-queued-components.md)<br/>     | Descrive le considerazioni di programmazione per la scrittura di componenti accodabili.<br/>                                     |
| [Errori dei componenti in coda](queued-components-errors.md)<br/>             | Vengono descritti i tipi di errori più comuni che possono verificarsi quando si utilizza il servizio componenti in coda COM+.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività dei componenti in coda COM+](com--queued-components-tasks.md)
</dt> </dl>

 

 




