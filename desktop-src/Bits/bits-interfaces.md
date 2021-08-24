---
title: Interfacce BITS
description: Usare le interfacce Servizio trasferimento intelligente in background (BITS) seguenti per trasferire i file e monitorare i processi all'interno della coda di trasferimento.
ms.assetid: 72668c9b-e6f3-4f3f-9d4b-50d930d1889d
ms.topic: article
ms.date: 01/08/2019
ms.openlocfilehash: 0edd4229e76a85767689427cfccd6cb38aa11c0e54345053ce10d1a99fc1fde8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529071"
---
# <a name="bits-interfaces"></a>Interfacce BITS

Usare le interfacce Servizio trasferimento intelligente in background (BITS) seguenti per trasferire i file e [monitorare i processi all'interno](using-bits.md) della coda di trasferimento.

| Interfaccia | Descrizione |
|-|-|
| [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) | I client implementano [**l'interfaccia IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) per ricevere la notifica del completamento, della modifica o dell'errore di un processo. |
| [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) | I client implementano [**l'interfaccia IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) per ricevere la notifica del completamento del download di un file. |
| [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) | I client implementano [**l'interfaccia IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) per ricevere la notifica del completamento del download degli intervalli di un file. |
| [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) | Recupera i dettagli di un errore del processo. |
| [**IBackgroundCopyFile**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyfile) | Recupera i nomi file locali e remoti di una richiesta di trasferimento file nel processo e il relativo stato di avanzamento. |
| [**IBackgroundCopyFile2**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2) | Specifica un nuovo nome remoto per il file e recupera l'elenco di intervalli da scaricare. |
| [**IBackgroundCopyFile3**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3) | Convalida il file in modo che i peer possano richiedere il contenuto e recuperare il nome del file temporaneo. |
| [**IBackgroundCopyFile4**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4) | Recupera le statistiche di download per peer e server di origine. |
| [**IBackgroundCopyFile5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5) | Fornisce metodi get e set di proprietà generiche per le proprietà BackgroundCopyFile. |
| [**IBackgroundCopyFile6**](/windows/desktop/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6) | Ottiene o imposta le proprietà generiche dei trasferimenti di file BITS. |
| [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) | Aggiunge file al processo, imposta il livello di priorità del processo, determina lo stato del processo e avvia e arresta il processo. |
| [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) | Recupera i dati di risposta da un processo di caricamento, determina lo stato di avanzamento del trasferimento dei dati di risposta al client, richiede l'esecuzione della riga di comando e fornisce le credenziali per un proxy e un server remoto. |
| [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3) | Scarica gli intervalli di un file, modifica il prefisso di un nome di file remoto e mantiene le informazioni sul proprietario e sull'ACL con il file. |
| [**IBackgroundCopyJob4**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4) | Abilita il peer caching, limita il tempo di download ed esamina le caratteristiche del token utente. |
| [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) | Esegue query o imposta diversi comportamenti facoltativi di un processo. |
| [**IBackgroundCopyJobHttpOptions**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) | Specifica i certificati client per l'autenticazione client basata su certificati e le intestazioni personalizzate per le richieste HTTP. |
| [**IBackgroundCopyJobHttpOptions2**](/windows/desktop/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2) | Utilizzare questa interfaccia per recuperare e/o eseguire l'override del metodo HTTP utilizzato per un trasferimento BITS. |
| [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) | Crea processi di trasferimento, recupera un oggetto enumeratore dei processi nella coda e recupera singoli processi dalla coda. |
| [**IBitsPeer**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeer) | Ottiene informazioni su un peer nel vicinato. |
| [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) | Gestire il pool di peer da cui è possibile scaricare il contenuto. |
| [**IBitsPeerCacheRecord**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacherecord) | Ottiene informazioni su un file nella cache. |
| [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) | Associa e gestisce una coppia di token di sicurezza per un processo di Servizio trasferimento intelligente in background (BITS). |
| [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) | Enumera i file nel processo. |
| [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) | Enumera i processi nella coda di trasferimento. |
| [**IEnumBitsPeerCacheRecords**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords) | Enumera i record della cache. |
| [**IEnumBitsPeers**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeers) | Enumera l'elenco di peer individuati da BITS. |



 

 

 




