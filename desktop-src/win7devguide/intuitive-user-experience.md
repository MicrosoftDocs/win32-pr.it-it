---
title: Esperienza utente intuitiva
description: Per la prima volta, Windows 7 consente agli sviluppatori e agli utenti finali di controllare i propri computer toccando lo schermo.
ms.assetid: cf5be4d6-4284-43e3-86ba-293c4513b477
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76576883186a77c53256dad7f011b75a7e260ae2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729479"
---
# <a name="intuitive-user-experience"></a>Esperienza utente intuitiva

Per la prima volta, Windows 7 consente agli sviluppatori e agli utenti finali di controllare i propri computer toccando lo schermo. Le funzionalità di tocco e multitocco forniscono agli utenti un modo naturale e intuitivo per interagire con i PC. La piattaforma per sviluppatori include le API di movimento di alto livello, oltre ai messaggi touch di basso livello e alle API di input touch. Gli elementi dell'interfaccia utente di livello superiore, ad esempio il menu *Start* e la *barra delle applicazioni*, presentano destinazioni maggiori rispetto alle versioni precedenti di Windows, semplificando la selezione con un dito invece che con il mouse. Viene fornito un feedback visivo per toccare e toccare doppio. Esplora risorse e Windows Internet Explorer 8 sono compatibili e sono facilmente integrabili con le applicazioni di Windows 7.

## <a name="multi-touch-gestures-and-manipulation-and-inertia-apis"></a>Movimenti multitocco e API di manipolazione e inerzia

Con Windows 7 è stato migliorato il supporto per tocco e movimento, consentendo agli sviluppatori di creare in modo rapido e semplice esperienze di applicazione univoche che vanno oltre il semplice puntatore del mouse, facendo clic e trascinando. Le nuove API multitocco supportano movimenti avanzati, ad esempio Pan, zoom e ruota. Tutti i movimenti forniscono commenti visivi diretti e interagiscono con il contenuto sottostante in modo naturale e intuitivo. Ad esempio, un movimento di zoom centra la visualizzazione in corrispondenza della posizione del movimento. Le API di input touch di livello inferiore sono disponibili anche per la definizione di movimenti personalizzati e per esperienze avanzate di risposta tocco. Windows 7 fornisce una piattaforma di sviluppo che offre agli sviluppatori gli strumenti necessari per sviluppare applicazioni creative per i dispositivi di input multitocco, elaborando l'input dell'utente da dispositivi multitocco e migliorando l'interfaccia utente. Il risultato è un ambiente più intuitivo, che consente le innovazioni nell'interazione con i PC.

Windows 7 fornisce inoltre supporto della piattaforma per la manipolazione degli oggetti e l'elaborazione dell'inerzia. Un set completo di funzioni di manipolazione consente di estendere, ridimensionare o ruotare più oggetti simultaneamente e con una granularità molto fine. Ad esempio, è possibile ritagliare, ridimensionare e ruotare più fotografie digitali in una singola sessione usando movimenti basati sul tocco.

Windows 7 include API di inerzia che simulano l'inerzia quando gli oggetti vengono spostati e funzionano in modo manuale con le API di manipolazione. Ad esempio, in un'applicazione Photo è possibile utilizzare le API di manipolazione per consentire agli utenti di ruotare, ridimensionare e spostare le foto. Analogamente, se un utente "lancia" una foto, le API di inerzia forniscono un'interazione naturale e consentono alla foto di costarsi a un punto di interruzione o di rimbalzo sui bordi della finestra dell'applicazione. (Vedere [Guida alla programmazione per Windows Touch](../wintouch/programming-guide.md) e [Windows Touch: risorse per sviluppatori](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch)).

## <a name="single-finger-panning"></a>Panoramica di Single-Finger

In molte applicazioni comuni, le funzionalità di tocco sono più utili per la navigazione rispetto alla selezione di testo. Con le API Touch estese, l'applicazione di uno sviluppatore può scegliere di abilitare la panoramica anziché il trascinamento. Se, ad esempio, è stata creata un'applicazione che utilizza movimenti multitocco per gli utenti che giocano musica, è possibile consentire a tali utenti di scorrere semplicemente un dito verso l'alto o verso il basso per modificare il volume, modificare le canzoni o scaricare un file. Non è necessario alcuno scorrimento.

Windows 7 offre innumerevoli opportunità per gli sviluppatori interessati alla creazione di applicazioni per PC di nuova generazione. Si tratta di un'operazione che consente di controllare le barre di scorrimento e di implementare la semantica di panoramica. Le applicazioni ricevono anche un set più completo di eventi e commenti e suggerimenti per il controllo personalizzato dei movimenti rispetto alle versioni precedenti di Windows. Vedere [miglioramento dell'esperienza di panoramica Single-Finger](../wintouch/improving-the-single-finger-panning-experience.md).

## <a name="raw-touch-input-data"></a>Dati di input tocco non elaborati

In Windows 7 le nuove esperienze di tocco sono abilitate dai modelli di interazione che accedono ai messaggi di input touch di livello inferiore e forniscono risposte personalizzate a combinazioni di messaggi di tocco. La piattaforma supporta la ricezione di dati di input di tocco non elaborati per scenari come le applicazioni di disegno multitocco e i movimenti personalizzati all'interno di un'applicazione. Puoi usare il supporto della piattaforma per toccare o creare esperienze personalizzate originali. Vedere la pagina relativa al [ \_ messaggio WM touch](../wintouch/wm-touchdown.md).

 

 