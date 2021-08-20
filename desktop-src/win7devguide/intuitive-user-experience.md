---
title: Esperienza utente intuitiva
description: Per la prima volta, Windows 7 consente agli sviluppatori e agli utenti finali di controllare i computer toccando lo schermo.
ms.assetid: cf5be4d6-4284-43e3-86ba-293c4513b477
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14157066225fcf0cbec6b3df5a263be606419eed1ce4fc799d07da6379035ced
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032038"
---
# <a name="intuitive-user-experience"></a>Esperienza utente intuitiva

Per la prima volta, Windows 7 consente agli sviluppatori e agli utenti finali di controllare i computer toccando lo schermo. Le funzionalità touch e multitocchetto offrono agli utenti un modo naturale e intuitivo per interagire con i PC. La piattaforma per sviluppatori include API di movimento di alto livello, nonché messaggi di tocco di basso livello e API di input tocco. Gli elementi dell'interfaccia utente di primo livello, ad esempio il menu *Start* e la barra delle *applicazioni,* hanno destinazioni più grandi rispetto alle versioni precedenti di Windows, semplificando la selezione con un dito anziché con il mouse. Il feedback visivo viene fornito per il tocco e il doppio tocco. Windows Explorer e Windows Internet Explorer 8 sono entrambi touch friendly e facilmente integrati con Windows 7.

## <a name="multi-touch-gestures-and-manipulation-and-inertia-apis"></a>Movimenti multitocchetto e API di manipolazione e inerzia

Windows 7 offre un supporto migliorato per tocco e movimenti, che consente agli sviluppatori di creare in modo semplice e rapido esperienze di applicazione univoche che vanno oltre il semplice puntamento del mouse, la selezione e il trascinamento. Le nuove API multitocchetto supportano movimenti rich, ad esempio panoramica, zoom e rotazione. Tutti i movimenti forniscono feedback visivo diretto e interagiscono con il contenuto sottostante in modo naturale e intuitivo. Ad esempio, un movimento di zoom centra la visualizzazione in corrispondenza della posizione del movimento. Le API di input tocco di livello inferiore sono disponibili anche per la definizione di movimenti personalizzati e le esperienze avanzate di risposta tocco. Windows 7 offre una piattaforma di sviluppo che offre agli sviluppatori gli strumenti necessari per sviluppare applicazioni creative per dispositivi di input multitocchetto, elaborando l'input utente da dispositivi multitocchetto e migliorando l'interfaccia utente. Il risultato sono ambienti più intuitivi, che consentono innovazioni nell'interazione con i PC.

Windows 7 offre anche il supporto della piattaforma per la manipolazione degli oggetti e l'elaborazione dell'inerzia. Un set dettagliato di funzioni di manipolazione consente di estendere, ridimensionare o ruotare più oggetti contemporaneamente e con una granularità molto fine. Ad esempio, più fotografie digitali possono essere ritagliate, ridimensionate e ruotate in una singola sessione usando movimenti basati sul tocco.

Windows 7 include API di inerzia che simulano l'inerzia quando gli oggetti vengono spostati, lavorando mano nella mano con le API di manipolazione. In un'applicazione di foto, ad esempio, è possibile usare le API di manipolazione per consentire agli utenti di ruotare, ridimensionare e spostare le foto. Analogamente, se un utente "butta" una foto, le API di inerzia forniscono un'interazione naturale e consentono alla foto di fermarsi o di buttarsi oltre i bordi della finestra dell'applicazione. (Vedere [Windows touch programming guide (Guida](../wintouch/programming-guide.md) alla programmazione di Touch) Windows Touch: Developer Resources (Guida per programmatori touch e Windows [Touch: risorse per sviluppatori).](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch)

## <a name="single-finger-panning"></a>Single-Finger panoramica

In molte applicazioni comuni, le funzionalità di tocco sono più utili per la navigazione che per la selezione del testo. Con le API di tocco estese, l'applicazione di uno sviluppatore può scegliere di abilitare la panoramica anziché il trascinamento. Ad esempio, se è stata creata un'applicazione che usa movimenti multitocchetto per gli utenti che riproduceno musica, è possibile consentire a questi utenti di scorrere semplicemente un dito verso l'alto o verso il basso per regolare il volume, modificare i brani o scaricare un file. Non è necessario scorrere.

Windows 7 offre infinite opportunità agli sviluppatori interessati a creare applicazioni per PC di nuova generazione. Soprattutto, esegue il lavoro necessario per verificare la presenza di barre di scorrimento e implementare la semantica di panoramica. Le applicazioni ricevono anche un set più completo di eventi e feedback per il controllo personalizzato dei movimenti rispetto alle versioni precedenti di Windows. Vedere [Improving the Single-Finger Panning Experience](../wintouch/improving-the-single-finger-panning-experience.md).)

## <a name="raw-touch-input-data"></a>Dati di input tocco non elaborati

In Windows 7, le nuove esperienze di tocco sono abilitate da modelli di interazione che accedono ai messaggi di input tocco di livello inferiore e forniscono risposte personalizzate a combinazioni di messaggi tocco. La piattaforma supporta la ricezione di dati di input tocco non elaborati per scenari come applicazioni di disegno multitocchetto e movimenti personalizzati all'interno di un'applicazione. È possibile usare il supporto della piattaforma per il tocco o creare esperienze originali multitocchetto. Vedere [WM \_ TOUCH Message](../wintouch/wm-touchdown.md).

 

 