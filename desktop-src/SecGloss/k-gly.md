---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera K.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f17042c3-ba1a-408f-af55-5f171b0dee33
title: K (Glossario sulla sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e7d1b474b774b5cdb7a0b8d05a512a8d291573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967880"
---
# <a name="k-security-glossary"></a>K (Glossario sulla sicurezza)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J K [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_kca_gly"></span><span id="_SECURITY_KCA_GLY"></span>**KCA**
</dt> <dd>

Vedere *autorità di certificazione principale*.

</dd> <dt>

<span id="_security_kdc_gly"></span><span id="_SECURITY_KDC_GLY"></span>**KDC**
</dt> <dd>

Vedere *centro distribuzione chiavi*.

</dd> <dt>

<span id="_security_kea_gly"></span><span id="_SECURITY_KEA_GLY"></span>**KEA**
</dt> <dd>

Vedere *algoritmo di scambio delle chiavi*.

</dd> <dt>

<span id="_security_kerberos_protocol_gly"></span><span id="_SECURITY_KERBEROS_PROTOCOL_GLY"></span>**Protocollo Kerberos**
</dt> <dd>

Protocollo che definisce la modalità di interazione fra i client e il servizio di autenticazione di rete. I client ottengono ticket dal centro di distribuzione chiave Kerberos (KDC, Kerberos Key Distribution Center) e quindi presentano questi ticket ai server durante la procedura di connessione. I ticket Kerberos rappresentano le credenziali di rete del client.

</dd> <dt>

<span id="_security_key_blob_gly"></span><span id="_SECURITY_KEY_BLOB_GLY"></span>**BLOB della chiave**
</dt> <dd>

BLOB contenente una chiave privata crittografata. I BLOB principali consentono di archiviare le chiavi all'esterno del CSP. I BLOB di chiavi vengono creati esportando una chiave esistente dal CSP chiamando la funzione **CryptExportKey** . Successivamente, il BLOB della chiave può essere importato in un provider (spesso un CSP diverso in un computer diverso) chiamando la funzione **CryptImportKey** . Viene creata una chiave nel CSP che è un duplicato di quello che è stato esportato.

Vedere anche un BLOB di chiavi [*semplice*](s-gly.md), un BLOB di [*chiavi pubbliche*](p-gly.md)e un [*BLOB di chiavi private*](p-gly.md).

</dd> <dt>

<span id="_security_key_blob_format_gly"></span><span id="_SECURITY_KEY_BLOB_FORMAT_GLY"></span>**formato BLOB chiave**
</dt> <dd>

Il formato del BLOB della chiave quando una chiave pubblica o di sessione viene esportata da un CSP. Il formato è specificato dal tipo di provider del CSP di esportazione. Un BLOB di chiavi viene creato chiamando **CryptExportKey**.

Vedere anche [*BLOB di chiavi pubbliche*](p-gly.md) e [*BLOB di chiavi semplici*](s-gly.md).

</dd> <dt>

<span id="_security_key_certification_authority_gly"></span><span id="_SECURITY_KEY_CERTIFICATION_AUTHORITY_GLY"></span>**autorità di certificazione chiave**
</dt> <dd>

KCA Entità attendibile che in genere mantiene un database protetto di messaggi composti firmati con la chiave privata del KCA. Nelle implementazioni pratiche, i messaggi composti sono costituiti dal nome dell'utente, dalla chiave pubblica dell'utente e da qualsiasi altra informazione importante relativa all'utente. Quando l'applicazione ricevente riceve un messaggio firmato da un utente, l'applicazione può quindi verificare la chiave pubblica ricevuta con il messaggio confrontandolo con la chiave pubblica archiviata nel database KCA.

</dd> <dt>

<span id="_security_key_container_gly"></span><span id="_SECURITY_KEY_CONTAINER_GLY"></span>**contenitore di chiavi**
</dt> <dd>

Parte del database chiave che contiene tutte le coppie di chiavi (coppie di chiavi di scambio e firma) appartenenti a un utente specifico. Ogni contenitore ha un nome univoco che viene usato quando si chiama la funzione **CryptAcquireContext** per ottenere un handle per il contenitore.

</dd> <dt>

<span id="_security_key_database_gly"></span><span id="_SECURITY_KEY_DATABASE_GLY"></span>**database chiave**
</dt> <dd>

Database contenente le chiavi crittografiche permanenti per un CSP specifico. Il database contiene uno o più contenitori di chiavi, che archiviano singolarmente tutte le coppie di chiavi crittografiche per un utente specifico.

Vedere anche *contenitore di chiavi*.

</dd> <dt>

<span id="_security_key_distribution_center_gly"></span><span id="_SECURITY_KEY_DISTRIBUTION_CENTER_GLY"></span>**Centro distribuzione chiavi**
</dt> <dd>

KDC Servizio di rete che fornisce ticket di sessione e chiavi di sessione temporanee utilizzate nel protocollo di autenticazione Kerberos V5. Il KDC viene eseguito come processo con privilegi in tutti i controller di dominio.

Vedere anche il *protocollo Kerberos*.

</dd> <dt>

<span id="_security_key_exchange_algorithm_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_GLY"></span>**algoritmo di scambio delle chiavi**
</dt> <dd>

Algoritmo utilizzato per crittografare e decrittografare le chiavi di scambio (chiavi della sessione simmetrica). Alcuni algoritmi di scambio di chiave comuni includono Diffie-Hellman e KEA, l'algoritmo di scambio delle chiavi specificato da un tipo di provider di prova \_ fortezza. L'algoritmo KEA è una versione migliorata dell'algoritmo Diffie-Hellman. Ogni tipo di provider può specificare un solo algoritmo di scambio di chiave.

</dd> <dt>

<span id="_security_key_exchange_algorithm_name_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_NAME_GLY"></span>**Algoritmo di scambio delle chiavi**
</dt> <dd>

Kea Algoritmo di scambio delle chiavi specificato da un \_ tipo di provider provo. Questo algoritmo è una versione migliorata dell'algoritmo Diffie-Hellman.

</dd> <dt>

<span id="_security_key_exchange_certificate_gly"></span><span id="_SECURITY_KEY_EXCHANGE_CERTIFICATE_GLY"></span>**certificato di scambio delle chiavi**
</dt> <dd>

Certificato utilizzato per crittografare le informazioni inviate a un'altra entità. Il certificato di scambio delle chiavi dell'autorità di certificazione (CA) può essere usato da un client per crittografare le informazioni inviate alla CA.

</dd> <dt>

<span id="_security_key_exchange_functions_gly"></span><span id="_SECURITY_KEY_EXCHANGE_FUNCTIONS_GLY"></span>**funzioni di scambio delle chiavi**
</dt> <dd>

Set di funzioni utilizzato per scambiare o trasmettere chiavi. Le funzioni di scambio di chiave possono essere usate anche per implementare scambi di chiavi a tre fasi completamente autenticati.

</dd> <dt>

<span id="_security_key_exchange_key_pair_gly"></span><span id="_SECURITY_KEY_EXCHANGE_KEY_PAIR_GLY"></span>**coppia di chiavi scambio di chiave**
</dt> <dd>

Vedere [*coppia di chiavi di scambio*](e-gly.md).

</dd> <dt>

<span id="_security_key_exchange_private_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PRIVATE_KEY_GLY"></span>**chiave privata per lo scambio delle chiavi**
</dt> <dd>

Chiave privata di una coppia di chiavi di scambio.

Vedere anche [*coppia di chiavi di scambio*](e-gly.md).

</dd> <dt>

<span id="_security_key_exchange_protocol_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PROTOCOL_GLY"></span>**protocollo di scambio delle chiavi**
</dt> <dd>

Protocollo con cui due entità scambiano informazioni per stabilire un segreto condiviso. Il segreto condiviso viene in genere usato come chiave di crittografia simmetrica.

</dd> <dt>

<span id="_security_key_exchange_public_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PUBLIC_KEY_GLY"></span>**chiave pubblica di scambio delle chiavi**
</dt> <dd>

Chiave pubblica di una coppia di chiavi di scambio.

Vedere anche [*coppia di chiavi di scambio*](e-gly.md).

</dd> <dt>

<span id="_security_key_generation_functions_gly"></span><span id="_SECURITY_KEY_GENERATION_FUNCTIONS_GLY"></span>**funzioni di generazione delle chiavi**
</dt> <dd>

Set di funzioni utilizzate dalle applicazioni per generare e personalizzare le chiavi crittografiche. Queste funzioni includono il supporto completo per la modifica delle modalità di concatenamento, i vettori di inizializzazione e altre funzionalità di crittografia.

</dd> <dt>

<span id="_security_key_length_gly"></span><span id="_SECURITY_KEY_LENGTH_GLY"></span>**lunghezza della chiave**
</dt> <dd>

Valori specificati da alcuni provider che indicano la lunghezza delle coppie di chiavi pubbliche/private e delle chiavi di sessione utilizzate con tale provider.

</dd> <dt>

<span id="_security_key_pair_gly"></span><span id="_SECURITY_KEY_PAIR_GLY"></span>**coppia di chiavi**
</dt> <dd>

Una chiave privata e la relativa chiave pubblica.

</dd> <dt>

<span id="_security_key_storage_provider_gly"></span><span id="_SECURITY_KEY_STORAGE_PROVIDER_GLY"></span>**provider di archiviazione chiavi**
</dt> <dd>

KSP Un modulo software indipendente che implementa la funzionalità per creare, gestire, archiviare e recuperare [*chiavi private*](p-gly.md).

</dd> <dt>

<span id="_security_ksp_gly"></span><span id="_SECURITY_KSP_GLY"></span>**KSP**
</dt> <dd>

Vedere *provider di archiviazione chiavi*.

</dd> </dl>

 

 



