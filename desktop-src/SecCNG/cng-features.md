---
description: CNG presenta le funzionalità seguenti.
ms.assetid: 400a2b6e-6bbe-4ba4-abde-a2f625007517
title: Funzionalità CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df40606a255adc90bd36540571979c1c34579611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305852"
---
# <a name="cng-features"></a>Funzionalità CNG

CNG presenta le funzionalità seguenti.

-   [Agilità crittografica](#cryptographic-agility)
-   [Certificazione e conformità](#certification-and-compliance)
-   [Supporto per Suite B](#suite-b-support)
-   [Supporto legacy](#legacy-support)
-   [Supporto della modalità kernel](#kernel-mode-support)
-   [Controllo](#auditing)
-   [Generatori di numeri casuali sostituibili](#replaceable-random-number-generators)
-   [Thread safety](#thread-safety)
-   [Modalità di funzionamento](#mode-of-operation)

## <a name="cryptographic-agility"></a>Agilità crittografica

Una delle proposte di valore chiave di CNG è l'agilità crittografica, definita anche agnosticismo crittografico. La conversione di un'implementazione di protocolli come [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) (SSL) o [*Transport Layer Security*](/windows/desktop/SecGloss/t-gly) (TLS), CMS (S/MIME), IPSec, Kerberos e così via, a CNG è stata tuttavia necessaria per rendere questa funzionalità preziosa. A livello di CNG, era necessario fornire la sostituzione e l'individuabilità per tutti i tipi di algoritmo (simmetrico, asimmetrico, funzioni hash), generazione di numeri casuali e altre funzioni di utilità. Le modifiche a livello di protocollo sono più significative perché, in molti casi, le API del protocollo necessarie per aggiungere la selezione degli algoritmi e altre opzioni di flessibilità che non esistono in precedenza.

CNG è disponibile per la prima volta in Windows Vista ed è posizionato per sostituire gli utilizzi esistenti di [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) in tutto lo stack di software Microsoft. Gli sviluppatori di terze parti troveranno numerose nuove funzionalità di CNG, tra cui:

-   Un nuovo sistema di configurazione della crittografia, che supporta una migliore agilità crittografica.
-   Astrazione più granulare per l'archiviazione delle chiavi (e la separazione dell'archiviazione dalle operazioni degli algoritmi).
-   Isolamento dei processi per le operazioni con chiavi a lungo termine.
-   Generatori di numeri casuali sostituibili.
-   Sollievo dalle restrizioni di firma dell'esportazione.
-   Thread safety in tutto lo stack.
-   API di crittografia in modalità kernel.

CNG include inoltre il supporto per tutti gli algoritmi di Suite B necessari, inclusa la [*crittografia a curva ellittica*](/windows/desktop/SecGloss/e-gly) (ecc). Le applicazioni CryptoAPI esistenti continueranno a funzionare quando CNG diventerà disponibile.

## <a name="certification-and-compliance"></a>Certificazione e conformità

CNG viene convalidato con FIPS (Federal Information Processing Standards) 140-2 ed è parte della destinazione della valutazione per la certificazione dei criteri comuni di Windows. CNG è stato progettato per essere utilizzato come componente in un sistema convalidato FIPS di livello 2.

CNG soddisfa i requisiti dei criteri comuni archiviando e usando chiavi di lunga durata in un processo protetto.

## <a name="suite-b-support"></a>Supporto per Suite B

Una funzionalità importante di CNG è il supporto per gli algoritmi di Suite B. Nel febbraio del 2005, National Security Agency (NSA) del Stati Uniti ha annunciato un set coordinato di crittografia simmetrica, un contratto di segreto asimmetrico (noto anche come scambio di chiave), una firma digitale e funzioni hash per l'uso da parte del governo degli Stati Uniti in futuro chiamato *Suite B*. Il NSA ha annunciato il fatto che le implementazioni di Suite B certificate possono e verranno usate per la protezione delle informazioni indicate come Top Secret, Secret e private, che in passato venivano descritte come sensibili, ma non classificate. Per questo motivo, Suite B supporto è molto importante per i fornitori di software applicativi e gli integratori di sistemi, nonché per Microsoft.

Tutti gli algoritmi di Suite B sono noti pubblicamente. Sono state sviluppate al di fuori dell'ambito della segretezza del governo, storicamente associata allo sviluppo di algoritmi di crittografia. In questo stesso intervallo di tempo, alcuni paesi e regioni europei hanno proposto anche le stesse Suite B requisiti per la protezione delle informazioni.

Suite B crittografia consiglia l'uso di Diffie-Hellman a curva ellittica (ECDH) in molti protocolli esistenti, ad esempio protocollo IKE (IKE, usato principalmente in IPsec), [*Transport Layer Security*](/windows/desktop/SecGloss/t-gly) (TLS) e Secure MIME (S/MIME).

CNG include il supporto per Suite B che si estende a tutti gli algoritmi necessari: AES (tutte le dimensioni delle chiavi), la famiglia SHA-2 (SHA-256, SHA-384 e SHA-512) degli algoritmi di hashing, ECDH e la curva ellittica DSA (ECDSA) sulle curve prime standard NIST P-256, P-384 e P-521. Le curve binarie, le curve Koblitz, le curve prime personalizzate e la curva ellittica Menezes-qu-Vanstone (ECMQV) non sono supportate dai provider di algoritmi Microsoft inclusi in Windows Vista.

## <a name="legacy-support"></a>Supporto legacy

CNG fornisce supporto per il set di algoritmi corrente in [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) 1,0. Ogni algoritmo attualmente supportato in *CryptoAPI* 1,0 continuerà a essere supportato in CNG.

## <a name="kernel-mode-support"></a>Supporto della modalità kernel

CNG supporta la crittografia in modalità kernel. Le stesse API vengono usate in modalità kernel e utente per supportare completamente le funzionalità di crittografia. SSL/TLS e IPsec funzionano in modalità kernel, oltre ai processi di avvio che utilizzeranno CNG. Non tutte le funzioni CNG possono essere chiamate dalla modalità kernel. L'argomento di riferimento per le funzioni che non possono essere chiamate dalla modalità kernel definirà in modo esplicito che la funzione non può essere chiamata dalla modalità kernel. In caso contrario, tutte le funzioni CNG possono essere chiamate dalla modalità kernel se il chiamante è in esecuzione a **\_ livello passivo** [*livello IRQL*](/windows/desktop/SecGloss/i-gly). Inoltre, alcune funzioni CNG in modalità kernel possono essere richiamabili a **livello di invio \_ livello IRQL**, a seconda delle funzionalità del provider.

L'interfaccia di Microsoft kernel Security Support Provider (Ksecdd.sys) è un modulo di crittografia per utilizzo generico, basato sul software, che risiede al livello di modalità kernel di Windows. Ksecdd.sys viene eseguito come driver di esportazione in modalità kernel e fornisce servizi di crittografia tramite le interfacce documentate ai componenti del kernel. L'unico algoritmo del provider Microsoft incorporato non supportato da Ksecdd.sys è DSA.

**Windows Server 2008 e Windows Vista:** CNG non supporta gli algoritmi e i provider plug-in in modalità kernel. Gli unici algoritmi di crittografia supportati disponibili in modalità kernel sono le implementazioni fornite da Microsoft tramite le API CNG in modalità kernel.

## <a name="auditing"></a>Controllo

Per soddisfare alcuni dei requisiti comuni relativi ai criteri, oltre a fornire una protezione completa, molte azioni che si verificano nel livello CNG vengono controllate nel provider di archiviazione chiavi (KSP) del software Microsoft. Il provider di archiviazione chiavi Microsoft rispetta le linee guida seguenti per creare record di controllo nel registro di sicurezza:

-   Gli errori di generazione di chiavi e coppie di chiavi, inclusi errori di test Self-Service, devono essere controllati.
-   È necessario controllare l'importazione e l'esportazione di chiavi.
-   Gli errori di distruzione delle chiavi devono essere controllati.
-   È necessario controllare le chiavi permanenti quando vengono scritte e lette dai file.
-   Gli errori di verifica della coerenza delle coppie devono essere controllati.
-   Gli eventuali errori di convalida della chiave privata devono essere controllati, ad esempio, controlli di parità sulle chiavi 3DES.
-   Gli errori di crittografia, decrittografia, hashing, firma, verifica, scambio di chiave e generazione di numeri casuali devono essere controllati.
-   I test autonomi crittografici devono essere controllati.

In generale, se una chiave non ha un nome, si tratta di una chiave temporanea. Una chiave temporanea non viene manomessa e il KSP Microsoft non genera record di controllo per le chiavi temporanee. Microsoft KSP genera record di controllo in modalità utente solo nel processo LSA. Nessun record di controllo viene generato da CNG in modalità kernel. Gli amministratori devono configurare i criteri di controllo per ottenere tutti i log di controllo KSP dal registro di sicurezza. Per configurare controlli aggiuntivi generati da KSP, un amministratore deve eseguire la riga di comando seguente:

**auditpol/set/SubCategory: "altri eventi di sistema"/Success: enable/failure: Enable**

## <a name="replaceable-random-number-generators"></a>Generatori di numeri casuali sostituibili

Un altro miglioramento fornito da CNG è la possibilità di sostituire il generatore di numeri casuali (RNG) predefinito. In CryptoAPI è possibile fornire un RNG alternativo come parte di un provider del servizio di crittografia (CSP), ma non è possibile reindirizzare i CSP di base di Microsoft per l'uso di un altro RNG. CNG consente di specificare in modo esplicito un determinato RNG da usare all'interno di chiamate particolari.

## <a name="thread-safety"></a>Thread safety

Tutte le funzioni che modificano la stessa area di memoria nello stesso momento (sezioni critiche) quando vengono chiamate da thread distinti non sono thread-safe.

## <a name="mode-of-operation"></a>Modalità di funzionamento

CNG supporta cinque modalità di operazioni che possono essere usate con le crittografie a blocchi simmetriche tramite le API di crittografia. Queste modalità e il relativo supporto sono elencate nella tabella seguente. È possibile modificare la modalità di operazione impostando la proprietà della [**\_ \_ modalità di concatenamento BCRYPT**](cng-property-identifiers.md) per il provider dell'algoritmo utilizzando la funzione [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) .



| Modalità di funzionamento           | \_Valore della modalità di concatenamento BCRYPT \_ | Algoritmi              | Standard  |
|-----------------------------|------------------------------|-------------------------|-----------|
| BCE (Electronic Codebook)   | **BCRYPT \_ Chain \_ mode \_ BCE** | Crittografie a blocchi simmetriche | SP800-38A |
| CBC (concatenamento di blocchi crittografici) | **CBC (BCRYPT \_ Chain \_ mode) \_** | Crittografie a blocchi simmetriche | SP800-38A |
| CFB (commenti e suggerimenti per la crittografia)       | **\_modalità a catena BCRYPT \_ \_ CFB** | Crittografie a blocchi simmetriche | SP800-38A |
| CCM (contatore con CBC)      | **\_ \_ CCM modalità a catena BCRYPT \_** | AES                     | SP800-38C |
| GCM (modalità Galois/Counter)   | **\_modalità a catena BCRYPT \_ \_ GCM** | AES                     | SP800-38D |



 

> [!Note]  
> Solo le modalità di funzionamento BCE, CBC e CFB sono definite in Windows Vista. GCM e CCM richiedono Windows Vista con Service Pack 1 (SP1) o Windows Server 2008.

 

 

 
