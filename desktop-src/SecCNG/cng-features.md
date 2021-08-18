---
description: CNG offre le funzionalità seguenti.
ms.assetid: 400a2b6e-6bbe-4ba4-abde-a2f625007517
title: Funzionalità CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434c72075c04b0c280c85831ca78d930c0fcc047de19609d11764bcf63ddad56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908448"
---
# <a name="cng-features"></a>Funzionalità CNG

CNG offre le funzionalità seguenti.

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

Una delle proposta di valore chiave di CNG è l'agilità crittografica, talvolta denominata agnosticismo crittografico. La conversione dell'implementazione di protocolli come [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) (SSL) o [*Transport Layer Security*](/windows/desktop/SecGloss/t-gly) (TLS), CMS (S/MIME), IPsec, Kerberos e così via, in CNG, tuttavia, è stata necessaria per rendere utile questa funzionalità. A livello CNG, era necessario fornire la sostituzione e l'individuabilità per tutti i tipi di algoritmo (simmetrica, asimmetrica, funzioni hash), la generazione di numeri casuali e altre funzioni di utilità. Le modifiche a livello di protocollo sono più significative perché in molti casi le API del protocollo necessarie per aggiungere la selezione dell'algoritmo e altre opzioni di flessibilità che non esistevano in precedenza.

CNG è disponibile per la prima volta in Windows Vista ed è posizionato per sostituire gli usi esistenti di [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) in tutto lo stack di software Microsoft. Gli sviluppatori di terze parti troveranno molte nuove funzionalità in CNG, tra cui:

-   Un nuovo sistema di configurazione della crittografia, che supporta una migliore agilità crittografica.
-   Astrazione con granularità più fine per l'archiviazione delle chiavi (e separazione dell'archiviazione dalle operazioni dell'algoritmo).
-   Isolamento dei processi per le operazioni con chiavi a lungo termine.
-   Generatori di numeri casuali sostituibili.
-   Non sono state applicate restrizioni di firma per l'esportazione.
-   Thread safety in tutto lo stack.
-   API di crittografia in modalità kernel.

CNG include anche il supporto per tutti gli algoritmi Suite B, inclusa la crittografia a curva [*ellittica*](/windows/desktop/SecGloss/e-gly) (ECC). Le applicazioni CryptoAPI esistenti continueranno a funzionare non appena CNG sarà disponibile.

## <a name="certification-and-compliance"></a>Certificazione e conformità

CNG viene convalidato in base a FIPS (Federal Information Processing Standards) 140-2 e fa parte della certificazione Target of Evaluation for the Windows Common Criteria. CNG è stato progettato per essere utilizzabile come componente in un sistema convalidato fiPS di livello 2.

CNG è conforme ai requisiti dei criteri comuni archiviando e usando chiavi di lunga durata in un processo sicuro.

## <a name="suite-b-support"></a>Supporto per Suite B

Una funzionalità importante di CNG è il supporto per Suite B algoritmi. Nel mese di febbraio 2005, la National Security Agency (NSA) del Stati Uniti ha annunciato un set coordinato di crittografia simmetrica, accordo segreto asimmetrico (noto anche come scambio di chiavi), firma digitale e funzioni hash per l'uso futuro del governo degli Stati Uniti *denominato Suite B*. L'NSA ha annunciato che le implementazioni Suite B certificate possono e verranno usate per la protezione delle informazioni designate come Top Secret, Secret e private information che in passato erano descritte come Sensitive-But-Unclassified. Per questo, il Suite B è molto importante per i fornitori di software applicativi e gli integratori di sistemi, nonché per Microsoft.

Tutti Suite B algoritmi sono noti pubblicamente. Sono stati sviluppati al di fuori dell'ambito della segretezza governativa associata cronologicamente allo sviluppo di algoritmi di crittografia. In questo stesso intervallo di tempo, alcuni paesi e aree geografiche europai hanno anche proposto gli stessi requisiti Suite B per la protezione delle informazioni.

Suite B crittografica consiglia l'uso di Diffie-Hellman a curva ellittica (ECDH) in molti protocolli esistenti, ad esempio Internet Key Exchange (IKE, usato principalmente in IPsec), [*Transport Layer Security*](/windows/desktop/SecGloss/t-gly) (TLS) e Secure MIME (S/MIME).

CNG include il supporto per Suite B che si estende a tutti gli algoritmi necessari: AES (tutte le dimensioni delle chiavi), la famiglia SHA-2 (SHA-256, SHA-384 e SHA-512) di algoritmi hash, ECDH e DSA a curva ellittica (ECDSA) sulle curve prime standard NIST P-256, P-384 e P-521. Le curve binarie, le curve di Koblitz, le curve prime personalizzate e le curve ellittiche Menezes-Qu-Vanstone (ECMQV) non sono supportate dai provider di algoritmi Microsoft inclusi in Windows Vista.

## <a name="legacy-support"></a>Supporto legacy

CNG fornisce il supporto per il set corrente di algoritmi in [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) 1.0. Ogni algoritmo attualmente supportato in *CryptoAPI* 1.0 continuerà a essere supportato in CNG.

## <a name="kernel-mode-support"></a>Supporto della modalità kernel

