---
title: Interazione con IMAPI
description: I passaggi seguenti descrivono un'interazione tipica tra un'applicazione e IMAPI.
ms.assetid: e57a86c4-7e27-40cf-a9c1-081b3f20d9d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab97d1a9d76d1e82dab64fb777ef5207d3d47560b2a889981c698ab78e3622b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726991"
---
# <a name="interacting-with-imapi"></a>Interazione con IMAPI

I passaggi seguenti descrivono un'interazione tipica tra un'applicazione e IMAPI.

1.  Creare un'istanza di **MSDiscMasterObj** (usando **CoCreateInstance**, puntatori intelligenti da un'importazione e così via) e richiedere [**l'interfaccia IDiscMaster.**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster)
2.  Acquisire l'accesso a IMAPI chiamando [**IDiscMaster::Open.**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) Se questa chiamata ha esito positivo, l'applicazione ha accesso completo a tutte le interfacce e a tutti i metodi implementati in **MSDiscMasterObj**.
3.  Recuperare l'enumeratore del formato master del disco [**usando EnumDiscMasterFormats.**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscmasterformats) Enumerare il set di formati supportati dall'oggetto master del disco, quindi selezionare il formato attivo. I formati restituiti dall'enumeratore sono gli IID delle interfacce per [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) [**e IRedbookDiscMaster.**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster)
4.  Recuperare l'enumeratore del registratore di dischi [**usando EnumDiscRecorders.**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscrecorders) Enumerare l'elenco dei registratori di dischi supportati (specifici del formato attivo), quindi selezionare il registratore attivo. [**L'interfaccia IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) rappresenta un dispositivo fisico.
5.  Usare [**IDiscMaster::P rogressAdvise per**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-progressadvise) eseguire la registrazione per i callback di stato.
6.  Usare l'interfaccia per il formato selezionato per creare il contenuto. Il contenuto viene compilato in modo incrementale, in modo che le tracce o il contenuto della cartella possano essere aggiunti a un disco singolo. La creazione di questo contenuto è detta *staging di un'immagine.* Il contenuto dell'immagine di staging non può essere eliminato in modo incrementale (non è possibile rimuovere una traccia aggiunta), ma è possibile cancellare il contenuto di un'immagine di staging in modo che la gestione temporanea possa essere avviata di nuovo. Usare [**IDiscMaster::ClearFormatContent per**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) riavviare la gestione temporanea.

**Per l'audio: **

1.  Usare [**IRedbookDiscMaster::CreateAudioTrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-createaudiotrack) per indicare che è in corso l'avvio di una nuova traccia audio sul disco.
2.  Usare [**IRedbookDiscMaster::AddAudioTrackBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-addaudiotrackblocks) per aggiungere dati audio non elaborati a una traccia. L'applicazione può [**usare GetAvailableAudioTrackBlocks,**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getavailableaudiotrackblocks) [**GetTotalAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-gettotalaudioblocks)e [**GetUsedAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getusedaudioblocks) per recuperare informazioni statistiche.
3.  Usare [**IRedbookDiscMaster::CloseAudioTrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-closeaudiotrack) per chiudere una traccia audio.
4.  Ripetere i passaggi da 1 a 3 fino a quando lo spazio non è insufficiente o non sono state scritte tutte le tracce audio.

**Per i dati: **

1.  Usare [**IJolietDiscMaster::AddData**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-adddata) per aggiungere il contenuto di una cartella all'immagine. Gli elementi all'interno di una cartella vengono inseriti nella radice del file di immagine. Usare [**GetTotalDataBlocks e**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-gettotaldatablocks) [**GetUsedDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-getuseddatablocks) per recuperare informazioni statistiche.
2.  Ripetere il passaggio precedente fino a quando non sono stati aggiunti tutti i dati o lo spazio disponibile.

**Per tutti i dischi: **

1.  Usare [**IDiscMaster::RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) per registrare il disco.
2.  Chiudere la sessione IMAPI [**usando IDiscMaster::Close**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-close). La chiusura della sessione cancella il contenuto dello stash del disco.

 

 




