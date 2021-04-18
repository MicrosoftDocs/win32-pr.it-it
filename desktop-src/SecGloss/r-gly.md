---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera R.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ce589e18-02ac-42c2-b76b-776deb686bbd
title: R (Glossario sulla sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc85a0da8aa4a0b985b8be040ef95e37068e8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314677"
---
# <a name="r-security-glossary"></a>R (Glossario sulla sicurezza)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_rc2_gly"></span><span id="_SECURITY_RC2_GLY"></span>**RC2**
</dt> <dd>

Nome dell'algoritmo [*CryptoAPI*](c-gly.md) per l'algoritmo RC2.

Vedere anche *algoritmo di blocco RC2*.

</dd> <dt>

<span id="_security_rc2_block_algorithm_gly"></span><span id="_SECURITY_RC2_BLOCK_ALGORITHM_GLY"></span>**Algoritmo di blocco RC2**
</dt> <dd>

Algoritmo di [*crittografia*](e-gly.md) dei dati basato sul codice a blocchi SIMMETRICo RC2 a 64 bit. RC2 viene specificato dai \_ tipi di \_ provider completi di prova RSA. [*CryptoAPI*](c-gly.md) fa riferimento a questo algoritmo in base al relativo identificatore (CALG \_ RC2), al nome (RC2) e alla classe ( \_ \_ crittografia dei dati della classe ALG \_ ).

</dd> <dt>

<span id="_security_rc4_gly"></span><span id="_SECURITY_RC4_GLY"></span>**RC4**
</dt> <dd>

Nome dell'algoritmo [*CryptoAPI*](c-gly.md) per l'algoritmo RC4.

Vedere anche *algoritmo di flusso RC4*.

</dd> <dt>

<span id="_security_rc4_stream_algorithm_gly"></span><span id="_SECURITY_RC4_STREAM_ALGORITHM_GLY"></span>**Algoritmo di flusso RC4**
</dt> <dd>

Algoritmo di [*crittografia*](e-gly.md) dei dati basato sulla crittografia del flusso simmetrico RC4. RC4 è specificato dai \_ tipi di \_ provider completi RSA di prova. [*CryptoAPI*](c-gly.md) fa riferimento a questo algoritmo in base al relativo identificatore (CALG \_ RC4), al nome (RC4) e alla classe ( \_ \_ crittografia dei dati della classe ALG \_ ).

</dd> <dt>

<span id="_security_rdn_gly"></span><span id="_SECURITY_RDN_GLY"></span>**RDN**
</dt> <dd>

Vedere *nome distinto relativo*.

</dd> <dt>

<span id="_security_reader_gly"></span><span id="_SECURITY_READER_GLY"></span>**lettore**
</dt> <dd>

Un dispositivo standard all'interno del sottosistema [*Smart Card*](s-gly.md) . Un dispositivo di interfaccia (IFD) che supporta input/output bidirezionale in una smart card. Può essere associato a un intero sistema, a uno o più gruppi di lettori o a un terminale specifico. Il sottosistema Smart Card consente a un lettore di essere dedicato al terminale a cui è assegnato. Attualmente, tuttavia, in un computer esiste solo un terminale.

</dd> <dt>

<span id="_security_reader_driver_gly"></span><span id="_SECURITY_READER_DRIVER_GLY"></span>**driver Lettore**
</dt> <dd>

Driver specifico che esegue il mapping dei servizi del driver a un dispositivo di lettura hardware specifico. Deve comunicare gli eventi di inserimento e rimozione delle schede al driver della classe [*Smart Card*](s-gly.md) per l'invio al gestore di risorse della smart card e deve fornire funzionalità di scambio di dati alla scheda da qualsiasi protocollo raw, t = 0, t = 1 o pts.

</dd> <dt>

<span id="_security_reader_group_gly"></span><span id="_SECURITY_READER_GROUP_GLY"></span>**gruppo Reader**
</dt> <dd>

Gruppo logico di Reader. I gruppi di Reader possono essere definiti dal sistema o creati dagli utenti o dagli amministratori. I gruppi di Reader vengono utilizzati dalle funzioni smart card che possono agire su gruppi di lettori. Per evitare conflitti di denominazione con i gruppi definiti dall'utente, Microsoft si riserva l'uso di qualsiasi nome che contiene il simbolo del dollaro ($).

</dd> <dt>

<span id="_security_reader_helper_driver_gly"></span><span id="_SECURITY_READER_HELPER_DRIVER_GLY"></span>**driver helper Reader**
</dt> <dd>

Fornisce le routine di supporto dei driver delle smart card comuni e il supporto del protocollo T = 0 e T = 1 aggiuntivo per i driver specifici in base alle esigenze.

</dd> <dt>

<span id="_security_reference_count_gly"></span><span id="_SECURITY_REFERENCE_COUNT_GLY"></span>**conteggio riferimenti**
</dt> <dd>

Valore integer utilizzato per tenere traccia di un oggetto COM. Quando viene creato un oggetto, il conteggio dei riferimenti viene impostato su uno. Ogni volta che un'interfaccia viene associata all'oggetto, il conteggio dei riferimenti viene incrementato; Quando la connessione all'interfaccia viene distrutta, il conteggio dei riferimenti viene decrementato. L'oggetto viene eliminato definitivamente quando il conteggio dei riferimenti raggiunge zero. Tutte le interfacce dell'oggetto non sono valide.

</dd> <dt>

<span id="_security_relative_distinguished_name_gly"></span><span id="_SECURITY_RELATIVE_DISTINGUISHED_NAME_GLY"></span>**nome distinto relativo**
</dt> <dd>

RDN Entità inclusa come oggetto in una richiesta di un certificato. Gli elementi in un RDN vengono definiti in base ai relativi attributi e non è necessario includere un nome. Per quanto concerne [*CryptoAPI*](c-gly.md), un RDN viene definito da una \_ struttura RDN del certificato, che a sua volta punta a una matrice di \_ strutture di attributi RDN del certificato \_ . Ogni struttura dell'attributo specifica un singolo attributo.

</dd> <dt>

<span id="_security_relative_identifier_gly"></span><span id="_SECURITY_RELATIVE_IDENTIFIER_GLY"></span>**identificatore relativo**
</dt> <dd>

SBARAZZARSI Parte di un [*ID di sicurezza*](s-gly.md) (SID) che identifica un utente o un gruppo in relazione all'autorità che ha emesso il SID.

</dd> <dt>

<span id="_security_relocated_store_gly"></span><span id="_SECURITY_RELOCATED_STORE_GLY"></span>**Archivio rilocato**
</dt> <dd>

[*Archivio certificati*](c-gly.md) spostato dal percorso predefinito del registro di sistema in una posizione diversa nel registro di sistema.

</dd> <dt>

<span id="_security_remote_store_gly"></span><span id="_SECURITY_REMOTE_STORE_GLY"></span>**Archivio remoto**
</dt> <dd>

[*Archivio certificati*](c-gly.md) che si trova in un altro computer, ad esempio un file server o un altro computer remoto condiviso.

</dd> <dt>

<span id="_security_reply_apdu_gly"></span><span id="_SECURITY_REPLY_APDU_GLY"></span>**APDU di risposta**
</dt> <dd>

Un' [*unità dati del protocollo dell'applicazione*](a-gly.md) (APDU) inviata in risposta a un APDU ricevuto.

