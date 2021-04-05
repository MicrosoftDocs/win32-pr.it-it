---
title: Interfacce BITS
description: Utilizzare le seguenti interfacce di Servizio trasferimento intelligente in background (BITS) per trasferire i file e monitorare i processi nella coda di trasferimento.
ms.assetid: 72668c9b-e6f3-4f3f-9d4b-50d930d1889d
ms.topic: article
ms.date: 01/08/2019
ms.openlocfilehash: fc95d4aea6d6d74ff2952cf2ef686fbaa1049732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955176"
---
# <a name="bits-interfaces"></a>Interfacce BITS

Utilizzare le seguenti interfacce di Servizio trasferimento intelligente in background (BITS) per [trasferire i file e monitorare i processi](using-bits.md) nella coda di trasferimento.

| Interfaccia | Descrizione |
|-|-|
| [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) | I client implementano l'interfaccia [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) per ricevere una notifica che indica che un processo è stato completato, è stato modificato o è in errore. |
| [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) | I client implementano l'interfaccia [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) per ricevere una notifica di completamento del download di un file. |
| [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) | I client implementano l'interfaccia [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) per ricevere una notifica per cui è stato completato il download degli intervalli di un file. |
| [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) | Recupera i dettagli di un errore del processo. |
| [**IBackgroundCopyFile**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyfile) | Recupera i nomi di file locali e remoti di una richiesta di trasferimento file nel processo e il relativo stato di avanzamento. |
| [**IBackgroundCopyFile2**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2) | Specifica un nuovo nome remoto per il file e recupera l'elenco di intervalli da scaricare. |
| [**IBackgroundCopyFile3**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3) | Convalida il file in modo che i peer possano richiedere il contenuto e recuperare il nome del file temporaneo. |
| [**IBackgroundCopyFile4**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4) | Recupera le statistiche di download per i peer e i server di origine. |
| [**IBackgroundCopyFile5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5) | Fornisce i metodi get e set di proprietà generiche per le proprietà BackgroundCopyFile. |
| [**IBackgroundCopyFile6**](/windows/desktop/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6) | Ottiene o imposta le proprietà generiche dei trasferimenti di file BITS. |
| [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) | Aggiunge file al processo, imposta il livello di priorità del processo, determina lo stato del processo e avvia e arresta il processo. |
| [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) | Recupera i dati di risposta da un processo di caricamento, determina lo stato di avanzamento del trasferimento dei dati di risposta al client, richiede l'esecuzione della riga di comando e fornisce le credenziali per un proxy e un server remoto. |
| [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3) | Scarica gli intervalli di un file, modifica il prefisso di un nome di file remoto e mantiene le informazioni sul proprietario e sull'ACL con il file. |
| [**IBackgroundCopyJob4**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4) | Consente di abilitare la memorizzazione nella cache peer, limitare il tempo di download ed esaminare le caratteristiche del token utente. |
| [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) | Esegue una query o imposta diversi comportamenti facoltativi di un processo. |
| [**IBackgroundCopyJobHttpOptions**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) | Specifica i certificati client per l'autenticazione client basata su certificato e le intestazioni personalizzate per le richieste HTTP. |
| [**IBackgroundCopyJobHttpOptions2**](/windows/desktop/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2) | Usare questa interfaccia per recuperare e/o per eseguire l'override del metodo HTTP usato per un trasferimento BITS. |
| [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) | Crea processi di trasferimento, recupera un oggetto enumeratore di processi nella coda e recupera singoli processi dalla coda. |
| [**IBitsPeer**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeer) | Ottiene informazioni su un peer nel quartiere. |
| [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) | Consente di gestire il pool di peer da cui è possibile scaricare il contenuto. |
| [**IBitsPeerCacheRecord**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacherecord) | Ottiene informazioni su un file nella cache. |
| [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) | Associa e gestisce una coppia di token di sicurezza per un processo di trasferimento Servizio trasferimento intelligente in background (BITS). |
| [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) | Enumera i file nel processo. |
| [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) | Enumera i processi nella coda di trasferimento. |
| [**IEnumBitsPeerCacheRecords**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords) | Enumera i record della cache. |
| [**IEnumBitsPeers**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeers) | Enumera l'elenco di peer individuati da BITS. |



 

 

 




