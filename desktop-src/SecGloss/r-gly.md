---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera R.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ce589e18-02ac-42c2-b76b-776deb686bbd
title: R (glossario della sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a566a939746cd65c6336e8f31ff05a7ee3f0a3b7954e9d790d3f15a8163f138b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895290"
---
# <a name="r-security-glossary"></a>R (glossario della sicurezza)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q R [S](s-gly.md) T [U](t-gly.md) [](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_rc2_gly"></span><span id="_SECURITY_RC2_GLY"></span>**RC2**
</dt> <dd>

Nome [*dell'algoritmo CryptoAPI*](c-gly.md) per l'algoritmo RC2.

Vedere anche *Algoritmo a blocchi RC2.*

</dd> <dt>

<span id="_security_rc2_block_algorithm_gly"></span><span id="_SECURITY_RC2_BLOCK_ALGORITHM_GLY"></span>**Algoritmo a blocchi RC2**
</dt> <dd>

Algoritmo [*di crittografia*](e-gly.md) dei dati basato sulla crittografia a blocchi simmetrica RC2 a 64 bit. RC2 viene specificato dai tipi di \_ provider PROV RSA \_ FULL. [*CryptoAPI fa*](c-gly.md) riferimento a questo algoritmo tramite il relativo identificatore (CALG \_ RC2), il nome (RC2) e la classe (ALG \_ CLASS DATA \_ \_ ENCRYPT).

</dd> <dt>

<span id="_security_rc4_gly"></span><span id="_SECURITY_RC4_GLY"></span>**RC4**
</dt> <dd>

Nome [*dell'algoritmo CryptoAPI*](c-gly.md) per l'algoritmo RC4.

Vedere anche *Algoritmo di flusso RC4.*

</dd> <dt>

<span id="_security_rc4_stream_algorithm_gly"></span><span id="_SECURITY_RC4_STREAM_ALGORITHM_GLY"></span>**Algoritmo di flusso RC4**
</dt> <dd>

Algoritmo [*di crittografia*](e-gly.md) dei dati basato sulla crittografia del flusso simmetrico RC4. RC4 viene specificato dai tipi di \_ provider PROV RSA \_ FULL. [*CryptoAPI fa*](c-gly.md) riferimento a questo algoritmo tramite il relativo identificatore (CALG \_ RC4), il nome (RC4) e la classe (ALG \_ CLASS DATA \_ \_ ENCRYPT).

</dd> <dt>

<span id="_security_rdn_gly"></span><span id="_SECURITY_RDN_GLY"></span>**Rdn**
</dt> <dd>

Vedere *il nome distinto relativo*.

</dd> <dt>

<span id="_security_reader_gly"></span><span id="_SECURITY_READER_GLY"></span>**Lettore**
</dt> <dd>

Un dispositivo standard all'interno [*smart card*](s-gly.md) sottosistema. Un dispositivo di interfaccia (IFD) che supporta l'input/output bidirezionale in un smart card. Può essere associato a un intero sistema, a uno o più gruppi di lettori o a un terminale specifico. Il smart card sottosistema consente a un lettore di essere dedicato al terminale a cui è assegnato. Tuttavia, attualmente esiste un solo terminale in un computer.

</dd> <dt>

<span id="_security_reader_driver_gly"></span><span id="_SECURITY_READER_DRIVER_GLY"></span>**driver lettore**
</dt> <dd>

Driver specifico che esegue il mapping dei servizi driver a un dispositivo lettore hardware specifico. Deve comunicare gli eventi di inserimento e rimozione di schede al driver di classe [*smart card*](s-gly.md) per l'inoltro al gestore di risorse di smart card e deve fornire funzionalità di scambio dei dati alla scheda da qualsiasi protocollo non elaborato, T=0, T=1 o PTS.

</dd> <dt>

<span id="_security_reader_group_gly"></span><span id="_SECURITY_READER_GROUP_GLY"></span>**gruppo di lettori**
</dt> <dd>

Gruppo logico di lettori. I gruppi di lettori possono essere definiti dal sistema o creati da utenti o amministratori. I gruppi di lettori vengono usati smart card funzioni che possono agire su gruppi di lettori. Per evitare conflitti di denominazione con i gruppi definiti dall'utente, Microsoft si riserva l'uso di qualsiasi nome contenente il simbolo del dollaro ($).

</dd> <dt>

<span id="_security_reader_helper_driver_gly"></span><span id="_SECURITY_READER_HELPER_DRIVER_GLY"></span>**driver helper reader**
</dt> <dd>

Fornisce routine smart card di supporto dei driver comuni e supporto aggiuntivo dei protocolli T=0 e T=1 a driver specifici in base alle esigenze.

</dd> <dt>

<span id="_security_reference_count_gly"></span><span id="_SECURITY_REFERENCE_COUNT_GLY"></span>**conteggio dei riferimenti**
</dt> <dd>

Valore intero utilizzato per tenere traccia di un oggetto COM. Quando viene creato un oggetto, il conteggio dei riferimenti viene impostato su uno. Ogni volta che un'interfaccia viene associata all'oggetto, il conteggio dei riferimenti viene incrementato; Quando la connessione all'interfaccia viene distrutta, il conteggio dei riferimenti viene decrementato. L'oggetto viene eliminato quando il conteggio dei riferimenti raggiunge lo zero. Tutte le interfacce per tale oggetto non sono quindi valide.

</dd> <dt>

<span id="_security_relative_distinguished_name_gly"></span><span id="_SECURITY_RELATIVE_DISTINGUISHED_NAME_GLY"></span>**nome distinto relativo**
</dt> <dd>

(RDN) Entità inclusa come oggetto in una richiesta di certificato. Gli elementi in un RDN sono definiti dai relativi attributi e non è necessario includere un nome. Per quanto riguarda [*CryptoAPI,*](c-gly.md)un RDN è definito da una struttura CERT RDN, che a sua volta punta a una matrice di strutture di \_ \_ attributi CERT RDN \_ ATTR. Ogni struttura dell'attributo specifica un singolo attributo.

</dd> <dt>

<span id="_security_relative_identifier_gly"></span><span id="_SECURITY_RELATIVE_IDENTIFIER_GLY"></span>**identificatore relativo**
</dt> <dd>

(RID) Parte di un [*ID di sicurezza*](s-gly.md) (SID) che identifica un utente o un gruppo in relazione all'autorità che ha emesso il SID.

</dd> <dt>

<span id="_security_relocated_store_gly"></span><span id="_SECURITY_RELOCATED_STORE_GLY"></span>**archivio rilocato**
</dt> <dd>

Archivio [*certificati spostato*](c-gly.md) dal percorso predefinito del Registro di sistema a un percorso diverso nel Registro di sistema.

</dd> <dt>

<span id="_security_remote_store_gly"></span><span id="_SECURITY_REMOTE_STORE_GLY"></span>**archivio remoto**
</dt> <dd>

Un [*archivio certificati che*](c-gly.md) si trova in un altro computer, ad esempio un file server o un altro computer remoto condiviso.

</dd> <dt>

<span id="_security_reply_apdu_gly"></span><span id="_SECURITY_REPLY_APDU_GLY"></span>**APDU di risposta**
</dt> <dd>

[*Un'unità dati del protocollo applicativo*](a-gly.md) (APDU) inviata in risposta a un'APDU ricevuta.

</dd> <dt>

<span id="_security_repudiation_gly"></span><span id="_SECURITY_REPUDIATION_GLY"></span>**Ripudio**
</dt> <dd>

Capacità di un utente di negare di aver eseguito una determinata azione in casi in cui risulta impossibile provare il contrario. Ad esempio, un utente che ha eliminato un file e che può negarlo correttamente.

</dd> <dt>

<span id="_security_resource_manager_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_GLY"></span>**resource manager**
</dt> <dd>

Il modulo del [*sottosistema smart card*](s-gly.md) che gestisce l'accesso a più lettori e smart card. Il gestore di risorse identifica e tiene traccia delle risorse, alloca lettori e risorse tra più applicazioni e supporta primitive di transazione per l'accesso ai servizi disponibili in una determinata scheda.

</dd> <dt>

<span id="_security_resource_manager_api_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_API_GLY"></span>**API di Resource Manager**
</dt> <dd>

Set di Windows che forniscono accesso diretto ai servizi del gestore di risorse.

</dd> <dt>

<span id="_security_resource_manager_context_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_CONTEXT_GLY"></span>**contesto di resource manager**
</dt> <dd>

Contesto usato dal gestore di risorse per l'accesso al database smart card database. Il contesto di resource manager viene usato principalmente dalle funzioni di query e gestione quando si accede al database. L'ambito del contesto di Gestione risorse può essere l'utente corrente o il sistema.

</dd> <dt>

<span id="_security_revocation_list_gly"></span><span id="_SECURITY_REVOCATION_LIST_GLY"></span>**elenco di revoche**
</dt> <dd>

Vedere [*Elenco di revoche di certificati.*](c-gly.md)

</dd> <dt>

<span id="_security_rid_gly"></span><span id="_SECURITY_RID_GLY"></span>**liberarsi**
</dt> <dd>

Vedere *l'identificatore relativo*.

</dd> <dt>

<span id="_security_root_authority_gly"></span><span id="_SECURITY_ROOT_AUTHORITY_GLY"></span>**autorità radice**
</dt> <dd>

Autorità [*di certificazione*](c-gly.md) (CA) all'inizio di una gerarchia di CA. L'autorità radice certifica le CA del livello immediatamente inferiore della gerarchia.

</dd> <dt>

<span id="_security_root_certificate_gly"></span><span id="_SECURITY_ROOT_CERTIFICATE_GLY"></span>**certificato radice**
</dt> <dd>

Certificato dell'autorità [*di certificazione*](c-gly.md) (CA) autofirmato che identifica una CA. Viene chiamato certificato radice perché è il certificato per la CA radice. La CA radice deve firmare il proprio certificato della CA perché, per definizione, non esiste un'autorità di certificazione superiore per firmare il certificato della CA.

</dd> <dt>

<span id="_security_rsa_gly"></span><span id="_SECURITY_RSA_GLY"></span>**Rsa**
</dt> <dd>

RSA Data Security, Inc., uno sviluppatore e un editore di standard [*PKCS (Public Key Cryptography Standards).*](p-gly.md) "RSA" nel nome è l'acronimo dei nomi dei tre sviluppatori e dei proprietari dell'azienda: Rivest, Shamir e Adleman.

</dd> <dt>

<span id="_security_rsa_keyx_gly"></span><span id="_SECURITY_RSA_KEYX_GLY"></span>**RSA \_ KEYX**
</dt> <dd>

Nome [*dell'algoritmo CryptoAPI*](c-gly.md) per l'algoritmo di scambio delle chiavi RSA. CryptoAPI fa riferimento a questo algoritmo anche tramite il relativo identificatore di algoritmo (CALG RSA KEYX) e la \_ \_ classe (ALG \_ CLASS KEY \_ \_ EXCHANGE).

</dd> <dt>

<span id="_security_rsa_sign_gly"></span><span id="_SECURITY_RSA_SIGN_GLY"></span>**RSA \_ SIGN**
</dt> <dd>

Nome dell'algoritmo CryptoAPI per l'algoritmo di firma RSA. CryptoAPI fa riferimento a questo algoritmo anche tramite il relativo identificatore di algoritmo (CALG \_ RSA \_ SIGN) e la classe (ALG \_ CLASS \_ SIGNATURE).

</dd> <dt>

<span id="_security_rsa_public_key_algorithm_gly"></span><span id="_SECURITY_RSA_PUBLIC_KEY_ALGORITHM_GLY"></span>**Algoritmo a chiave pubblica RSA**
</dt> <dd>

Algoritmo di scambio di chiavi e firma basato sulla crittografia a chiave pubblica RSA più diffusa. Questo algoritmo viene usato dai tipi di \_ provider SSL PROV RSA \_ FULL, PROV \_ RSA \_ SIG, PROV \_ MS EXCHANGE e \_ \_ PROV. CryptoAPI fa riferimento a questo algoritmo tramite i relativi identificatori (CALG RSA KEYX e CALG RSA SIGN), i nomi (RSA KEYX e RSA SIGN) e la \_ \_ classe \_ \_ \_ \_ (ALG \_ CLASS KEY \_ \_ EXCHANGE).

</dd> </dl>

 

 



