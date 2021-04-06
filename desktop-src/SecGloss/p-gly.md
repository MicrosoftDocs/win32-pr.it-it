---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a
title: P (Glossario sulla sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd5b580295c35bc021ade53d3cb922ce8fe13d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883274"
---
# <a name="p-security-glossary"></a>P (Glossario sulla sicurezza)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**imbottitura**
</dt> <dd>

Stringa in genere aggiunta quando l'ultimo blocco di testo non crittografato è breve. Ad esempio, se la lunghezza del blocco è 64 bit e l'ultimo blocco contiene solo 40 bit, è necessario aggiungere 24 bit di riempimento all'ultimo blocco. La stringa di riempimento può contenere zeri, zeri alternati o altri criteri. Le applicazioni che usano [*CryptoAPI*](c-gly.md) non devono aggiungere spaziatura interna al testo non crittografato prima di essere crittografati, né devono essere rimossi dopo la decrittografia. Questa operazione viene gestita automaticamente.

</dd> <dt>

<span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**filtro password**
</dt> <dd>

Una DLL che fornisce l'applicazione dei criteri password e la notifica delle modifiche. Le funzioni implementate dai filtri password vengono chiamate dall' [*autorità di sicurezza locale*](l-gly.md).

</dd> <dt>

<span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**archiviazione permanente**
</dt> <dd>

Qualsiasi supporto di archiviazione che rimanga intatto quando viene scollegata l'alimentazione. Molti database dell' [*archivio certificati*](c-gly.md) sono formati di archiviazione permanente.

</dd> <dt>

<span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**
</dt> <dd>

Vedere *standard di crittografia a chiave pubblica*.

</dd> <dt>

<span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**
</dt> <dd>

Gli standard consigliati per l'implementazione della crittografia a chiave pubblica basata sull'algoritmo RSA come definito nella [specifica RFC 3447](https://tools.ietf.org/html/rfc3447).

</dd> <dt>

<span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**
</dt> <dd>

Lo standard della sintassi scambio informazioni personali, sviluppato e gestito da RSA Data Security, Inc. Questo standard di sintassi specifica un formato portabile per archiviare o trasferire le chiavi private, i certificati e i segreti esterni di un utente.

Vedere anche [*certificati*](c-gly.md) e *standard di crittografia a chiave pubblica*.

</dd> <dt>

<span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**\#Dati firmati PKCS 7**
</dt> <dd>

Oggetto dati firmato con la chiave pubblica Cryptography Standard \# 7 (PKCS \# 7) e che incapsula le informazioni utilizzate per firmare un file. In genere include il certificato del firmatario e il [*certificato radice*](r-gly.md).

</dd> <dt>

<span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**
</dt> <dd>

Standard della sintassi dei messaggi crittografati. Si tratta di una sintassi generale per dati crittografabili, come firme digitali e crittografia, Viene inoltre fornita una sintassi per la divulgazione di certificati, elenchi di revoche di certificati e altri attributi del messaggio, ad esempio timestamp, al messaggio.

</dd> <dt>

<span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**\_ \_ Codifica ASN 7 \_ ASN**
</dt> <dd>

[*Tipo di codifica del messaggio*](m-gly.md). I tipi di codifica dei messaggi vengono archiviati nella parola più significativa di un valore **DWORD** (il valore è: 0x00010000).

</dd> <dt>

<span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**testo non crittografato**
</dt> <dd>

Messaggio di testo non crittografato.

</dd> <dt>

<span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Immagine PE (Portable Executable)**
</dt> <dd>

Formato eseguibile standard di Windows.

</dd> <dt>

<span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**
</dt> <dd>

Vedere *funzione pseudo-random*.

</dd> <dt>

<span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**credenziali primarie**
</dt> <dd>

Il \_ pacchetto di autenticazione MsV1 0 definisce un valore stringa Primary Credential Key: la stringa Primary Credentials include le credenziali specificate al momento dell'accesso iniziale. Include il nome utente e i form con distinzione tra maiuscole e minuscole e con distinzione tra maiuscole e minuscole della password dell'utente.

Vedere anche [*credenziali aggiuntive*](s-gly.md).

</dd> <dt>

<span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**provider di servizi primario**
</dt> <dd>

Provider di servizi che fornisce le interfacce di controllo alla scheda. Ogni smart card può registrare il proprio provider di servizi primario nel database delle smart card.

</dd> <dt>

<span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**token primario**
</dt> <dd>

Un token di accesso che viene in genere creato solo dal kernel di Windows. Può essere assegnato a un processo per rappresentare le informazioni di sicurezza predefinite per il processo.

Vedere anche [*token di accesso*](a-gly.md) e [*token di rappresentazione*](i-gly.md).

</dd> <dt>

<span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**principale**
</dt> <dd>

Vedere [*entità di sicurezza*](s-gly.md).

</dd> <dt>

<span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**privacy**
</dt> <dd>

Condizione di isolamento dalla vista o dal segreto. Per quanto riguarda i messaggi, i messaggi privati sono messaggi crittografati il cui testo è nascosto nella visualizzazione. Per quanto riguarda le chiavi, una chiave privata è una chiave segreta nascosta da altri.

</dd> <dt>

<span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**chiave privata**
</dt> <dd>

Metà segreta di una coppia di chiavi utilizzata in un algoritmo a chiave pubblica. Le chiavi private vengono in genere utilizzate per crittografare una chiave di sessione simmetrica, includere una firma digitale in un messaggio o decrittografare un messaggio crittografato con la chiave pubblica corrispondente.

Vedere anche *chiave pubblica*.

</dd> <dt>

<span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**BLOB della chiave privata**
</dt> <dd>

BLOB della chiave che contiene una coppia di chiavi pubblica/privata completa. I BLOB di chiavi private vengono utilizzati dai programmi amministrativi per trasportare coppie di chiavi. Poiché la parte della chiave privata della coppia di chiavi è estremamente riservata, questi BLOB vengono in genere mantenuti crittografati con una crittografia simmetrica. Questi BLOB di chiavi possono essere usati anche da applicazioni avanzate in cui le coppie di chiavi sono archiviate all'interno dell'applicazione, anziché basarsi sul meccanismo di archiviazione del CSP. Un BLOB di chiavi viene creato chiamando la funzione **CryptExportKey** .

</dd> <dt>

<span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**privilegio**
</dt> <dd>

Diritto di un utente a eseguire varie operazioni di sistema, come l'arresto del sistema, il caricamento dei driver di periferica o la modifica dell'ora del sistema. Il token di accesso di un utente contiene un elenco dei privilegi utilizzati dall'utente o dai gruppi dell'utente.

</dd> <dt>

<span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**processo**
</dt> <dd>

Contesto di sicurezza in cui un'applicazione viene eseguita. In genere, il contesto di sicurezza è associato a un utente, pertanto tutte le applicazioni che sono in esecuzione all'interno di un dato processo ereditano le autorizzazioni e i privilegi dell'utente che le possiede.

</dd> <dt>

<span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**PROVA \_ DSS**
</dt> <dd>

Vedere *\_ tipo di provider prov DSS*.

</dd> <dt>

<span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**\_Tipo di provider prov DSS**
</dt> <dd>

Tipo di provider predefinito che supporta solo firme digitali e hash. Specifica l'algoritmo di firma DSA e gli algoritmi di hash MD5 e SHA-1.

</dd> <dt>

<span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**PROVA \_ DSS \_ DH**
</dt> <dd>

Vedere *tipo di provider di prova \_ DSS \_ DH*.

</dd> <dt>

<span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**\_Tipo di \_ provider prov DSS DH**
</dt> <dd>

Tipo di provider predefinito che fornisce gli algoritmi di scambio di chiave, firma digitale e hash. È simile al \_ tipo di provider prov DSS.

</dd> <dt>

<span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**PROVA \_ fortezza**
</dt> <dd>

Vedere *il \_ tipo di provider prova fortezza*.

</dd> <dt>

<span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**Tipo di provider dimostrativo \_**
</dt> <dd>

Tipo di provider predefinito che fornisce gli algoritmi di scambio di chiave, firma digitale, crittografia e hash. I protocolli di crittografia e gli algoritmi specificati da questo tipo di provider sono di proprietà del National Institute of Standards and Technology (NIST).

</dd> <dt>

<span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROVA \_ MS \_ Exchange**
</dt> <dd>

Vedere *tipo di provider di prova \_ MS \_ Exchange*.

</dd> <dt>

<span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**Tipo di provider di prova \_ MS \_ Exchange**
</dt> <dd>

Tipo di provider predefinito progettato per le esigenze di Microsoft Exchange, nonché altre applicazioni compatibili con Microsoft Mail. Fornisce lo scambio di chiave, la firma digitale, la crittografia e gli algoritmi di hash.

</dd> <dt>

<span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROV \_ RSA \_ completo**
</dt> <dd>

Vedere *\_ tipo di \_ provider completo RSA di prova*.

</dd> <dt>

<span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**\_Tipo di \_ provider completo RSA di prova**
</dt> <dd>

Tipo di provider predefinito definito da Microsoft e RSA Data Security, Inc. Questo tipo di provider per utilizzo generico fornisce gli algoritmi di scambio di chiave, firma digitale, crittografia e hash. Gli algoritmi di scambio di chiave, firma digitale e crittografia sono basati sulla crittografia a chiave pubblica RSA.

</dd> <dt>

<span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROVA \_ RSA \_ sig**
</dt> <dd>

Vedere *il \_ tipo di provider prov RSA \_ sig*.

</dd> <dt>

<span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**\_Tipo di \_ provider prov RSA Sig**
</dt> <dd>

Tipo di provider predefinito definito da Microsoft e dalla sicurezza dei dati RSA. Questo tipo di provider è un subset di prova \_ RSA \_ full che fornisce solo algoritmi di firma digitale e hash. L'algoritmo di firma digitale è un algoritmo di chiave pubblica RSA.

</dd> <dt>

<span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**PROVA \_ SSL**
</dt> <dd>

Vedere *\_ tipo di provider di prova SSL*.

</dd> <dt>

<span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**Tipo di provider di prova \_ SSL**
</dt> <dd>

Tipo di provider predefinito che supporta il protocollo Secure Sockets Layer (SSL). Questo tipo fornisce la crittografia chiave, la firma digitale, la crittografia e gli algoritmi di hash. Una specifica che spiega SSL è disponibile in Netscape Communications Corp.

</dd> <dt>

<span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**provider**
</dt> <dd>

Vedere [*provider del servizio di crittografia*](c-gly.md).

</dd> <dt>

<span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**Nome provider**
</dt> <dd>

Nome utilizzato per identificare un CSP. Ad esempio, la versione 1,0 del provider di crittografia di base di Microsoft. Il nome del provider viene in genere utilizzato quando si chiama la funzione **CryptAcquireContext** per la connessione a un CSP.

</dd> <dt>

<span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**tipo di provider**
</dt> <dd>

Termine utilizzato per identificare un tipo di provider del servizio di crittografia (CSP). I CSP sono raggruppati in tipi di provider diversi che rappresentano famiglie specifiche di protocolli e formati di dati standard. Diversamente dal nome del provider univoco del CSP, i tipi di provider non sono univoci per un determinato CSP. Il tipo di provider viene in genere utilizzato quando si chiama la funzione **CryptAcquireContext** per la connessione a un CSP.

</dd> <dt>

<span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**funzione pseudo-random**
</dt> <dd>

PRF Funzione che accetta una chiave, un'etichetta e un valore di inizializzazione come input, quindi produce un output di lunghezza arbitraria.

</dd> <dt>

<span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**coppia di chiavi pubblica/privata**
</dt> <dd>

Coppia di chiavi di crittografia utilizzata nella crittografia a chiave pubblica. Per ogni utente, un CSP gestisce in genere due coppie di chiavi pubbliche/private, ovvero una coppia di chiavi di scambio e una coppia di chiavi di firma digitale. Entrambe le coppie di chiavi vengono mantenute di sessione in sessione.

Vedere coppia di [*chiavi di scambio*](e-gly.md) e coppia di [*chiavi di firma*](s-gly.md).

</dd> <dt>

<span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**chiave pubblica**
</dt> <dd>

Chiave di crittografia in genere utilizzata per decrittografare una chiave di sessione o una firma digitale. La chiave pubblica può inoltre essere utilizzata per crittografare un messaggio in modo che possa essere decrittografato soltanto tramite la chiave privata corrispondente.

Vedere anche *chiave privata*.

</dd> <dt>

<span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**algoritmo a chiave pubblica**
</dt> <dd>

Crittografia asimmetrica che utilizza due chiavi, una per la crittografia, la chiave pubblica e l'altra per la decrittografia, la chiave privata. Come implicito dai nomi delle chiavi, la chiave pubblica usata per codificare il testo non crittografato può essere resa disponibile a chiunque. Tuttavia, la chiave privata deve rimanere segreta. Solo la chiave privata può decrittografare il testo crittografato. L'algoritmo di chiave pubblica usato in questo processo è lento (nell'ordine di 1.000 volte più lento rispetto agli algoritmi simmetrici) e viene in genere usato per crittografare le chiavi di sessione o per firmare digitalmente un messaggio.

Vedere anche *chiave pubblica* e *chiave privata*.

</dd> <dt>

<span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**BLOB a chiave pubblica**
</dt> <dd>

BLOB utilizzato per archiviare la parte della chiave pubblica di una coppia di chiavi pubblica/privata. I BLOB di chiave pubblica non vengono crittografati perché la chiave pubblica contenuta in non è segreta. Un BLOB di chiave pubblica viene creato chiamando la funzione **CryptExportKey** .

</dd> <dt>

<span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Standard di crittografia a chiave pubblica**
</dt> <dd>

PKCS Set di standard di sintassi per la crittografia a chiave pubblica che copre le funzioni di sicurezza, inclusi i metodi per la firma dei dati, lo scambio di chiavi, la richiesta di certificati, la crittografia e la decrittografia a chiave pubblica e altre funzioni di sicurezza.

</dd> <dt>

<span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**crittografia a chiave pubblica**
</dt> <dd>

Crittografia basata su una coppia di chiavi, una per crittografare i dati e l'altra per decrittografarli. Gli algoritmi di crittografia simmetrica utilizzano invece un'unica chiave sia per crittografare sia per decrittografare i dati. In pratica, la crittografia a chiave pubblica viene in genere usata per proteggere la chiave di sessione usata da un algoritmo di crittografia simmetrico. In questo caso, la chiave pubblica viene utilizzata per crittografare la chiave di sessione che a sua volta è stata utilizzata per crittografare i dati, mentre la chiave privata viene utilizzata per la decrittografia. Oltre a proteggere le chiavi di sessione, la crittografia a chiave pubblica può essere utilizzata per includere una firma digitale in un messaggio (tramite la chiave privata) e convalidare tale firma (tramite la chiave pubblica).

Vedere anche *algoritmo a chiave pubblica*.

</dd> </dl>

 

 



