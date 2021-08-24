---
title: Migrazione del driver di grafica Windows 10
description: Windows 10 Media e Windows 10, come il suo predecessore, Windows 8.1, non dispone di driver di grafica di terze parti nel kit multimediale Windows o "In Box".
ms.assetid: E6240CF0-5A65-4A66-98AE-856C783EB320
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b1703210318f55dad3e50f4dcdd7e143434275b7ef3b41203f41792262a53e5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882711"
---
# <a name="graphics-driver-migration-to-windows-10"></a>Migrazione del driver di grafica Windows 10

Windows 10 Media e Windows 10, come il suo predecessore, Windows 8.1, non dispone di driver di grafica di terze parti nel kit multimediale Windows o "In Box". Viene invece effettuato il provisioning dei driver di grafica per un'ampia gamma di dispositivi in WU, che consente ai fornitori di hardware di aggiornare i driver senza richiedere una modifica all'immagine del sistema operativo. Inoltre, non viene eseguita la migrazione dei driver esistenti a Windows 10 durante un aggiornamento del sistema operativo a Windows 10 da Windows 7, Windows 8 o Windows 8.1. Ciò influisce anche sugli aggiornamenti da Windows Server 2012.

## <a name="upgrades-and-installation"></a>Aggiornamenti e installazione

Per gli aggiornamenti e le nuove installazioni, i driver di grafica devono essere ottenuti da Windows Update (WU) o dal sito Web IHV/OEM per l'hardware pertinente. È richiesta una connessione a Internet. I driver in WU vengono inseriti nella configurazione del sistema operativo da Aggiornamento dinamico quando un utente aggiorna il sistema Windows 7 o Windows 8.x a Windows 10.

> [!Note]  
> Questo non si applica ai sistemi che Windows preinstallato, ad esempio i computer pre-installati acquistati in un negozio al dettaglio. Questi sistemi hanno già i driver di grafica installati dall'OEM. L'OEM potrebbe anche fornire un DVD (per la nuova installazione del sistema operativo) che include i driver.

 

Dopo l'aggiornamento a Windows 10, gli utenti potrebbero scoprire che non sono installati driver di grafica nel PC. Ciò può essere dovuto a una serie di motivi:

-   L'utente ha scelto di eseguire un'installazione pulita, ad esempio non un aggiornamento.
-   L'utente ha selezionato l'opzione per verificare la disponibilità di aggiornamenti durante l'aggiornamento, ovvero ha disabilitato in modo efficace l'aggiornamento dinamico.
-   La connessione Internet non funzionava durante l'aggiornamento.
-   L'installazione del driver non è riuscita.

Dopo un'installazione pulita del sistema operativo, non saranno presenti driver di grafica nel PC finché il client WU non viene eseguito automaticamente e non scarica i driver applicabili. Nel frattempo il PC eseguirà l'adattatore microsoft basic display (MSBDA), che ha funzionalità limitate, ad esempio nessun supporto per più monitor e l'utente potrebbe anche avere prestazioni scarse rispetto a un driver hardware, ad esempio la velocità dei fotogrammi lenta o lo sfregamento nella riproduzione video.

## <a name="manifestations"></a>Manifestazioni

Per i PC meno recenti (in genere creati prima di Windows 7), è possibile che non siano presenti driver per Windows 10 in WU perché le schede grafiche hanno raggiunto end-of-life (EOL) e non sono più supportate dai fornitori di hardware. Anche i sistemi che eseguono Windows 7 o 8.x potrebbero essere stati aggiornati da un sistema operativo precedente e potrebbero avere schede grafiche EOL.

I PC più recenti potrebbero non avere driver disponibili perché la scheda grafica è stata trasferita da un computer meno recente, ad esempio durante un aggiornamento hardware. Ciò si verifica più spesso per i computer con più schede grafiche in cui l'utente conservava una scheda grafica precedente quando acquistava un nuovo computer per usare più schermi.

Un'altra possibilità per una piccola percentuale di computer è che Windows update abbia solo driver di "copertura". Si tratta di driver generici che non dispongono di personalizzazioni OEM. Un utente a cui viene recapitato uno di questi driver dopo l'aggiornamento a Windows 10 potrebbe vedere che alcune funzionalità sono mancanti, ad esempio i tasti funzione per controllare la luminosità dello schermo non funzionano più.

## <a name="mitigations"></a>Soluzioni di prevenzione

-   I driver di grafica appropriati devono essere recapitati da DU durante il processo di aggiornamento o da WU subito dopo il completamento dell'aggiornamento. Gli OEM devono assicurarsi che i driver di grafica appropriati siano inclusi nelle immagini di sistema usate per l'installazione di Windows 10 nei computer.
-   Dopo un aggiornamento, l'utente può controllare in modo esplicito Impostazioni Windows per i driver, anche se questo non \\ deve essere necessario. Gli utenti che forzano un controllo durante l'installazione automatica di un driver in background potrebbero visualizzare un errore di installazione del driver se l'installazione automatica viene completata per prima. Questo messaggio può essere ignorato.
-   Gli utenti che intendono eseguire un'installazione pulita di Windows 10 devono ottenere i driver pertinenti prima di installare o fare affidamento su Windows Update per fornire i driver in un secondo momento, nel qual caso devono assicurarsi che la connessione Internet funzioni.
-   Per i computer che ricevono un driver di copertura non esiste alcuna mitigazione per la funzionalità mancante. Tuttavia, questo problema deve verificarsi solo nei casi in cui il fornitore dell'hardware non gestisce più i driver, ad esempio i computer di diversi anni.

> [!Note]  
> Per i sistemi con un singolo schermo, ad esempio un computer portatile, molti utenti trovano che MSBDA è accettabile e non si nota la mancanza di un driver hardware. In questo caso non è necessaria alcuna mitigazione.

 

## <a name="solutions"></a>Soluzioni

È fondamentale che gli IHV e gli OEM carichino i driver Windows 10 grafica in WU per qualsiasi hardware che intendono supportare.

Gli utenti devono lasciare selezionata l'opzione "Controlla aggiornamenti" (impostazione predefinita) durante l'aggiornamento. A seconda della velocità della connessione di rete e del carico sui server WU, ciò può significare che i driver non vengono installati fino al completamento della configurazione guidata e all'accesso dell'utente per la prima volta. Nel frattempo, l'utente potrebbe notare alcune funzionalità limitate o prestazioni ridotte.

Gli utenti devono assicurarsi che la connessione Internet funzioni prima di avviare un aggiornamento anche se vengono aggiornati usando supporti (DVD o flash drive).

-   Se il PC è connesso a Internet, i driver appropriati devono essere scaricati e installati automaticamente. L'utente non deve eseguire alcuna azione.
-   Se il PC non è connesso a Internet, i driver devono essere scaricati dal sito Web IHV o OEM usando un computer connesso a Internet. trasferito al computer di destinazione usando un'unità flash o un CD/DVD; e quindi installati manualmente.

 

 