CNG supporta la crittografia in modalità kernel. Le stesse API vengono usate sia in modalità kernel che in modalità utente per supportare completamente le funzionalità di crittografia. SSL/TLS e IPsec funzionano in modalità kernel oltre ai processi di avvio che usano CNG. Non tutte le funzioni CNG possono essere chiamate dalla modalità kernel. L'argomento di riferimento per le funzioni che non possono essere chiamate dalla modalità kernel indica in modo esplicito che la funzione non può essere chiamata dalla modalità kernel. In caso contrario, tutte le funzioni CNG possono essere chiamate dalla modalità kernel se il chiamante è in esecuzione a **LIVELLO \_ PASSIVO** [*IRQL.*](/windows/desktop/SecGloss/i-gly) Inoltre, alcune funzioni CNG in modalità kernel possono essere chiamate a **livello di DISPATCH \_ IRQL,** a seconda delle funzionalità del provider.

Microsoft kernel security support provider interface (Ksecdd.sys) è un modulo di crittografia basato su software generico che si trova al livello di modalità kernel di Windows. Ksecdd.sys viene eseguito come driver di esportazione in modalità kernel e fornisce servizi di crittografia tramite le interfacce documentate ai componenti del kernel. L'unico algoritmo del provider Microsoft incorporato non supportato da Ksecdd.sys è DSA.

**Windows Server 2008 e Windows Vista:** CNG non supporta algoritmi e provider collegabili in modalità kernel. Gli unici algoritmi di crittografia supportati disponibili in modalità kernel sono le implementazioni fornite da Microsoft tramite le API CNG in modalità kernel.

## <a name="auditing"></a>Controllo

Per rispettare alcuni dei requisiti di criteri comuni oltre a garantire una sicurezza completa, molte azioni che si verificano nel livello CNG vengono controllati nel provider di archiviazione chiavi software (KSP) Microsoft. Microsoft KSP rispetta le linee guida seguenti per creare record di controllo nel log di sicurezza:

-   È necessario controllare gli errori di generazione di chiavi e coppie di chiavi, inclusi gli errori di auto-test.
-   È necessario controllare l'importazione e l'esportazione delle chiavi.
-   È necessario controllare gli errori di distruzione delle chiavi.
-   Le chiavi persistenti devono essere controllati quando vengono scritte e lette dai file.
-   È necessario controllare gli errori delle verifiche di coerenza a livello di coppia.
-   Gli eventuali errori di convalida della chiave privata devono essere controllati, ad esempio i controlli di parità sulle chiavi 3DES.
-   È necessario controllare gli errori di crittografia, decrittografia, hash, firma, verifica, scambio di chiavi e generazione di numeri casuali.
-   È necessario controllare gli auto test crittografici.

In generale, se una chiave non ha un nome, è una chiave ffimera. Una chiave effimera non viene mantenuta e il provider di chiavi Microsoft KSP non genera record di controllo per le chiavi ffimeri. Microsoft KSP genera record di controllo solo in modalità utente nel processo LSA. Nessun record di controllo viene generato da CNG in modalità kernel. Gli amministratori devono configurare i criteri di controllo per ottenere tutti i log di controllo KSP dal log di sicurezza. Un amministratore deve eseguire la riga di comando seguente per configurare controlli aggiuntivi generati dai KSP:

**auditpol /set /subcategory:"other system events" /success:enable /failure:enable**

## <a name="replaceable-random-number-generators"></a>Generatori di numeri casuali sostituibili

Un altro miglioramento fornito da CNG è la possibilità di sostituire il generatore di numeri casuali (RNG) predefinito. In CryptoAPI è possibile fornire un RNG alternativo come parte di un provider del servizio di crittografia (CSP), ma non è possibile reindirizzare i CSP Di base Microsoft per l'uso di un altro RNG. CNG consente di specificare in modo esplicito un RNG specifico da usare all'interno di chiamate specifiche.

## <a name="thread-safety"></a>Thread safety

Tutte le funzioni che modificano la stessa area di memoria contemporaneamente (sezioni critiche) quando vengono chiamate da thread separati non sono thread-safe.

## <a name="mode-of-operation"></a>Modalità di funzionamento

CNG supporta cinque modalità di operazioni che possono essere usate con crittografie a blocchi simmetriche tramite le API di crittografia. Queste modalità e la relativa supportabilità sono elencate nella tabella seguente. La modalità di funzionamento può essere modificata impostando la proprietà [**BCRYPT \_ CHAINING \_ MODE**](cng-property-identifiers.md) per il provider di algoritmi usando la [**funzione BCryptSetProperty.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty)



| Modalità di funzionamento           | Valore BCRYPT \_ CHAINING \_ MODE | Algoritmi              | Standard  |
|-----------------------------|------------------------------|-------------------------|-----------|
| ELECTRONIC (Electronic Codebook)   | **BCRYPT \_ CHAIN \_ MODE \_ ESEREZIONE** | Crittografie a blocchi simmetriche | SP800-38A |
| CBC (Cipher Block Chaining) | **BCRYPT \_ CHAIN \_ MODE \_ CBC** | Crittografie a blocchi simmetriche | SP800-38A |
| CFB (Feedback di crittografia)       | **BCRYPT \_ CHAIN \_ MODE \_ CFB** | Crittografie a blocchi simmetriche | SP800-38A |
| CCM (contatore con CBC)      | **BCRYPT \_ CHAIN \_ MODE \_ CCM** | AES                     | SP800-38C |
| GCM (Modalità galeo/contatore)   | **BCRYPT \_ CHAIN \_ MODE \_ GCM** | AES                     | SP800-38D |



 

> [!Note]  
> In VISTA vengono definite solo le modalità di funzionamento DISA, CBC e CFB Windows Vista. GCM e CCM richiedono Windows Vista con Service Pack 1 (SP1) o Windows Server 2008.

 

 

 
