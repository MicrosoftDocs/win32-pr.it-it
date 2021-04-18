---
title: Migrazione di driver grafici a Windows 10
description: Windows 10 media e Windows 10, come il suo predecessore, Windows 8.1 non hanno driver grafici di terze parti in Windows Media Kit o "in box".
ms.assetid: E6240CF0-5A65-4A66-98AE-856C783EB320
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a23d8ae341172223955fcc781f95b7615bcfc867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298713"
---
# <a name="graphics-driver-migration-to-windows-10"></a>Migrazione di driver grafici a Windows 10

Windows 10 media e Windows 10, come il suo predecessore, Windows 8.1 non hanno driver grafici di terze parti in Windows Media Kit o "in box". Al contrario, viene eseguito il provisioning dei driver grafici per un'ampia gamma di dispositivi in WU, che consente ai fornitori di hardware di aggiornare i driver senza richiedere una modifica all'immagine del sistema operativo. Inoltre, i driver esistenti non vengono migrati a Windows 10 durante un aggiornamento del sistema operativo a Windows 10 da Windows 7, Windows 8 o Windows 8.1. Questa operazione influisca anche sugli aggiornamenti da Windows Server 2012.

## <a name="upgrades-and-installation"></a>Aggiornamenti e installazione

Per gli aggiornamenti e le nuove installazioni, i driver grafici devono essere ottenuti da Windows Update (WU) o dal sito Web IHV/OEM per l'hardware pertinente. È richiesta una connessione a Internet. I driver in WU vengono inseriti nella configurazione del sistema operativo tramite aggiornamento dinamico (DU) quando un utente aggiorna il sistema Windows 7 o Windows 8. x a Windows 10.

> [!Note]  
> Questa operazione non si applica ai sistemi dotati di Windows preinstallati, ad esempio computer fuori programma acquistati in un negozio al dettaglio. Questi sistemi hanno già i driver grafici installati dall'OEM. L'OEM potrebbe anche fornire un DVD (per reinstallare il sistema operativo) che include i driver.

 

Dopo l'aggiornamento a Windows 10, gli utenti potrebbero scoprire che nel PC non sono installati driver grafici. Ciò può essere dovuto a una serie di motivi:

-   L'utente ha scelto di eseguire un'installazione pulita, ovvero non un aggiornamento.
-   L'utente ha selezionato l'opzione per verificare la disponibilità di aggiornamenti durante l'aggiornamento, ovvero l'aggiornamento dinamico (DU) disabilitato in modo efficace.
-   La connessione Internet non funzionava durante l'aggiornamento.
-   Installazione del driver non riuscita.

Dopo un'installazione pulita del sistema operativo, non saranno presenti driver grafici nel PC finché il client WU non verrà eseguito automaticamente e scaricherà i driver applicabili. Nel frattempo il PC eseguirà Microsoft Basic Display Adapter (MSBDA), che ha funzionalità limitate, ad esempio nessun supporto per più monitor, e l'utente potrebbe anche riscontrare una riduzione delle prestazioni rispetto a un driver hardware, ad esempio una frequenza di fotogrammi rallentata o un'operazione di strappo alla riproduzione video.

## <a name="manifestations"></a>Manifestazioni

Per i PC meno recenti (in genere compilati prima di Windows 7), è possibile che non esistano driver per Windows 10 in WU perché le schede grafiche hanno raggiunto il termine del ciclo di vita (EOL) e non sono più supportate dai fornitori di hardware. Anche i sistemi che eseguono Windows 7 o 8. x potrebbero essere stati aggiornati da un sistema operativo precedente e potrebbero avere schede grafiche EOL.

I PC più recenti potrebbero non avere driver disponibili perché la scheda grafica è stata trasferita da un computer precedente, ad esempio durante un aggiornamento hardware. Questa situazione si verifica più spesso per i computer con più schede grafiche in cui l'utente ha mantenuto una vecchia scheda grafica durante l'acquisto di una nuova macchina per poter usare più schermi.

Un'altra possibilità per una piccola percentuale di computer è che Windows Update ha solo driver di "code coverage". Si tratta di driver generici privi di personalizzazioni OEM. Un utente che viene recapitato uno di questi driver dopo l'aggiornamento a Windows 10 potrebbe verificare che alcune funzionalità siano mancanti, ad esempio i tasti funzione per il controllo della luminosità dello schermo non funzionano più.

## <a name="mitigations"></a>Soluzioni di prevenzione

-   I driver grafici appropriati devono essere distribuiti da DU durante il processo di aggiornamento o da WU subito dopo il completamento dell'aggiornamento. Gli OEM devono garantire che i driver grafici appropriati siano inclusi nelle immagini di sistema utilizzate per l'installazione in fabbrica di Windows 10 nei propri computer.
-   Dopo un aggiornamento, l'utente può controllare in modo esplicito le impostazioni \\ Windows Update per i driver anche se questa operazione non è necessaria. Se l'installazione automatica viene completata per prima, gli utenti che forzano un controllo mentre un driver viene installato automaticamente in background potrebbero riscontrare un errore di installazione del driver. Questo messaggio può essere ignorato.
-   Gli utenti che intendono eseguire un'installazione pulita di Windows 10 devono ottenere i driver appropriati prima di installare o utilizzare Windows Update per fornire i driver in un secondo momento, nel qual caso devono assicurarsi che la connessione Internet sia funzionante.
-   Per i computer che ricevono un driver di code coverage non esiste alcuna attenuazione per la funzionalità mancante. Questa operazione dovrebbe tuttavia verificarsi solo nei casi in cui il fornitore dell'hardware non gestisce più i driver, ad esempio computer che Risaleno a diversi anni fa.

> [!Note]  
> Per i sistemi con un unico schermo, ad esempio un portatile, molti utenti ritengono che MSBDA sia accettabile e non si noti la mancanza di un driver hardware. In questo caso non è necessaria alcuna mitigazione.

 

## <a name="solutions"></a>Soluzioni

È fondamentale che IHV e gli OEM carichino i driver grafici Windows 10 in WU per qualsiasi hardware che intende supportare.

Quando si esegue l'aggiornamento, gli utenti devono lasciare selezionato "Verifica disponibilità aggiornamenti" (impostazione predefinita). A seconda della velocità della connessione di rete e del carico sui server WU, questo può significare che i driver non vengono installati finché non viene completata la configurazione guidata e l'utente ha effettuato l'accesso per la prima volta. Nel frattempo, l'utente potrebbe notare alcune funzionalità limitate o scarse prestazioni.

Gli utenti devono assicurarsi che la connessione a Internet funzioni prima di avviare un aggiornamento anche se si sta eseguendo l'aggiornamento con supporti (DVD o unità flash).

-   Se il PC è connesso a Internet, è necessario scaricare e installare automaticamente i driver appropriati. L'utente non deve eseguire alcuna azione.
-   Se il PC non è connesso a Internet, i driver devono essere scaricati dal sito Web IHV o OEM utilizzando un computer connesso a Internet. trasferiti nel computer di destinazione tramite un'unità flash o un CD/DVD; e quindi installati manualmente.

 

 




