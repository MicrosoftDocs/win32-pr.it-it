---
title: Interazione con IMAPi
description: Nei passaggi seguenti viene descritta una tipica interazione tra un'applicazione e IMAPi.
ms.assetid: e57a86c4-7e27-40cf-a9c1-081b3f20d9d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e68bee24cfe0724ed14d439b0789f5023338853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955541"
---
# <a name="interacting-with-imapi"></a>Interazione con IMAPi

Nei passaggi seguenti viene descritta una tipica interazione tra un'applicazione e IMAPi.

1.  Creare un'istanza di **MSDiscMasterObj** (usando **CoCreateInstance**, i puntatori intelligenti da un'importazione e così via) e richiedere l'interfaccia [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) .
2.  Acquisire l'accesso a IMAPi chiamando [**IDiscMaster:: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open). Se la chiamata ha esito positivo, l'applicazione ha accesso completo a tutte le interfacce e i metodi implementati in **MSDiscMasterObj**.
3.  Recuperare l'enumeratore del formato master del disco utilizzando [**EnumDiscMasterFormats**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscmasterformats). Enumerare il set di formati supportato dall'oggetto master del disco, quindi selezionare il formato attivo. I formati restituiti dall'enumeratore sono IID delle interfacce per [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) e [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster).
4.  Recuperare l'enumeratore del registratore di dischi utilizzando [**EnumDiscRecorders**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscrecorders). Enumerare l'elenco di masterizzatori di dischi supportati (specifici del formato attivo), quindi selezionare il registratore attivo. L'interfaccia [**IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) rappresenta un dispositivo fisico.
5.  Usare [**IDiscMaster::P rogressadvise**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-progressadvise) per la registrazione per i callback di stato.
6.  Usare l'interfaccia per il formato selezionato per compilare il contenuto. Il contenuto viene compilato in modo incrementale, quindi è possibile aggiungere tracce o contenuto di cartelle a un disco. La creazione di questo contenuto è detta *staging di un'immagine*. Il contenuto dell'immagine di gestione temporanea non può essere eliminato in modo incrementale (non è possibile rimuovere una traccia aggiunta), ma è possibile cancellare il contenuto di un'immagine di gestione temporanea in modo che sia possibile avviare di nuovo la gestione temporanea. Usare [**IDiscMaster:: ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) per riavviare la gestione temporanea.

**Per audio:  **

1.  Usare [**IRedbookDiscMaster:: CreateAudioTrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-createaudiotrack) per indicare che è in corso l'avvio di una nuova traccia audio sul disco.
2.  Usare [**IRedbookDiscMaster:: AddAudioTrackBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-addaudiotrackblocks) per aggiungere dati audio non elaborati a una traccia. L'applicazione può usare [**GetAvailableAudioTrackBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getavailableaudiotrackblocks), [**GetTotalAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-gettotalaudioblocks)e [**GetUsedAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getusedaudioblocks) per recuperare le informazioni statistiche.
3.  Usare [**IRedbookDiscMaster:: CloseAudioTrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-closeaudiotrack) per chiudere una traccia audio.
4.  Ripetere i passaggi 1-3 fino a esaurire lo spazio o tutte le tracce audio sono state scritte.

**Per i dati:  **

1.  Usare [**IJolietDiscMaster:: AddData**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-adddata) per aggiungere il contenuto di una cartella all'immagine. Gli elementi all'interno di una cartella vengono inseriti nella radice del file di immagine. Usare [**GetTotalDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-gettotaldatablocks) e [**GetUsedDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-getuseddatablocks) per recuperare le informazioni statistiche.
2.  Ripetere il passaggio precedente fino a esaurire lo spazio o tutti i dati aggiunti.

**Per tutti i dischi:  **

1.  Usare [**IDiscMaster:: RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) per registrare il disco.
2.  Chiudere la sessione IMAPi usando [**IDiscMaster:: Close**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-close). Chiudendo la sessione si cancella il contenuto del Stash del disco.

 

 




