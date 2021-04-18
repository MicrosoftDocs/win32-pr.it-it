---
description: La crittografia a chiave pubblica (detta anche crittografia a chiave asimmetrica) usa una coppia di chiavi per crittografare e decrittografare il contenuto.
ms.assetid: 93f65367-ca4b-4b44-9833-0653cfd3f3d3
title: Infrastruttura a chiave pubblica (PKI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e4ff0b2b3912bc44851be105c2e2b15200eb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314142"
---
# <a name="public-key-infrastructure"></a>Infrastruttura a chiave pubblica (PKI)

La crittografia a chiave pubblica (detta anche crittografia a chiave asimmetrica) usa una coppia di chiavi per crittografare e decrittografare il contenuto. La coppia di chiavi è costituita da una chiave pubblica e una chiave privata correlate matematicamente. Un utente che intende comunicare in modo sicuro con altri utenti può distribuire la [*chiave pubblica*](/windows/desktop/SecGloss/p-gly) , ma deve tenere segreta la [*chiave privata*](/windows/desktop/SecGloss/p-gly) . Il contenuto crittografato tramite una delle chiavi può essere decrittografato utilizzando l'altro. Si supponga, ad esempio, che Bob desideri inviare un messaggio di posta elettronica protetto ad Alice. Questa operazione può essere eseguita nel modo seguente:

1.  Bob e Alice hanno coppie di chiavi personalizzate. Hanno mantenuto le chiavi private in modo sicuro e hanno inviato le chiavi pubbliche direttamente tra loro.
2.  Bob usa la chiave pubblica di Alice per crittografare il messaggio e lo invia al suo.
3.  Alice usa la propria chiave privata per decrittografare il messaggio.

Questo esempio semplificato evidenzia almeno una preoccupazione ovvia che Bob deve avere sulla chiave pubblica usata per crittografare il messaggio. Ovvero, non sa con certezza che la chiave usata per la crittografia appartiene effettivamente ad Alice. È possibile che un'altra parte che monitora il canale di comunicazione tra Bob e Alice sostituisca con una chiave diversa.

Il concetto di infrastruttura a chiave pubblica si è evoluto per aiutare a risolvere questo problema e altri. Un'infrastruttura a chiave pubblica (PKI) è costituita da elementi software e hardware che possono essere utilizzati da terze parti attendibili per stabilire l'integrità e la proprietà di una chiave pubblica. La parte attendibile, detta [*autorità di certificazione*](/windows/desktop/SecGloss/c-gly) (CA), in genere esegue questa operazione mediante l'emissione di certificati binari firmati (crittografati) che affermano l'identità del soggetto del certificato e associano tale identità alla chiave pubblica contenuta nel certificato. La CA firma il certificato usando la relativa chiave privata. Rilascia la chiave pubblica corrispondente a tutte le parti interessate in un certificato della CA autofirmato. Quando si usa un'autorità di certificazione, l'esempio precedente può essere modificato nel modo seguente:

1.  Si supponga che la CA abbia emesso un certificato digitale firmato che contenga la chiave pubblica. La CA firma autonomamente questo certificato usando la chiave privata corrispondente alla chiave pubblica nel certificato.
2.  Alice e Bob accettano di usare la CA per verificare le proprie identità.
3.  Alice richiede un certificato di chiave pubblica dalla CA.
4.  La CA verifica la propria identità, calcola un hash del contenuto che costituirà il certificato, firma l'hash usando la chiave privata corrispondente alla chiave pubblica nel certificato della CA pubblicata, crea un nuovo certificato concatenando il contenuto del certificato e l'hash firmato e rende disponibile pubblicamente il nuovo certificato.
5.  Bob recupera il certificato, decrittografa l'hash firmato usando la chiave pubblica dell'autorità di certificazione, calcola un nuovo hash del contenuto del certificato e confronta i due hash. Se gli hash corrispondono, la firma viene verificata e Bob può presumere che la chiave pubblica nel certificato appartenga effettivamente a Alice.
6.  Bob usa la chiave pubblica verificata di Alice per crittografare un messaggio.
7.  Alice usa la propria chiave privata per decrittografare il messaggio da Bob.

In sintesi, il processo di firma del certificato consente a Bob di verificare che la chiave pubblica non sia stata manomessa o danneggiata durante il transito. Prima di emettere un certificato, la CA esegue l'hashing del contenuto, firma (crittografa) l'hash usando la relativa chiave privata e include l'hash crittografato nel certificato emesso. Bob verifica il contenuto del certificato decrittografando l'hash con la chiave pubblica dell'autorità di certificazione, eseguendo un hash separato del contenuto del certificato e confrontando i due hash. Se corrispondono, Bob può essere ragionevolmente certi che il certificato e la chiave pubblica che contiene non siano stati modificati.

Una PKI tipica è costituita dagli elementi seguenti.

| Elemento                            | Descrizione                                                                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Autorità di certificazione<br/> | Funge da radice di attendibilità in un'infrastruttura a chiave pubblica e fornisce servizi che autenticano l'identità di singoli utenti, computer e altre entità in una rete.<br/>      |
| Autorità di registrazione<br/>  | È certificato da una CA radice per emettere certificati per usi specifici consentiti dalla radice. In un'infrastruttura a chiave pubblica Microsoft, un'autorità di registrazione (RA) viene in genere chiamata CA subordinata.<br/> |
| Database di certificati<br/>    | Salva le richieste di certificati e i certificati emessi e revocati e le richieste di certificati sulla CA o RA.<br/>                                                                       |
| Archivio certificati<br/>       | Salva i certificati emessi e le richieste di certificati in sospeso o rifiutate nel computer locale.<br/>                                                                                  |
| Server di archiviazione chiavi<br/>     | Salva le chiavi private crittografate nel database dei certificati per il ripristino dopo la perdita.<br/>                                                                                              |



 

L'API di registrazione certificati consente di inviare richieste di certificati e di archiviazione delle chiavi alle autorità di certificazione e registrazione e di installare il certificato emesso in un computer locale. Non consente di modificare direttamente il database dei certificati o l'archivio certificati.

Gli argomenti seguenti illustrano l'infrastruttura a chiave pubblica Microsoft in modo più dettagliato:

-   [Certificati di chiave pubblica X. 509](about-x-509-public-key-certificates.md)
-   [Elementi PKI](about-pki-components.md)
-   [Modelli di attendibilità](about-trust-models.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API di registrazione certificati](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

