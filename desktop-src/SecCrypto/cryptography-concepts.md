---
description: 'La comunicazione protetta su reti non sicure comporta in genere tre aree principali di interesse: privacy, autenticazione e integrità.'
ms.assetid: bfffe87d-8392-4b4a-8bbc-01b9c13fba47
title: Concetti relativi alla crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aad1528032c20c5492a98798f8a175ca331e462
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306453"
---
# <a name="cryptography-concepts"></a>Concetti relativi alla crittografia

La comunicazione protetta su reti non sicure comporta in genere tre aree principali di interesse: [privacy](#privacy), [autenticazione](#authentication)e [integrità](#integrity). Microsoft Cryptography API ([*CryptoAPI*](../secgloss/c-gly.md)) è un set di funzioni, interfacce e strumenti che possono essere utilizzati dalle applicazioni per migliorare la sicurezza in queste aree.

Oltre alle funzionalità per la privacy, l'autenticazione e l'integrità, [*CryptoAPI*](../secgloss/c-gly.md) fornisce anche:

-   Codifica dei messaggi nel form [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN. 1).
-   Decodifica dei messaggi ASN. 1.
-   Gestione di raccolte di [*certificati*](../secgloss/c-gly.md) negli [*archivi certificati*](../secgloss/c-gly.md).
-   Uso di [*elenchi di certificati attendibili*](../secgloss/c-gly.md) e catene di certificati per la verifica della validità dei certificati.

## <a name="privacy"></a>Privacy

Per ottenere la privacy, gli utenti devono impedire a tutti gli utenti, ad eccezione del destinatario previsto, di leggere un messaggio. Il miglioramento della probabilità di privacy comporta in genere l'uso di una forma di [*crittografia*](../secgloss/c-gly.md). Le tecniche di crittografia vengono utilizzate per crittografare i messaggi (Scramble) prima che i messaggi vengano archiviati o trasmessi.

La crittografia dei dati trasforma il [*testo non crittografato*](../secgloss/p-gly.md) in [*testo*](../secgloss/c-gly.md)crittografato. I dati da crittografare possono essere testo [*ASCII*](../secgloss/a-gly.md) , un file di database o qualsiasi altro dato. In questa documentazione, il termine [*messaggio*](../secgloss/m-gly.md) viene usato per fare riferimento a qualsiasi dato, il testo non crittografato fa riferimento a dati che non sono stati crittografati e il *testo* crittografato fa riferimento ai dati crittografati. Un valido sistema di crittografia dei dati rende difficile trasformare i dati crittografati di nuovo in testo non crittografato senza una chiave privata.

I dati crittografati possono essere archiviati in supporti non protetti o trasmessi tramite una rete non protetta. Successivamente, è possibile decrittografare i dati nel formato originale. Questo processo è illustrato nella figura seguente.

![conservazione della privacy durante la crittografia e la decrittografia](images/capi01.png)

Quando i dati vengono crittografati, il messaggio e una chiave di [*crittografia*](../secgloss/e-gly.md) vengono passati all'algoritmo di crittografia. Per decrittografare i dati, il testo crittografato e una chiave di [*decrittografia*](../secgloss/d-gly.md) vengono passati all'algoritmo di decrittografia. La crittografia e la decrittografia possono essere eseguite utilizzando una singola chiave in un processo denominato crittografia simmetrica.

Le chiavi usate per decrittografare un messaggio devono essere mantenute come segrete e più sicure possibile e devono essere trasmesse ad altri utenti usando tecniche di miglioramento della sicurezza. Questa operazione viene descritta ulteriormente in [crittografia e decrittografia dei dati](data-encryption-and-decryption.md). La sfida principale è la limitazione corretta dell'accesso alla chiave di decrittografia perché chiunque lo possiede sarà in grado di decrittografare tutti i messaggi crittografati con la chiave di crittografia corrispondente.

Per risolvere gli obiettivi di privacy indicati, gli sviluppatori possono usare [*CryptoAPI*](../secgloss/c-gly.md) per crittografare e firmare digitalmente i dati in modo flessibile, garantendo al tempo stesso la protezione dei dati riservati della chiave privata dell'utente.

[*CryptoAPI*](../secgloss/c-gly.md) fornisce le seguenti aree di funzionalità per eseguire le attività di crittografia/decrittografia, firma dei messaggi e archiviazione delle chiavi:

-   [Funzioni di crittografia di base](cryptography-functions.md)
-   [Funzioni di messaggio semplificate](cryptography-functions.md)
-   [Funzioni di messaggio di basso livello](cryptography-functions.md)

## <a name="authentication"></a>Authentication

Le comunicazioni sicure richiedono che le persone che comunicano conoscano l'identità degli utenti con cui comunicano. L'autenticazione è il processo di verifica dell'identità di una persona o di un'entità.

Ad esempio, nella vita quotidiana, la documentazione fisica, spesso denominata credenziali, viene usata per verificare l'identità di un utente. Quando si incassa un assegno, l'utente che incassa il controllo può richiedere la visualizzazione della licenza di un driver. La licenza del driver è un documento fisico che aumenta la fiducia dell'esercente nell'identità della persona che incassa il controllo. In questo caso, la persona che incassa il controllo Considera attendibile che lo stato che emette la licenza ha verificato adeguatamente l'identità del titolare della licenza.

I passaporti forniscono un altro esempio. Un ufficiale doganale esamina un passaporto e lo accetta come prova che una persona è quella che dichiara di essere. Il governo ufficiale considera attendibile che il governo abbia eseguito un lavoro adeguato per identificare il titolare del passaporto prima di emettere il passaporto. In entrambi gli esempi, esiste un livello di attendibilità nell'emittente del documento fisico.

L'autenticazione comporta inoltre la verifica che i dati ricevuti siano i dati inviati. Se la parte A invia un messaggio all'entità B, l'entità B deve essere in grado di dimostrare che il messaggio ricevuto è il messaggio che l'entità A è stata inviata e non un messaggio sostituito da tale messaggio. Per fornire questo tipo di autenticazione, [*CryptoAPI*](../secgloss/c-gly.md) fornisce funzioni per la firma dei dati e la verifica delle firme mediante coppie di chiavi pubbliche/private.

Poiché le comunicazioni su una rete di computer hanno luogo senza contatto fisico tra i comunicatori, la verifica dell'identità dipende spesso da credenziali che possono essere inviate e ricevute in rete. Tali credenziali devono essere emesse da un'autorità emittente attendibile di credenziali. I certificati digitali, comunemente noti come certificati, sono solo credenziali di questo tipo. Sono un modo per verificare l'identità e ottenere l'autenticazione in una rete di computer.

Un certificato digitale è una credenziale rilasciata da un'organizzazione o da un'entità attendibile denominata autorità di certificazione (CA). Questa credenziale contiene una chiave pubblica (vedere [coppie di chiavi pubbliche/private](public-private-key-pairs.md)) e i dati che identificano l'oggetto del certificato. Un certificato viene emesso da un'autorità di certificazione solo dopo che l'autorità di certificazione ha verificato l'identità del soggetto del certificato e ha confermato che la chiave pubblica inclusa nel certificato appartiene a tale oggetto.

La comunicazione tra un'autorità di certificazione e un richiedente del certificato può essere eseguita dal richiedente che trasporta fisicamente le informazioni necessarie, eventualmente archiviate in un disco floppy, alla CA. Tuttavia, la comunicazione viene in genere eseguita con un messaggio firmato inviato in rete. La CA USA spesso un'applicazione attendibile denominata server dei certificati per rilasciare i certificati.

[*CryptoAPI*](../secgloss/c-gly.md) supporta l'autenticazione tramite l'utilizzo di certificati digitali, con funzioni di codifica/decodifica dei certificati e funzioni di [*archivio certificati*](../secgloss/c-gly.md) .

Per ulteriori informazioni sulla verifica dell'identità e l'autenticazione tramite l'utilizzo di certificati, vedere la pagina relativa ai [certificati digitali](digital-certificates.md).

## <a name="integrity"></a>Integrità

Tutti i dati inviati su un supporto non sicuro possono essere modificati per errore o per finalità. Nel mondo reale, le guarnizioni vengono usate per fornire e dimostrare l'integrità. Un bottle di aspirina, ad esempio, può essere incluso in una confezione a prova di manomissione che presenta un sigillo non interrotto per dimostrare che nulla è stato inserito nel pacchetto dopo che il pacchetto ha lasciato il produttore.

Allo stesso modo, un destinatario di dati deve essere in grado di verificare l'identità del mittente dei dati e assicurarsi che i dati ricevuti siano esattamente i dati inviati. ovvero, non è stata manomessa. La definizione dell' [*integrità*](../secgloss/i-gly.md) dei dati ricevuti viene spesso eseguita inviando non solo i dati originali, ma anche un messaggio di verifica, denominato [*hash*](../secgloss/h-gly.md), su tali dati. Sia i dati che il messaggio di verifica possono essere inviati con una [*firma digitale*](../secgloss/d-gly.md) che dimostra l'origine di entrambi.

L'integrità viene fornita in CryptoAPI per mezzo dell'uso di [firme digitali](digital-signatures.md) e [hash di dati](data-hashes.md).

[*CryptoAPI*](../secgloss/c-gly.md) supporta l'integrità tramite l'utilizzo di funzioni di messaggio per la firma dei dati e la verifica delle firme digitali.

 

 
