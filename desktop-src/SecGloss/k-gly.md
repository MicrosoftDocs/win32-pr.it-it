---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera K.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f17042c3-ba1a-408f-af55-5f171b0dee33
title: K (Glossario della sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c92abf9b3df1eb49f0caaee90ccbce8755d003478683aba35570d9ea99fa2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895594"
---
# <a name="k-security-glossary"></a>K (Glossario della sicurezza)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J K [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P Q](p-gly.md) R [](r-gly.md) [S](s-gly.md) [T U](t-gly.md) [](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_kca_gly"></span><span id="_SECURITY_KCA_GLY"></span>**Kca**
</dt> <dd>

Vedere *Autorità di certificazione della chiave*.

</dd> <dt>

<span id="_security_kdc_gly"></span><span id="_SECURITY_KDC_GLY"></span>**Kdc**
</dt> <dd>

Vedere *Centro distribuzione chiavi*.

</dd> <dt>

<span id="_security_kea_gly"></span><span id="_SECURITY_KEA_GLY"></span>**Kea**
</dt> <dd>

Vedere *Algoritmo di scambio di chiavi*.

</dd> <dt>

<span id="_security_kerberos_protocol_gly"></span><span id="_SECURITY_KERBEROS_PROTOCOL_GLY"></span>**Protocollo Kerberos**
</dt> <dd>

Protocollo che definisce la modalità di interazione fra i client e il servizio di autenticazione di rete. I client ottengono ticket dal centro di distribuzione chiave Kerberos (KDC, Kerberos Key Distribution Center) e quindi presentano questi ticket ai server durante la procedura di connessione. I ticket Kerberos rappresentano le credenziali di rete del client.

</dd> <dt>

<span id="_security_key_blob_gly"></span><span id="_SECURITY_KEY_BLOB_GLY"></span>**BLOB di chiavi**
</dt> <dd>

BLOB contenente una chiave privata crittografata. I BLOB delle chiavi consentono di archiviare le chiavi all'esterno di CSP. I BLOB delle chiavi vengono creati esportando una chiave esistente dal provider di servizi di crittografia chiamando la **funzione CryptExportKey.** Successivamente, il BLOB della chiave può essere importato in un provider (spesso un provider CSP diverso in un computer diverso) chiamando la funzione **CryptImportKey.** Verrà creata una chiave nel provider di servizi di configurazione che è un duplicato di quella esportata.

Vedere anche [*BLOB di chiave*](s-gly.md)semplice, BLOB di [*chiave*](p-gly.md)pubblica e BLOB di [*chiave privata.*](p-gly.md)

</dd> <dt>

<span id="_security_key_blob_format_gly"></span><span id="_SECURITY_KEY_BLOB_FORMAT_GLY"></span>**formato BLOB di chiavi**
</dt> <dd>

Formato del BLOB della chiave quando una chiave pubblica o di sessione viene esportata da un provider di servizi di configurazione. Il formato viene specificato dal tipo di provider del provider CSP esportatore. Un BLOB di chiavi viene creato chiamando **CryptExportKey**.

Vedere anche [*BLOB di chiave pubblica*](p-gly.md) e BLOB di chiave [*semplice.*](s-gly.md)

</dd> <dt>

<span id="_security_key_certification_authority_gly"></span><span id="_SECURITY_KEY_CERTIFICATION_AUTHORITY_GLY"></span>**autorità di certificazione della chiave**
</dt> <dd>

(KCA) Entità attendibile che in genere mantiene un database sicuro di messaggi composti firmati con la chiave privata del KCA. Nelle implementazioni pratiche, i messaggi composti sono costituiti dal nome dell'utente, dalla chiave pubblica dell'utente e da qualsiasi altra informazione importante sull'utente. Quando l'applicazione ricevente ottiene un messaggio firmato da un utente, l'applicazione può quindi verificare la chiave pubblica ricevuta con il messaggio confrontandolo con la chiave pubblica archiviata nel database KCA.

</dd> <dt>

<span id="_security_key_container_gly"></span><span id="_SECURITY_KEY_CONTAINER_GLY"></span>**contenitore di chiavi**
</dt> <dd>

Parte del database delle chiavi che contiene tutte le coppie di chiavi (coppie di chiavi di scambio e firma) appartenenti a un utente specifico. Ogni contenitore ha un nome univoco che viene usato quando si chiama la funzione **CryptAcquireContext** per ottenere un handle per il contenitore.

</dd> <dt>

<span id="_security_key_database_gly"></span><span id="_SECURITY_KEY_DATABASE_GLY"></span>**database delle chiavi**
</dt> <dd>

Database che contiene le chiavi crittografiche persistenti per un provider di servizi di configurazione specifico. Il database contiene uno o più contenitori di chiavi, che archiviano singolarmente tutte le coppie di chiavi crittografiche per un utente specifico.

Vedere anche *contenitore di chiavi*.

</dd> <dt>

<span id="_security_key_distribution_center_gly"></span><span id="_SECURITY_KEY_DISTRIBUTION_CENTER_GLY"></span>**Centro distribuzione chiavi**
</dt> <dd>

(KDC) Servizio di rete che fornisce ticket di sessione e chiavi di sessione temporanee usate nel protocollo di autenticazione Kerberos V5. Il KDC viene eseguito come processo con privilegi in tutti i controller di dominio.

Vedere anche *Protocollo Kerberos*.

</dd> <dt>

<span id="_security_key_exchange_algorithm_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_GLY"></span>**algoritmo di scambio di chiavi**
</dt> <dd>

Algoritmo usato per crittografare e decrittografare le chiavi di scambio (chiavi di sessione simmetriche). Alcuni algoritmi di scambio di chiavi comuni includono Diffie-Hellman e KEA, l'algoritmo di scambio di chiavi specificato da un tipo di provider PROV \_ FORTEZZA. L'algoritmo KEA è una versione migliorata dell'Diffie-Hellman. Ogni tipo di provider può specificare un solo algoritmo di scambio delle chiavi.

</dd> <dt>

<span id="_security_key_exchange_algorithm_name_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_NAME_GLY"></span>**Algoritmo Exchange chiave**
</dt> <dd>

(KEA) Algoritmo di scambio di chiavi specificato da un tipo di provider PROV \_ FORTEZZA. Questo algoritmo è una versione migliorata dell'algoritmo Diffie-Hellman.

</dd> <dt>

<span id="_security_key_exchange_certificate_gly"></span><span id="_SECURITY_KEY_EXCHANGE_CERTIFICATE_GLY"></span>**certificato di scambio di chiavi**
</dt> <dd>

Certificato usato per crittografare le informazioni inviate a un'altra parte. Il certificato di scambio delle chiavi dell'autorità di certificazione (CA) può essere usato da un client per crittografare le informazioni inviate alla CA.

</dd> <dt>

<span id="_security_key_exchange_functions_gly"></span><span id="_SECURITY_KEY_EXCHANGE_FUNCTIONS_GLY"></span>**funzioni di scambio delle chiavi**
</dt> <dd>

Set di funzioni utilizzate per scambiare o trasmettere chiavi. Le funzioni di scambio delle chiavi possono essere usate anche per implementare scambi di chiavi in tre fasi completamente autenticati.

</dd> <dt>

<span id="_security_key_exchange_key_pair_gly"></span><span id="_SECURITY_KEY_EXCHANGE_KEY_PAIR_GLY"></span>**coppia di chiavi di scambio di chiavi**
</dt> <dd>

Vedere [*Coppia di chiavi di scambio*](e-gly.md).

</dd> <dt>

<span id="_security_key_exchange_private_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PRIVATE_KEY_GLY"></span>**chiave privata di scambio di chiavi**
</dt> <dd>

Chiave privata di una coppia di chiavi di scambio.

Vedere anche [*Scambiare una coppia di chiavi.*](e-gly.md)

</dd> <dt>

<span id="_security_key_exchange_protocol_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PROTOCOL_GLY"></span>**protocollo di scambio delle chiavi**
</dt> <dd>

Protocollo con cui due parti scambiano informazioni per stabilire un segreto condiviso. Il segreto condiviso viene quindi in genere usato come chiave di crittografia simmetrica.

</dd> <dt>

<span id="_security_key_exchange_public_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PUBLIC_KEY_GLY"></span>**chiave pubblica di scambio di chiavi**
</dt> <dd>

Chiave pubblica di una coppia di chiavi di scambio.

Vedere anche [*Scambiare una coppia di chiavi.*](e-gly.md)

</dd> <dt>

<span id="_security_key_generation_functions_gly"></span><span id="_SECURITY_KEY_GENERATION_FUNCTIONS_GLY"></span>**funzioni di generazione delle chiavi**
</dt> <dd>

Set di funzioni usate dalle applicazioni per generare e personalizzare le chiavi crittografiche. Queste funzioni includono il supporto completo per la modifica delle modalità di concatenamento, dei vettori di inizializzazione e di altre funzionalità di crittografia.

</dd> <dt>

<span id="_security_key_length_gly"></span><span id="_SECURITY_KEY_LENGTH_GLY"></span>**lunghezza della chiave**
</dt> <dd>

Valori specificati da alcuni provider che indicano la lunghezza delle coppie di chiavi pubblica/privata e delle chiavi di sessione usate con tale provider.

</dd> <dt>

<span id="_security_key_pair_gly"></span><span id="_SECURITY_KEY_PAIR_GLY"></span>**coppia di chiavi**
</dt> <dd>

Una chiave privata e la chiave pubblica correlata.

</dd> <dt>

<span id="_security_key_storage_provider_gly"></span><span id="_SECURITY_KEY_STORAGE_PROVIDER_GLY"></span>**provider di archiviazione chiavi**
</dt> <dd>

(KSP) Modulo software indipendente che implementa la funzionalità per creare, gestire, archiviare e recuperare [*chiavi private.*](p-gly.md)

</dd> <dt>

<span id="_security_ksp_gly"></span><span id="_SECURITY_KSP_GLY"></span>**Ksp**
</dt> <dd>

Vedere *Provider di archiviazione chiavi*.

</dd> </dl>

 

 



