---
description: La crittografia a chiave pubblica (detta anche crittografia a chiave asimmetrica) usa una coppia di chiavi per crittografare e decrittografare il contenuto.
ms.assetid: 93f65367-ca4b-4b44-9833-0653cfd3f3d3
title: Infrastruttura a chiave pubblica (PKI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a306f227a3e39c32b7e0eef2dbf1dc4ae9d59942096fb71428339d8a166a04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101131"
---
# <a name="public-key-infrastructure"></a>Infrastruttura a chiave pubblica (PKI)

La crittografia a chiave pubblica (detta anche crittografia a chiave asimmetrica) usa una coppia di chiavi per crittografare e decrittografare il contenuto. La coppia di chiavi è costituita da una chiave pubblica e una chiave privata correlate matematicamente. Un utente che intende comunicare in modo sicuro con altri utenti può distribuire [*la*](/windows/desktop/SecGloss/p-gly) chiave pubblica, ma deve mantenere la [*chiave*](/windows/desktop/SecGloss/p-gly) privata segreta. Il contenuto crittografato tramite una delle chiavi può essere decrittografato usando l'altra. Si supponga, ad esempio, che Bob voglia inviare un messaggio di posta elettronica sicuro ad Alice. Questa operazione può essere eseguita nel modo seguente:

1.  Bob e Alice hanno le proprie coppie di chiavi. Le chiavi private sono state mantenute in modo sicuro e le chiavi pubbliche sono state inviate direttamente l'una all'altra.
2.  Bob usa la chiave pubblica di Alice per crittografare il messaggio e inviarlo a lei.
3.  Alice usa la chiave privata per decrittografare il messaggio.

Questo esempio semplificato evidenzia almeno un ovvio problema che Bob deve avere sulla chiave pubblica usata per crittografare il messaggio. Ciò significa che non può sapere con certezza che la chiave usata per la crittografia appartiene effettivamente ad Alice. È possibile che un'altra parte che monitori il canale di comunicazione tra Bob e Alice sostituisca una chiave diversa.

Il concetto di infrastruttura a chiave pubblica si è evoluto per risolvere questo problema e altri. Un'infrastruttura a chiave pubblica è costituita da elementi software e hardware che una terza parte attendibile può usare per stabilire l'integrità e la proprietà di una chiave pubblica. L'entità attendibile, denominata autorità di certificazione [*(CA),*](/windows/desktop/SecGloss/c-gly) in genere esegue questa operazione emettendo certificati binari firmati (crittografati) che confermano l'identità del soggetto del certificato e associano tale identità alla chiave pubblica contenuta nel certificato. La CA firma il certificato usando la relativa chiave privata. Elava la chiave pubblica corrispondente a tutte le parti interessate in un certificato CA autofirmato. Quando si usa una CA, l'esempio precedente può essere modificato nel modo seguente:

1.  Si supponga che la CA abbia emesso un certificato digitale firmato che contiene la chiave pubblica. La CA autofirma il certificato usando la chiave privata corrispondente alla chiave pubblica nel certificato.
2.  Alice e Bob accettano di usare la CA per verificare le identità.
3.  Alice richiede un certificato di chiave pubblica all'autorità di certificazione.
4.  La CA verifica la propria identità, calcola un hash del contenuto che costituisce il certificato, firma l'hash usando la chiave privata che corrisponde alla chiave pubblica nel certificato della CA pubblicata, crea un nuovo certificato concatenando il contenuto del certificato e l'hash firmato e rende il nuovo certificato disponibile pubblicamente.
5.  Bob recupera il certificato, decrittografa l'hash firmato usando la chiave pubblica della CA, calcola un nuovo hash del contenuto del certificato e confronta i due hash. Se gli hash corrispondono, la firma viene verificata e Bob può presupporre che la chiave pubblica nel certificato appartenga effettivamente ad Alice.
6.  Bob usa la chiave pubblica verificata di Alice per crittografare un messaggio.
7.  Alice usa la chiave privata per decrittografare il messaggio da Bob.

In sintesi, il processo di firma del certificato consente a Bob di verificare che la chiave pubblica non sia stata manomesso o danneggiato durante il transito. Prima di rilasciare un certificato, la CA esegue l'hashing del contenuto, firma (crittografa) l'hash usando la propria chiave privata e include l'hash crittografato nel certificato emesso. Bob verifica il contenuto del certificato decrittografando l'hash con la chiave pubblica della CA, eseguendo un hash separato del contenuto del certificato e confrontando i due hash. Se corrispondono, Bob può essere ragionevolmente certo che il certificato e la chiave pubblica in esso contenuta non siano stati modificati.

Un'infrastruttura a chiave pubblica tipica è costituita dai seguenti elementi.

| Elemento                            | Descrizione                                                                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Autorità di certificazione<br/> | Funge da radice di attendibilità in un'infrastruttura a chiave pubblica e fornisce servizi che autenticano l'identità di singoli utenti, computer e altre entità in una rete.<br/>      |
| Autorità di registrazione<br/>  | È certificata da una CA radice per rilasciare certificati per usi specifici consentiti dalla radice. In un'infrastruttura a chiave pubblica Microsoft, un'autorità di registrazione (RA) è in genere denominata CA subordinata.<br/> |
| Database dei certificati<br/>    | Salva le richieste di certificato e i certificati rilasciati e revocati e le richieste di certificato nella CA o nell'autorità di certificazione.<br/>                                                                       |
| Archivio certificati<br/>       | Salva i certificati rilasciati e le richieste di certificato in sospeso o rifiutate nel computer locale.<br/>                                                                                  |
| Server di archiviazione delle chiavi<br/>     | Salva le chiavi private crittografate nel database dei certificati per il ripristino dopo la perdita.<br/>                                                                                              |



 

L'API Di registrazione certificati consente di inviare richieste di archiviazione di certificati e chiavi alle autorità di certificazione e registrazione e di installare il certificato emesso in un computer locale. Non consente di modificare direttamente il database dei certificati o l'archivio certificati.

Negli argomenti seguenti viene illustrata in modo più dettagliato l'infrastruttura a chiave pubblica Microsoft:

-   [Certificati a chiave pubblica X.509](about-x-509-public-key-certificates.md)
-   [Elementi PKI](about-pki-components.md)
-   [Modelli di attendibilità](about-trust-models.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API di registrazione certificati](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

