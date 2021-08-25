---
description: 'La comunicazione sicura su reti non sicure comporta in genere tre principali aree di interesse: privacy, autenticazione e integrità.'
ms.assetid: bfffe87d-8392-4b4a-8bbc-01b9c13fba47
title: Concetti relativi alla crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1909cf999bd5eb2f91bd5c7e0243b13969e692792c4ff32804e7c9a7d2940b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876157"
---
# <a name="cryptography-concepts"></a>Concetti relativi alla crittografia

La comunicazione sicura su reti non sicure comporta in genere tre principali aree di interesse: [privacy,](#privacy) [autenticazione](#authentication)e [integrità.](#integrity) L'API di crittografia Microsoft ([*CryptoAPI*](../secgloss/c-gly.md)) è un set di funzioni, interfacce e strumenti che le applicazioni possono usare per migliorare l'attendibilità della sicurezza in queste aree.

Oltre alle funzionalità per la privacy, l'autenticazione e l'integrità, [*CryptoAPI*](../secgloss/c-gly.md) offre anche:

-   Codifica dei messaggi nel formato ASN.1 [*(Abstract Syntax Notation One).*](../secgloss/a-gly.md)
-   Decodifica dei messaggi ASN.1.
-   Gestione di raccolte [*di certificati*](../secgloss/c-gly.md) negli [*archivi certificati*](../secgloss/c-gly.md).
-   Uso di [*elenchi di certificati attendibili*](../secgloss/c-gly.md) e catene di certificati per verificare la validità dei certificati.

## <a name="privacy"></a>Privacy

Per ottenere la privacy, gli utenti devono impedire a chiunque, ad eccezione del destinatario previsto, di leggere un messaggio. Il miglioramento della probabilità di privacy comporta in genere l'uso di una qualche forma [*di crittografia.*](../secgloss/c-gly.md) Le tecniche di crittografia vengono usate per crittografare (scramble) i messaggi prima che i messaggi siano archiviati o trasmessi.

La crittografia dei dati trasforma [*il testo non crittografato*](../secgloss/p-gly.md) [*in testo crittografato.*](../secgloss/c-gly.md) I dati da crittografare possono essere [*testo ASCII,*](../secgloss/a-gly.md) un file di database o qualsiasi altro dato. In questa documentazione [](../secgloss/m-gly.md) il termine messaggio viene usato per fare riferimento a qualsiasi dato, il  testo non crittografato fa riferimento a dati non crittografati e il testo crittografato fa riferimento ai dati crittografati. Un buon sistema di crittografia dei dati rende difficile trasformare i dati crittografati in testo non crittografato senza una chiave privata.

I dati crittografati possono essere archiviati su supporti non protetti o trasmessi tramite una rete non protetta. Successivamente, i dati possono essere decrittografati nel formato originale. Questo processo è illustrato nella figura seguente.

![contribuire a mantenere la privacy durante la crittografia e la decrittografia](images/capi01.png)

Quando i dati vengono crittografati, il messaggio e una chiave [*di*](../secgloss/e-gly.md) crittografia vengono passati all'algoritmo di crittografia. Per decrittografare i dati, il testo crittografato e una chiave [*di decrittografia*](../secgloss/d-gly.md) vengono passati all'algoritmo di decrittografia. La crittografia e la decrittografia possono essere eseguite usando una singola chiave in un processo denominato crittografia simmetrica.

Le chiavi usate per decrittografare un messaggio devono essere mantenute il più possibile segrete e sicure e devono essere trasmesse ad altri utenti usando tecniche di miglioramento della sicurezza. Questo argomento è descritto più avanti in [Crittografia dei dati e decrittografia.](data-encryption-and-decryption.md) La sfida principale consiste nel limitare correttamente l'accesso alla chiave di decrittografia perché chiunque la possieda sarà in grado di decrittografare tutti i messaggi crittografati con la chiave di crittografia corrispondente.

Per raggiungere gli obiettivi dichiarati della privacy, gli sviluppatori possono usare [*CryptoAPI*](../secgloss/c-gly.md) per crittografare e firmare digitalmente i dati in modo flessibile, consentendo al tempo stesso di fornire protezione per i dati sensibili della chiave privata dell'utente.

[*CryptoAPI*](../secgloss/c-gly.md) offre le seguenti aree di funzionalità per eseguire le attività di crittografia/decrittografia, firma dei messaggi e archiviazione delle chiavi:

-   [Funzioni di crittografia di base](cryptography-functions.md)
-   [Funzioni dei messaggi semplificate](cryptography-functions.md)
-   [Funzioni di messaggi di basso livello](cryptography-functions.md)

## <a name="authentication"></a>Autenticazione

Le comunicazioni protette richiedono che gli utenti che comunicano sappiano l'identità di coloro con cui comunicano. L'autenticazione è il processo di verifica dell'identità di una persona o di un'entità.

Ad esempio, nella vita quotidiana, la documentazione fisica, spesso denominata credenziali, viene usata per verificare l'identità di una persona. Quando un assegno viene incassato, la persona che lo incassa può chiedere di vedere la patente di guida. La patente di guida è un documento fisico che aumenta la fiducia dell'esercente nell'identità della persona che incassa l'assegno. In questo caso, la persona che incassa l'assegno considera attendibile che lo stato che emette la licenza sia adeguatamente verificato l'identità del titolare della licenza.

I passaporti forniscono un altro esempio. Un ufficiale delle dogane esamina un passaporto e lo accetta come prova che una persona è ciò che dice di essere. Il funzionario si fida che il governo abbia fatto un lavoro adeguato per identificare il titolare del passaporto prima di rilasciare il passaporto. In entrambi gli esempi esiste un livello di attendibilità nell'autorità emittente del documento fisico.

L'autenticazione comporta anche la verifica che i dati ricevuti siano i dati inviati. Se l'entità A invia un messaggio all'entità B, l'entità B deve essere in grado di dimostrare che il messaggio ricevuto è il messaggio inviato dall'entità A e non un messaggio sostituito da tale messaggio. Per fornire questa forma di autenticazione, [*CryptoAPI*](../secgloss/c-gly.md) fornisce funzioni per la firma dei dati e la verifica delle firme tramite coppie di chiavi pubblica/privata.

Poiché le comunicazioni su una rete di computer vengono esercite senza contatto fisico tra i comunicatori, la verifica dell'identità dipende spesso da una credenziale che può essere inviata e ricevuta tramite una rete. Tali credenziali devono essere rilasciate da un'autorità emittente attendibile delle credenziali. I certificati digitali, comunemente noti come certificati, sono solo credenziali di questo tipo. Sono un modo per verificare l'identità e ottenere l'autenticazione in una rete di computer.

Un certificato digitale è una credenziale emessa da un'organizzazione o un'entità attendibile denominata autorità di certificazione (CA). Questa credenziale contiene una chiave pubblica (vedere [Coppie di chiavi pubbliche/private)](public-private-key-pairs.md)e dati che identificano il soggetto del certificato. Un certificato viene rilasciato da una CA solo dopo che la CA ha verificato l'identità del soggetto del certificato e ha confermato che la chiave pubblica inclusa nel certificato appartiene a tale soggetto.

La comunicazione tra una CA e un richiedente di certificati può essere eseguita dal richiedente fisicamente trasportando le informazioni necessarie, magari archiviate su un disco floppy, alla CA. Tuttavia, la comunicazione viene in genere eseguita con un messaggio firmato inviato in rete. La CA usa spesso un'applicazione attendibile denominata server di certificati per emissione di certificati.

[*CryptoAPI*](../secgloss/c-gly.md) supporta l'autenticazione tramite l'uso di certificati digitali, con funzioni di codifica/decodifica dei certificati e funzioni [*di archivio*](../secgloss/c-gly.md) certificati.

Per altre informazioni sulla verifica dell'identità e l'autenticazione tramite l'uso di certificati, vedere [Certificati digitali](digital-certificates.md).

## <a name="integrity"></a>Integrità

Tutti i dati inviati tramite un supporto non sicuro possono essere modificati accidentalmente o di proposito. Nel mondo reale, i sigilli vengono usati per fornire e dimostrare l'integrità. Una bottiglia di aspirante, ad esempio, può essere inserita in imballaggi a prova di manomissione con un sigillo ininterrotta per dimostrare che non è stato inserito nulla nel pacchetto dopo che il pacchetto ha lasciato il produttore.

Allo stesso modo, un ricevitore di dati deve essere in grado di verificare l'identità del mittente dei dati e assicurarsi che i dati ricevuti siano esattamente i dati inviati; ciò significa che non è stato manomesso. La definizione [*dell'integrità*](../secgloss/i-gly.md) dei dati ricevuti viene spesso eseguita inviando non solo i dati originali, ma anche un messaggio di verifica, denominato [*hash*](../secgloss/h-gly.md), su questi dati. Sia i dati che il messaggio di verifica possono essere inviati con una [*firma digitale*](../secgloss/d-gly.md) che dimostra l'origine di entrambi.

L'integrità viene fornita in CryptoAPI tramite l'uso [di firme digitali](digital-signatures.md) e hash di [dati.](data-hashes.md)

[*CryptoAPI*](../secgloss/c-gly.md) supporta l'integrità tramite l'uso di funzioni di messaggio per firmare i dati e per verificare le firme digitali.

 

 