</dd> <dt>

<span id="_security_repudiation_gly"></span><span id="_SECURITY_REPUDIATION_GLY"></span>**ripudio**
</dt> <dd>

Capacità di un utente di negare di aver eseguito una determinata azione in casi in cui risulta impossibile provare il contrario. Ad esempio, un utente che ha eliminato un file e chi può negarlo correttamente.

</dd> <dt>

<span id="_security_resource_manager_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_GLY"></span>**Resource Manager**
</dt> <dd>

Il modulo del sottosistema [*Smart Card*](s-gly.md) che gestisce l'accesso a più lettori e smart card. Resource Manager identifica e tiene traccia delle risorse, alloca Reader e risorse tra più applicazioni e supporta le primitive delle transazioni per accedere ai servizi disponibili in una scheda specifica.

</dd> <dt>

<span id="_security_resource_manager_api_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_API_GLY"></span>**API di Resource Manager**
</dt> <dd>

Set di funzioni di Windows che forniscono accesso diretto ai servizi di Resource Manager.

</dd> <dt>

<span id="_security_resource_manager_context_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_CONTEXT_GLY"></span>**contesto di Resource Manager**
</dt> <dd>

Contesto utilizzato da Resource Manager quando si accede al database della smart card. Il contesto di Resource Manager viene utilizzato principalmente dalle funzioni di gestione e query quando si accede al database. L'ambito del contesto di Resource Manager può essere l'utente corrente o il sistema.

