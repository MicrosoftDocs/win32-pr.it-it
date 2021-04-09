---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera M.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 4c4402e9-7455-4868-978f-3899a8fd86c1
title: M (Glossario sulla sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63fc76d4b8b803d523c46012dcb10ed5380e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967878"
---
# <a name="m-security-glossary"></a>M (Glossario sulla sicurezza)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) M [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_mac_gly"></span><span id="_SECURITY_MAC_GLY"></span>**MAC**
</dt> <dd>

Vedere *Message Authentication Code*.

</dd> <dt>

<span id="_security_mac_key_gly"></span><span id="_SECURITY_MAC_KEY_GLY"></span>**Chiave MAC**
</dt> <dd>

Chiave del codice di autenticazione del messaggio utilizzata con i protocolli [*Schannel*](s-gly.md) .

</dd> <dt>

<span id="_security_master_key_gly"></span><span id="_SECURITY_MASTER_KEY_GLY"></span>**chiave master**
</dt> <dd>

Chiave utilizzata dal client e dal server per la generazione di tutte le chiavi della sessione. La chiave master viene utilizzata per generare la chiave di lettura del client, la chiave di scrittura del client, la chiave di lettura del server e la chiave di scrittura del server. Le chiavi master possono essere esportate come semplici BLOB di chiavi.

</dd> <dt>

<span id="_security_md2_gly"></span><span id="_SECURITY_MD2_GLY"></span>**MD2**
</dt> <dd>

Nome dell'algoritmo CryptoAPI per l'algoritmo hash MD2. Gli altri algoritmi di hashing includono *MD4*, *MD5* e [*Sha*](s-gly.md).

Vedere anche *algoritmo MD2*.

</dd> <dt>

<span id="_security_md2_algorithm_gly"></span><span id="_SECURITY_MD2_ALGORITHM_GLY"></span>**Algoritmo MD2**
</dt> <dd>

MD2 Algoritmo di hashing che crea un valore hash a 128 bit. MD2 è stato ottimizzato per l'utilizzo con computer a 8 bit. CryptoAPI fa riferimento a questo algoritmo in base al tipo (CALG \_ MD2), al nome (Mac) e alla classe ( \_ hash della classe ALG \_ ). MD2 è stato sviluppato da RSA Data Security, Inc.

Vedere anche *algoritmo MD4*, *algoritmo MD5*.

</dd> <dt>

<span id="_security_md4_gly"></span><span id="_SECURITY_MD4_GLY"></span>**MD4**
</dt> <dd>

Nome dell'algoritmo CryptoAPI per l'algoritmo hash MD4. Gli altri algoritmi di hashing includono *MD2*, *MD5* e [*Sha*](s-gly.md).

Vedere *algoritmo MD4*.

</dd> <dt>

<span id="_security_md4_algorithm_gly"></span><span id="_SECURITY_MD4_ALGORITHM_GLY"></span>**Algoritmo MD4**
</dt> <dd>

MD4 Algoritmo di hashing che crea un valore hash a 128 bit. MD4 è stato ottimizzato per computer a 32 bit. È ora considerato rotto perché i conflitti possono essere trovati troppo rapidamente e facilmente. MD4 è stato sviluppato da RSA Data Security, Inc.

Vedere anche *algoritmo MD2*, *algoritmo MD5*.

</dd> <dt>

<span id="_security_md5_gly"></span><span id="_SECURITY_MD5_GLY"></span>**MD5**
</dt> <dd>

Nome dell'algoritmo CryptoAPI per l'algoritmo hash MD5. Gli altri algoritmi di hashing includono *MD2*, *MD4* e [*Sha*](s-gly.md).

Vedere anche *algoritmo MD5*.

</dd> <dt>

<span id="_security_md5_algorithm_gly"></span><span id="_SECURITY_MD5_ALGORITHM_GLY"></span>**Algoritmo MD5**
</dt> <dd>

MD5 Algoritmo di hashing che crea un valore hash a 128 bit. MD5 è stato ottimizzato per computer a 32 bit. CryptoAPI fa riferimento a questo algoritmo tramite il relativo identificatore di algoritmo (CALG \_ MD5), Name (MD5) e Class (ALG \_ Class \_ hash). MD5 è stato sviluppato da RSA Data Security, Inc. e viene specificato dai tipi di provider di prova RSA \_ \_ full, prov \_ RSA \_ sig, dimostra \_ DSS, prov \_ DSS \_ DH e prova \_ MS \_ Exchange.

Vedere anche *algoritmo MD2*, *algoritmo MD4*.

</dd> <dt>

<span id="_security_message_gly"></span><span id="_SECURITY_MESSAGE_GLY"></span>**Messaggio**
</dt> <dd>

Qualsiasi dato codificato per la trasmissione o la ricezione da una persona o da un'entità. I messaggi possono essere crittografati per la privacy, firmati digitalmente per scopi di autenticazione o entrambi.

</dd> <dt>

<span id="_security_message_digest_gly"></span><span id="_SECURITY_MESSAGE_DIGEST_GLY"></span>**digest del messaggio**
</dt> <dd>

Vedere [*hash*](h-gly.md).

</dd> <dt>

<span id="_security_message_authentication_code_gly"></span><span id="_SECURITY_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**Message Authentication Code**
</dt> <dd>

Mac Algoritmo di hash con chiave che utilizza una chiave di sessione simmetrica per garantire che un blocco di dati abbia mantenuto l'integrità dal momento in cui è stato inviato fino al momento in cui è stato ricevuto. Quando si utilizza questo tipo di algoritmo, l'applicazione ricevente deve disporre anche della chiave della sessione per ricalcolare il valore hash in modo da poter verificare che i dati di base non siano stati modificati. CryptoAPI fa riferimento a questo algoritmo in base al tipo (CALG \_ Mac), al nome (Mac) e alla classe ( \_ hash della classe ALG \_ ).

</dd> <dt>

<span id="_security_message_encoding_type_gly"></span><span id="_SECURITY_MESSAGE_ENCODING_TYPE_GLY"></span>**tipo di codifica messaggi**
</dt> <dd>

Definisce la modalità di codifica del messaggio. Il tipo di codifica dei messaggi viene archiviato nella parola più ordinata della struttura del tipo di codifica. I tipi di codifica definiti attualmente sono: CRYPT \_ ASN \_ Encoding, X509 \_ ASN \_ Encoding e PKCS \_ 7 \_ ASN \_ Encoding.

</dd> <dt>

<span id="_security_message_management_functions_gly"></span><span id="_SECURITY_MESSAGE_MANAGEMENT_FUNCTIONS_GLY"></span>**funzioni di gestione dei messaggi**
</dt> <dd>

Funzioni che forniscono due livelli di gestione dei messaggi: funzioni di messaggio di basso livello e funzioni di messaggio semplificate. Le funzioni di messaggio di basso livello offrono maggiore flessibilità rispetto alle funzioni di messaggio semplificate. Tuttavia, richiedono più chiamate di funzione.

</dd> <dt>

<span id="_security_message_signing_functions_gly"></span><span id="_SECURITY_MESSAGE_SIGNING_FUNCTIONS_GLY"></span>**funzioni di firma del messaggio**
</dt> <dd>

Funzioni utilizzate per firmare messaggi e dati.

Vedere anche [*funzioni di messaggio semplificate*](s-gly.md).

</dd> <dt>

<span id="_security_mpr_gly"></span><span id="_SECURITY_MPR_GLY"></span>**MPR**
</dt> <dd>

Vedere *più router del provider*.

</dd> <dt>

<span id="_security_multiple_provider_router_gly"></span><span id="_SECURITY_MULTIPLE_PROVIDER_ROUTER_GLY"></span>**Router per più provider**
</dt> <dd>

MPR Componente di sistema che gestisce le comunicazioni tra il sistema e tutti i provider di rete. Il MPR chiama le funzioni del provider di rete esposte da ogni provider di rete.

</dd> </dl>

 

 