</dd> <dt>

<span id="_security_revocation_list_gly"></span><span id="_SECURITY_REVOCATION_LIST_GLY"></span>**elenco di revoche**
</dt> <dd>

Vedere l' [*elenco di revoche di certificati*](c-gly.md).

</dd> <dt>

<span id="_security_rid_gly"></span><span id="_SECURITY_RID_GLY"></span>**SBARAZZARSI**
</dt> <dd>

Vedere *identificatore relativo*.

</dd> <dt>

<span id="_security_root_authority_gly"></span><span id="_SECURITY_ROOT_AUTHORITY_GLY"></span>**autorità radice**
</dt> <dd>

[*Autorità di certificazione*](c-gly.md) (CA) all'inizio di una gerarchia di CA. L'autorità radice certifica le CA del livello immediatamente inferiore della gerarchia.

</dd> <dt>

<span id="_security_root_certificate_gly"></span><span id="_SECURITY_ROOT_CERTIFICATE_GLY"></span>**certificato radice**
</dt> <dd>

Un certificato dell' [*autorità di certificazione*](c-gly.md) (CA) autofirmato che identifica una CA. Viene chiamato certificato radice perché è il certificato per la CA radice. La CA radice deve firmare il proprio certificato CA perché per definizione non esiste un'autorità di certificazione più elevata per firmare il certificato della CA.

</dd> <dt>

<span id="_security_rsa_gly"></span><span id="_SECURITY_RSA_GLY"></span>**RSA**
</dt> <dd>

RSA Data Security, Inc., uno sviluppatore e un editore principali di PKCS ( [*Public Key Cryptography Standards*](p-gly.md) ). Il nome "RSA" nel nome corrisponde ai nomi dei tre sviluppatori della società e dei proprietari: Rivet, Shamir e Adleman.

</dd> <dt>

<span id="_security_rsa_keyx_gly"></span><span id="_SECURITY_RSA_KEYX_GLY"></span>**\_KEYX RSA**
</dt> <dd>

Nome dell'algoritmo [*CryptoAPI*](c-gly.md) per l'algoritmo di scambio delle chiavi RSA. CryptoAPI fa riferimento anche a questo algoritmo in base al relativo identificatore di algoritmo (CALG \_ RSA \_ KEYX) e alla classe (ALG \_ Class \_ Key \_ Exchange).

</dd> <dt>

<span id="_security_rsa_sign_gly"></span><span id="_SECURITY_RSA_SIGN_GLY"></span>**\_segno RSA**
</dt> <dd>

Nome dell'algoritmo CryptoAPI per l'algoritmo di firma RSA. CryptoAPI fa riferimento anche a questo algoritmo tramite il relativo identificatore di algoritmo (CALG \_ RSA \_ Sign) e la classe (ALG \_ Class \_ Signature).

</dd> <dt>

<span id="_security_rsa_public_key_algorithm_gly"></span><span id="_SECURITY_RSA_PUBLIC_KEY_ALGORITHM_GLY"></span>**Algoritmo di chiave pubblica RSA**
</dt> <dd>

Uno scambio di chiave e un algoritmo di firma basati sul noto codice di crittografia a chiave pubblica RSA. Questo algoritmo viene usato dai tipi di provider di prova \_ RSA \_ full, prov \_ RSA \_ sig, prov \_ MS \_ Exchange e dimostrati \_ SSL. CryptoAPI fa riferimento a questo algoritmo mediante i relativi identificatori (CALG \_ RSA \_ KEYX e CALG \_ RSA \_ Sign), i nomi (RSA \_ KEYX e RSA \_ Sign) e Class (ALG \_ Class \_ Key \_ Exchange).

</dd> </dl>

 

 



