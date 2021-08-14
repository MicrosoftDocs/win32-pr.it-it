---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera S.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e9d7672-2314-45c8-8178-5a0afcfd0c50
title: S (Glossario della sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99805289ca49b0505a1bbba292ec5fc7753e684aa08d4b5f0ac464f9160633ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969949"
---
# <a name="s-security-glossary"></a>S (Glossario della sicurezza)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P Q](p-gly.md) R [S](r-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_s_mime_gly"></span><span id="_SECURITY_S_MIME_GLY"></span>**S/MIME**
</dt> <dd>

Vedere *Secure/Multipurpose Internet Mail Extensions*.

</dd> <dt>

<span id="_security_sacl_gly"></span><span id="_SECURITY_SACL_GLY"></span>**Sacl**
</dt> <dd>

Vedere elenco *di controllo di accesso di sistema*.

</dd> <dt>

<span id="_security_salt_value_gly"></span><span id="_SECURITY_SALT_VALUE_GLY"></span>**valore salt**
</dt> <dd>

Dati casuali talvolta inclusi come parte di una chiave di sessione. Quando vengono aggiunti a una chiave di sessione, i dati salt di testo non crittografato vengono inseriti davanti ai dati della chiave crittografata. I valori salt vengono aggiunti per aumentare il lavoro necessario per montare un attacco di forza bruta (dizionario) contro i dati crittografati con una crittografia a chiave simmetrica. I valori salt vengono generati chiamando **CryptGenRandom**.

</dd> <dt>

<span id="_security_sam_gly"></span><span id="_SECURITY_SAM_GLY"></span>**Sam**
</dt> <dd>

Vedere *Gestione account di sicurezza*.

</dd> <dt>

<span id="_security_sanitized_name_gly"></span><span id="_SECURITY_SANITIZED_NAME_GLY"></span>**nome sanitizzato**
</dt> <dd>

Forma di un nome di autorità di certificazione (CA) utilizzato nei nomi di file (ad esempio per un elenco [*di revoche*](c-gly.md)di certificati) e nelle chiavi del Registro di sistema. Il processo di rimozione del nome della CA è necessario per rimuovere i caratteri non validi per nomi di file, nomi di chiavi del Registro di sistema o valori di nome distinto o non validi per motivi specifici della tecnologia. In Servizi certificati il processo di sanità converte qualsiasi carattere non valido nel nome comune della CA in una rappresentazione di 5 caratteri nel formato **!** _xxxx_, dove **!** viene usato come carattere di escape e *xxxx* rappresenta quattro numeri interi esadecimali che identificano in modo univoco il carattere convertito.

</dd> <dt>

<span id="security.s_1_gly"></span><span id="SECURITY.S_1_GLY"></span>**Sas**
</dt> <dd>

Vedere *la sequenza di attenzione sicura.*

</dd> <dt>

<span id="_security_scard_defaultreaders_gly"></span><span id="_SECURITY_SCARD_DEFAULTREADERS_GLY"></span>**SCard$DefaultReaders**
</dt> <dd>

Un gruppo di lettori del terminale che contiene tutti i lettori assegnati a tale terminale, tuttavia, non è riservato per questo uso specifico.

</dd> <dt>

<span id="_security_scard_allreaders_gly"></span><span id="_SECURITY_SCARD_ALLREADERS_GLY"></span>**SCard$AllReaders**
</dt> <dd>

Un smart card di lettura a livello di sistema che include tutti i lettori introdotti smart card resource manager. I lettori vengono aggiunti automaticamente al gruppo quando vengono introdotti nel sistema.

</dd> <dt>

<span id="_security_scard_autoallocate_gly"></span><span id="_SECURITY_SCARD_AUTOALLOCATE_GLY"></span>**SCARD \_ AUTOALLOCATE**
</dt> <dd>

Costante smart card di sistema che indica al gestore delle risorse smart card di allocare memoria sufficiente, restituisce un puntatore al buffer allocato anziché compilare un buffer fornito dall'utente. Il buffer restituito deve quindi essere liberato chiamando **SCardFreeMemory**.

</dd> <dt>

<span id="_security_scep_gly"></span><span id="_SECURITY_SCEP_GLY"></span>**SCEP**
</dt> <dd>

Vedere *Simple Certificate Enrollment Protocol*

</dd> <dt>

<span id="_security_schannel_gly"></span><span id="_SECURITY_SCHANNEL_GLY"></span>**Schannel**
</dt> <dd>

Pacchetto di sicurezza che fornisce l'autenticazione tra client e server.

</dd> <dt>

<span id="_security_secure_attention_sequence_gly"></span><span id="_SECURITY_SECURE_ATTENTION_SEQUENCE_GLY"></span>**sequenza di attenzione sicura**
</dt> <dd>

(firma di accesso condiviso) Sequenza di chiavi che avvia il processo di accesso o disconnessione. La sequenza predefinita è CTRL+ALT+CANC.

</dd> <dt>

<span id="_security_secure_electronic_transaction_gly"></span><span id="_SECURITY_SECURE_ELECTRONIC_TRANSACTION_GLY"></span>**Transazione elettronica sicura**
</dt> <dd>

(SET) Protocollo per transazioni elettroniche protette tramite Internet.

</dd> <dt>

<span id="_security_secure_hash_algorithm_gly"></span><span id="_SECURITY_SECURE_HASH_ALGORITHM_GLY"></span>**Algoritmo hash sicuro**
</dt> <dd>

(SHA) Algoritmo hash che genera un digest del messaggio. SHA è utilizzato insieme a molte tecnologie, fra cui l'algoritmo Digital Signature Algorithm (DSA) dello standard Digital Signature Standard (DSS). CryptoAPI fa riferimento a questo algoritmo tramite l'identificatore dell'algoritmo (CALG SHA), il nome \_ (SHA) e la classe (ALG \_ CLASS \_ HASH). Esistono quattro versioni di SHA: SHA-1, SHA-256, SHA-384 e SHA-512. SHA-1 genera un digest del messaggio a 160 bit. SHA-256, SHA-384 e SHA-512 generano rispettivamente un digest del messaggio a 256, 384 e 512 bit. SHA è stato sviluppato dall'istituto National Institute of Standards and Technology (NIST) e dall'agenzia National Security Agency (NSA).

</dd> <dt>

<span id="_security_secure_hash_standard_gly"></span><span id="_SECURITY_SECURE_HASH_STANDARD_GLY"></span>**Standard hash sicuro**
</dt> <dd>

Uno standard progettato da NIST e NSA. Questo standard definisce l'algoritmo SHA-1 (Secure Hash Algorithm) da usare con DSS (Digital Signature Standard).

Vedere anche *Secure Hash Algorithm*.

</dd> <dt>

<span id="_security_secure_sockets_layer_protocol_gly"></span><span id="_SECURITY_SECURE_SOCKETS_LAYER_PROTOCOL_GLY"></span>**Secure Sockets Layer protocollo**
</dt> <dd>

(SSL) Protocollo per le comunicazioni di rete protette usando una combinazione di tecnologia di chiave pubblica e privata.

</dd> <dt>

<span id="_security_secure_multipurpose_internet_mail_extensions_gly"></span><span id="_SECURITY_SECURE_MULTIPURPOSE_INTERNET_MAIL_EXTENSIONS_GLY"></span>**Sicurezza/Multipurpose Internet Mail Extensions**
</dt> <dd>

(S/MIME) Standard di sicurezza della posta elettronica che usa la crittografia a chiave pubblica.

</dd> <dt>

<span id="_security_security_accounts_manager_gly"></span><span id="_SECURITY_SECURITY_ACCOUNTS_MANAGER_GLY"></span>**Gestione account di sicurezza**
</dt> <dd>

(SAM) Un Windows usato durante il processo di accesso. SAM gestisce le informazioni sull'account utente, inclusi i gruppi a cui appartiene un utente.

</dd> <dt>

<span id="_security_security_context_gly"></span><span id="_SECURITY_SECURITY_CONTEXT_GLY"></span>**contesto di sicurezza**
</dt> <dd>

Attributi o regole di sicurezza correntemente applicati. Esempi di contesti di sicurezza sono l'utente connesso correntemente al computer o il codice PIN immesso da un utente di smart card. Per l'interfaccia SSPI, un contesto di sicurezza è una struttura non trasparente di dati che contiene dati di sicurezza relativi a una connessione, ad esempio una chiave di sessione o un'indicazione della durata della sessione.

</dd> <dt>

<span id="_security_security_descriptor_gly"></span><span id="_SECURITY_SECURITY_DESCRIPTOR_GLY"></span>**descrittore di sicurezza**
</dt> <dd>

Struttura e dati associati che contengono le informazioni di sicurezza per un oggetto a protezione diretta. Un descrittore di sicurezza identifica il proprietario e il gruppo primario dell'oggetto. Può anche contenere un elenco DACL che controlla l'accesso all'oggetto e un SACL che controlla la registrazione dei tentativi di accesso all'oggetto.

Vedere anche [*descrittore di sicurezza assoluto,*](a-gly.md)elenco di controllo di [*accesso discrezionale,*](d-gly.md)descrittore di *sicurezza self-relative,* *elenco di controllo di accesso di sistema.*

</dd> <dt>

<span id="_security_security_identifier_gly"></span><span id="_SECURITY_SECURITY_IDENTIFIER_GLY"></span>**identificatore di sicurezza**
</dt> <dd>

(SID) Struttura di dati di lunghezza variabile che identifica gli account utente, gruppo e computer. Ogni account in una rete viene emesso un SID univoco quando l'account viene creato per la prima volta. I processi interni in Windows si riferiscono al SID di un account anziché al nome dell'utente o del gruppo dell'account.

</dd> <dt>

<span id="_security_security_package_gly"></span><span id="_SECURITY_SECURITY_PACKAGE_GLY"></span>**pacchetto di sicurezza**
</dt> <dd>

Implementazione software di un protocollo di sicurezza. I pacchetti di sicurezza sono contenuti nelle DLL del provider di supporto della sicurezza o nelle DLL dei pacchetti di autenticazione/provider di supporto per la sicurezza.

</dd> <dt>

<span id="_security_security_protocol_gly"></span><span id="_SECURITY_SECURITY_PROTOCOL_GLY"></span>**protocollo di sicurezza**
</dt> <dd>

Specifica che definisce gli oggetti dati correlati alla sicurezza e le regole relative al modo in cui gli oggetti vengono usati per mantenere la sicurezza in un sistema informatico.

</dd> <dt>

<span id="_security_security_principal_gly"></span><span id="_SECURITY_SECURITY_PRINCIPAL_GLY"></span>**entità di sicurezza**
</dt> <dd>

Entità riconosciuta dal sistema di sicurezza. Le entità di sicurezza possono essere utenti o processi autonomi.

</dd> <dt>

<span id="_security_security_support_provider_gly"></span><span id="_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY"></span>**provider di supporto per la sicurezza**
</dt> <dd>

(provider di servizi condivisi) Libreria a collegamento dinamico (DLL) che implementa SSPI rendendo disponibili uno o più pacchetti di sicurezza per le applicazioni. Ogni pacchetto di sicurezza fornisce associazioni tra le chiamate di funzione dell'interfaccia SSPI di un'applicazione e le funzioni di un modello di sicurezza effettivo. I pacchetti di sicurezza supportano protocolli di sicurezza come l'autenticazione Kerberos e Microsoft LAN Manager.

</dd> <dt>

<span id="_security_security_support_provider_interface_gly"></span><span id="_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY"></span>**Interfaccia del provider di supporto per la sicurezza**
</dt> <dd>

(SSPI) Interfaccia comune tra applicazioni a livello di trasporto, ad esempio RPC (Remote Procedure Call) Microsoft, e provider di sicurezza, ad esempio Windows sicurezza distribuita. L'interfaccia SSPI consente a un'applicazione a livello di trasporto di chiamare uno dei diversi provider di sicurezza per ottenere una connessione autenticata. Queste chiamate non richiedono una conoscenza approfondita dei dettagli del protocollo di sicurezza.

</dd> <dt>

<span id="_security_self_relative_security_descriptor_gly"></span><span id="_SECURITY_SELF_RELATIVE_SECURITY_DESCRIPTOR_GLY"></span>**descrittore di sicurezza self-relative**
</dt> <dd>

Descrittore di sicurezza che archivia tutte le informazioni di sicurezza in un blocco contiguo di memoria.

Vedere anche *descrittore di sicurezza*.

</dd> <dt>

<span id="_security_serialize_gly"></span><span id="_SECURITY_SERIALIZE_GLY"></span>**Serializzare**
</dt> <dd>

Processo di conversione dei dati in una stringa di uno e zero in modo che possano essere trasmessi in serie. La codifica fa parte di questo processo.

</dd> <dt>

<span id="_security_serialized_certificate_store_format_gly"></span><span id="_SECURITY_SERIALIZED_CERTIFICATE_STORE_FORMAT_GLY"></span>**Formato dell'archivio certificati serializzato**
</dt> <dd>

(SST) Il formato archivio certificati serializzato è l'unico formato che mantiene tutte le proprietà dell'archivio certificati. È utile nei casi in cui le radici sono state configurate con proprietà EKU personalizzate e si vuole spostarle in un altro computer.

</dd> <dt>

<span id="_security_server_gly"></span><span id="_SECURITY_SERVER_GLY"></span>**Server**
</dt> <dd>

Computer che risponde ai comandi di un computer client. Il client e il server funzionano insieme per eseguire la funzionalità dell'applicazione distributiva.

Vedere anche [*client*](c-gly.md).

</dd> <dt>

<span id="_security_server_certificate_gly"></span><span id="_SECURITY_SERVER_CERTIFICATE_GLY"></span>**certificato server**
</dt> <dd>

Fa riferimento a un certificato utilizzato per l'autenticazione server, ad esempio l'autenticazione di un server Web in un Web browser. Quando un client Web browser tenta di accedere a un server Web protetto, il server invia il certificato al browser per consentire la verifica dell'identità del server.

</dd> <dt>

<span id="_security_server_gated_cryptography_gly"></span><span id="_SECURITY_SERVER_GATED_CRYPTOGRAPHY_GLY"></span>**crittografia con controllo del server**
</dt> <dd>

(SGC) Estensione di *Secure Sockets Layer* (SSL) che consente alle organizzazioni, ad esempio gli istituti finanziari, che hanno versioni di esportazione di Internet Information Services (IIS) di usare la crittografia avanzata, ad esempio la crittografia a 128 bit.

</dd> <dt>

<span id="_security_service_principal_name_gly"></span><span id="_SECURITY_SERVICE_PRINCIPAL_NAME_GLY"></span>**nome dell'entità servizio**
</dt> <dd>

(SPN) Nome con cui un client identifica in modo univoco un'istanza di un servizio. Se si installano più istanze di un servizio in computer distribuiti in una foresta, a ogni istanza deve essere associato un nome SPN distinto. Una determinata istanza del servizio può avere più nomi SPN se sono presenti più nomi che i client potrebbero usare per l'autenticazione

</dd> <dt>

<span id="_security_service_provider_smart_card__gly"></span><span id="_SECURITY_SERVICE_PROVIDER_SMART_CARD__GLY"></span>**provider di servizi (smart card)**
</dt> <dd>

Componente smart card sottosistema che fornisce l'accesso a smart card servizi tramite interfacce COM.

Vedere anche [*provider di servizi primario.*](p-gly.md)

</dd> <dt>

<span id="_security_session_gly"></span><span id="_SECURITY_SESSION_GLY"></span>**Sessione**
</dt> <dd>

Scambio di messaggi protetto mediante un solo elemento di materiale per le chiavi. Ad esempio, le sessioni SSL utilizzano un'unica chiave per proteggere lo scambio di più messaggi.

</dd> <dt>

<span id="_security_session_key_gly"></span><span id="_SECURITY_SESSION_KEY_GLY"></span>**chiave di sessione**
</dt> <dd>

Una chiave crittografica di durata relativamente breve, spesso negoziata da un client e un server basata su un segreto condiviso. La durata di una chiave di sessione è limitata dalla sessione a cui è associata. Una chiave di sessione deve essere sufficientemente forte da sostenere la crittografia per l'intervallo di vita della sessione. Quando vengono trasmesse, le chiavi di sessione sono in genere protette con chiavi di scambio delle chiavi (in genere chiavi asimmetriche) in modo che solo il destinatario previsto possa accedervi. Le chiavi di sessione possono essere derivate da valori hash chiamando la **funzione CryptDeriveKey.**

</dd> <dt>

<span id="_security_session_key_derivation_scheme_gly"></span><span id="_SECURITY_SESSION_KEY_DERIVATION_SCHEME_GLY"></span>**schema di derivazione della chiave di sessione**
</dt> <dd>

Specifica quando una chiave è derivata da un hash. I metodi usati dipendono dal tipo CSP.

</dd> <dt>

<span id="_security_set_gly"></span><span id="_SECURITY_SET_GLY"></span>**Impostare**
</dt> <dd>

Vedere *Secure Electronic Transaction.*

</dd> <dt>

<span id="_security_sha_gly"></span><span id="_SECURITY_SHA_GLY"></span>**Sha**
</dt> <dd>

Nome CryptoAPI per l'algoritmo Secure Hash, SHA-1. Altri algoritmi hash includono [*MD2,*](m-gly.md) [*MD4*](m-gly.md)e [*MD5.*](m-gly.md)

Vedere anche *Secure Hash Algorithm.*

</dd> <dt>

<span id="_security_shs_gly"></span><span id="_SECURITY_SHS_GLY"></span>**Shs**
</dt> <dd>

Vedere *Secure Hash Standard.*

</dd> <dt>

<span id="_security_sid_gly"></span><span id="_SECURITY_SID_GLY"></span>**Sid**
</dt> <dd>

Vedere *l'identificatore di sicurezza*.

</dd> <dt>

<span id="_security_signature_and_data_verification_functions_gly"></span><span id="_SECURITY_SIGNATURE_AND_DATA_VERIFICATION_FUNCTIONS_GLY"></span>**Firma e funzioni di verifica dei dati**
</dt> <dd>

Funzioni di messaggio semplificate usate per firmare i messaggi in uscita e verificare l'autenticità delle firme applicate nei messaggi ricevuti e nei dati correlati.

Vedere *funzioni di messaggio semplificate.*

</dd> <dt>

<span id="_security_signature_certificate_gly"></span><span id="_SECURITY_SIGNATURE_CERTIFICATE_GLY"></span>**certificato di firma**
</dt> <dd>

Certificato contenente una chiave pubblica utilizzata per verificare le firme digitali.

</dd> <dt>

<span id="_security_signature_file_gly"></span><span id="_SECURITY_SIGNATURE_FILE_GLY"></span>**file di firma**
</dt> <dd>

File che contiene la firma di un provider [*del servizio di crittografia*](c-gly.md) (CSP) specifico. Il file di firma è necessario per garantire che CryptoAPI riconosca il provider di servizi di configurazione. CryptoAPI convalida questa firma periodicamente per garantire che il CSP non sia stato manomesso.

</dd> <dt>

<span id="_security_signature_functions_gly"></span><span id="_SECURITY_SIGNATURE_FUNCTIONS_GLY"></span>**Funzioni di firma**
</dt> <dd>

Funzioni utilizzate per creare e verificare le firme digitali.

Vedere anche *funzioni di messaggio semplificate.*

</dd> <dt>

<span id="_security_signature_key_pair_gly"></span><span id="_SECURITY_SIGNATURE_KEY_PAIR_GLY"></span>**coppia di chiavi di firma**
</dt> <dd>

Coppia di chiavi pubblica/privata usata per l'autenticazione (firma digitale) dei messaggi. Le coppie di chiavi di firma vengono create chiamando **CryptGenKey.**

Vedere anche [*Scambiare una coppia di chiavi.*](e-gly.md)

</dd> <dt>

<span id="_security_signature_private_key_gly"></span><span id="_SECURITY_SIGNATURE_PRIVATE_KEY_GLY"></span>**chiave privata della firma**
</dt> <dd>

Chiave privata di una coppia di chiavi di firma.

Vedere *Coppia di chiavi di firma.*

</dd> <dt>

<span id="_security_signed_and_enveloped_data_gly"></span><span id="_SECURITY_SIGNED_AND_ENVELOPED_DATA_GLY"></span>**dati firmati e in busta**
</dt> <dd>

Tipo di contenuto di dati definito da PKCS \# 7. Questo tipo di dati è costituito da contenuto crittografato di qualsiasi tipo, chiavi di crittografia del contenuto crittografate per uno o più destinatari e hash dei messaggi doppiamente crittografati per uno o più firmatari. La doppia crittografia è costituita da una crittografia con la chiave privata del firmatario seguita da una crittografia con la chiave di crittografia del contenuto.

</dd> <dt>

<span id="_security_signed_data_gly"></span><span id="_SECURITY_SIGNED_DATA_GLY"></span>**dati firmati**
</dt> <dd>

Tipo di contenuto di dati definito da PKCS \# 7. Questo tipo di dati è costituito da qualsiasi tipo di contenuto più hash dei messaggi crittografati (digest) del contenuto per zero o più firmatari. Gli hash risultanti possono essere usati per confermare chi ha firmato il messaggio. Questi hash confermano anche che il messaggio originale non è stato modificato dopo la firma del messaggio.

</dd> <dt>

<span id="_security_simple_certificate_enrollment_protocol_gly"></span><span id="_SECURITY_SIMPLE_CERTIFICATE_ENROLLMENT_PROTOCOL_GLY"></span>**Simple Certificate Enrollment Protocol**
</dt> <dd>

(SCEP) Acronimo di Simple Certificate Enrollment Protocol. Il protocollo è attualmente una bozza di standard Internet che definisce la comunicazione tra i dispositivi di rete e un'autorità di registrazione (RA) per la registrazione del certificato. Per altre informazioni, vedere Microsoft SCEP Implementation White paper (White [paper sull'implementazione di Microsoft SCEP).](https://www.scribd.com/document/31941679/Microsoft-SCEP-Implementation-Whitepaper)

</dd> <dt>

<span id="_security_simple_key_blob_gly"></span><span id="_SECURITY_SIMPLE_KEY_BLOB_GLY"></span>**BLOB della chiave semplice**
</dt> <dd>

Chiave di sessione crittografata con la chiave pubblica di scambio delle chiavi dell'utente di destinazione. Questo tipo di BLOB di chiave viene usato quando si archivia una chiave di sessione o si trasmette una chiave di sessione a un altro utente. Un BLOB di chiavi viene creato chiamando **CryptExportKey**.

</dd> <dt>

<span id="_security_simplified_message_functions_gly"></span><span id="_SECURITY_SIMPLIFIED_MESSAGE_FUNCTIONS_GLY"></span>**funzioni di messaggi semplificate**
</dt> <dd>

Funzioni di gestione dei messaggi, ad esempio la crittografia dei messaggi, la decrittografia, la firma e le funzioni di verifica della firma. Le funzioni di messaggio semplificate operano a un livello superiore rispetto alle funzioni di crittografia di base o alle funzioni di messaggi di basso livello. Le funzioni di messaggio semplificate eseguono il wrapping di diverse funzioni di crittografia, di basso livello e di certificato di base in un'unica funzione che esegue un'attività specifica in modo specifico, ad esempio la crittografia di un messaggio PKCS 7 o la firma di un \# messaggio.

Vedere anche [*funzioni di messaggi di basso livello.*](l-gly.md)

</dd> <dt>

<span id="_security_single_sign_on_gly"></span><span id="_SECURITY_SINGLE_SIGN_ON_GLY"></span>**Single Sign-On**
</dt> <dd>

(SSO) Possibilità di collegare un account Microsoft (ad esempio un account Microsoft Outlook.com) a un account locale in modo che un accesso consenta all'utente di usare altre applicazioni che supportano l'accesso con il proprio account Microsoft.

</dd> <dt>

<span id="_security_sip_gly"></span><span id="_SECURITY_SIP_GLY"></span>**Sip**
</dt> <dd>

Vedere *il pacchetto dell'interfaccia dell'oggetto*.

</dd> <dt>

<span id="_security_site_certificate_gly"></span><span id="_SECURITY_SITE_CERTIFICATE_GLY"></span>**certificato del sito**
</dt> <dd>

Sia i certificati server che [*i certificati dell'autorità*](c-gly.md) di certificazione (CA) sono talvolta denominati certificati del sito. Quando si fa riferimento a un certificato del server, il certificato identifica il server Web che presenta il certificato. Quando si fa riferimento a un certificato della CA, il certificato identifica la CA che emissione certificati di autenticazione server e/o client per i server e i client che richiedono tali certificati.

</dd> <dt>

<span id="_security_skipjack_gly"></span><span id="_SECURITY_SKIPJACK_GLY"></span>**Palamite**
</dt> <dd>

Algoritmo di crittografia specificato come parte della suite di crittografia Forgle. Skipjack è una crittografia simmetrica con una lunghezza di chiave fissa di 80 bit. Skipjack è un algoritmo classificato creato dalla Stati Uniti National Security Agency (NSA). I dettagli tecnici dell'algoritmo Skipjack sono segreti.

</dd> <dt>

<span id="_security_smart_card_gly"></span><span id="_SECURITY_SMART_CARD_GLY"></span>**smart card**
</dt> <dd>

Una scheda di circuito integrato (ICC) di proprietà di un singolo utente o di un gruppo le cui informazioni devono essere protette in base ad assegnazioni di proprietà specifiche. Fornisce il proprio controllo di accesso fisico. senza il sottosistema smart card che inserisce un controllo di accesso aggiuntivo sul smart card. Un smart card è una scheda di card card contenente un circuito integrato compatibile con ISO 7816.

</dd> <dt>

<span id="_security_smart_card_common_dialog_gly"></span><span id="_SECURITY_SMART_CARD_COMMON_DIALOG_GLY"></span>**smart card di dialogo comune**
</dt> <dd>

Finestra di dialogo comune che assiste l'utente nella selezione e nell'individuazione di un smart card. Funziona con i servizi di gestione di database smart card e con i servizi lettore per consentire all'applicazione e, se necessario, all'utente di identificare il smart card da usare per uno scopo specifico.

</dd> <dt>

<span id="_security_smart_card_database_gly"></span><span id="_SECURITY_SMART_CARD_DATABASE_GLY"></span>**smart card database**
</dt> <dd>

Database usato da Resource Manager per gestire le risorse. Contiene un elenco di smart card note, le interfacce e il provider di servizi primario di ogni scheda e i gruppi di lettori e lettori smart card noti.

</dd> <dt>

<span id="_security_smart_card_subsystem_gly"></span><span id="_SECURITY_SMART_CARD_SUBSYSTEM_GLY"></span>**smart card sottosistema**
</dt> <dd>

Sottosistema utilizzato per fornire un collegamento tra smart card lettori e smart card applicazioni in grado di riconoscere le applicazioni.

</dd> <dt>

<span id="_security_software_publisher_certificate_gly"></span><span id="_SECURITY_SOFTWARE_PUBLISHER_CERTIFICATE_GLY"></span>**Certificato Publisher software**
</dt> <dd>

(SPC) Oggetto dati firmato PKCS \# 7 che contiene certificati X.509.

</dd> <dt>

<span id="_security_spc_gly"></span><span id="_SECURITY_SPC_GLY"></span>**Spc**
</dt> <dd>

Vedere *Certificato Publisher software.*

</dd> <dt>

<span id="_security_spn_gly"></span><span id="_SECURITY_SPN_GLY"></span>**Spn**
</dt> <dd>

Vedere *il nome dell'entità servizio*.

</dd> <dt>

<span id="_security_ssl_gly"></span><span id="_SECURITY_SSL_GLY"></span>**Ssl**
</dt> <dd>

Vedere *Secure Sockets Layer protocollo*.

</dd> <dt>

<span id="_security_ssl3_client_authentication_algorithm_gly"></span><span id="_SECURITY_SSL3_CLIENT_AUTHENTICATION_ALGORITHM_GLY"></span>**Algoritmo di autenticazione client SSL3**
</dt> <dd>

Algoritmo usato per l'autenticazione client Secure Sockets Layer (SSL) versione 3. Nel protocollo SSL3, una concatenazione di un hash MD5 e un hash SHA-1 viene firmata con una chiave privata RSA. CryptoAPI e Microsoft Base e i provider del servizio di crittografia avanzata supportano SSL3 con il tipo hash CALG \_ SSL3 \_ SHAMD5.

</dd> <dt>

<span id="_security_ssl3_protocol_gly"></span><span id="_SECURITY_SSL3_PROTOCOL_GLY"></span>**Protocollo SSL3**
</dt> <dd>

Versione 3 del protocollo Secure Sockets Layer (SSL).

</dd> <dt>

<span id="_security_sso_gly"></span><span id="_SECURITY_SSO_GLY"></span>**Sso**
</dt> <dd>

Vedere *Single Sign-On.*

</dd> <dt>

<span id="_security_ssp_gly"></span><span id="_SECURITY_SSP_GLY"></span>**Ssp**
</dt> <dd>

Vedere *Security Support Provider*.

</dd> <dt>

<span id="_security_sspi_gly"></span><span id="_SECURITY_SSPI_GLY"></span>**Sspi**
</dt> <dd>

Vedere *Security Support Provider Interface*.

</dd> <dt>

<span id="_security_sst_gly"></span><span id="_SECURITY_SST_GLY"></span>**Sst**
</dt> <dd>

Vedere *Formato dell'archivio certificati serializzato.*

</dd> <dt>

<span id="_security_state_gly"></span><span id="_SECURITY_STATE_GLY"></span>**Stato**
</dt> <dd>

Set di tutti i valori persistenti associati a un'entità di crittografia, ad esempio una chiave o un hash. Questo set può includere elementi come il [*vettore*](i-gly.md) di inizializzazione (IV) in uso, l'algoritmo usato o il valore dell'entità già calcolato.

</dd> <dt>

<span id="_security_stream_cipher_gly"></span><span id="_SECURITY_STREAM_CIPHER_GLY"></span>**crittografia del flusso**
</dt> <dd>

Crittografia che crittografa in modo seriale i dati, un bit alla volta.

Vedere anche [*crittografia a blocchi.*](b-gly.md)

</dd> <dt>

<span id="_security_subauthentication_package_gly"></span><span id="_SECURITY_SUBAUTHENTICATION_PACKAGE_GLY"></span>**pacchetto di autenticazione secondaria**
</dt> <dd>

DLL facoltativa che fornisce funzionalità di autenticazione aggiuntive, in genere estendendo l'algoritmo di autenticazione. Se è installato un pacchetto di autenticazione secondaria, il pacchetto di autenticazione chiamerà il pacchetto di autenticazione secondaria prima di restituire il risultato dell'autenticazione all'autorità di sicurezza locale (LSA).

Vedere anche [*Autorità di sicurezza locale.*](l-gly.md)

</dd> <dt>

<span id="_security_subject_interface_package_gly"></span><span id="_SECURITY_SUBJECT_INTERFACE_PACKAGE_GLY"></span>**pacchetto dell'interfaccia soggetto**
</dt> <dd>

(SIP) Specifica proprietaria Microsoft per un livello software che consente alle applicazioni di creare, archiviare, recuperare e verificare una firma del soggetto. Gli argomenti includono, a parte, immagini eseguibili portabili (.exe), immagini cab (.cab), file flat e file di catalogo. Ogni tipo di soggetto usa un subset diverso dei dati per il calcolo hash e richiede una procedura diversa per l'archiviazione e il recupero. Ogni tipo di soggetto ha pertanto una specifica univoca del pacchetto dell'interfaccia soggetto.

</dd> <dt>

<span id="_security_suite_b_gly"></span><span id="_SECURITY_SUITE_B_GLY"></span>**Suite B**
</dt> <dd>

Set di algoritmi di crittografia dichiarati apertamente dalla National Security Agency degli Stati Uniti come parte del programma di modernizzazione crittografica.

</dd> <dt>

<span id="_security_supplemental_credentials_gly"></span><span id="_SECURITY_SUPPLEMENTAL_CREDENTIALS_GLY"></span>**credenziali supplementari**
</dt> <dd>

Credenziali da usare per l'autenticazione di *un'entità di sicurezza* in domini di sicurezza esterni.

Vedere anche [*credenziali primarie.*](p-gly.md)

</dd> <dt>

<span id="_security_symmetric_algorithm_gly"></span><span id="_SECURITY_SYMMETRIC_ALGORITHM_GLY"></span>**algoritmo simmetrico**
</dt> <dd>

Algoritmo di crittografia che in genere usa una singola chiave, spesso definita chiave di sessione, per la crittografia e la decrittografia. Gli algoritmi simmetrici possono essere suddivisi in due categorie,  algoritmi di flusso e algoritmi a blocchi (detti anche crittografie [*di flusso e a blocchi).*](b-gly.md)

</dd> <dt>

<span id="_security_symmetric_encryption_gly"></span><span id="_SECURITY_SYMMETRIC_ENCRYPTION_GLY"></span>**crittografia simmetrica**
</dt> <dd>

Crittografia che utilizza un'unica chiave sia per la crittografia sia per la decrittografia. La crittografia simmetrica è preferibile quando si esegue la crittografia di notevoli quantità di dati. Alcuni degli algoritmi di crittografia simmetrica più comuni [*sono RC2*](r-gly.md), [*RC4*](r-gly.md)e [*Data Encryption Standard*](d-gly.md) (DES).

Vedere anche [*crittografia a chiave pubblica.*](p-gly.md)

</dd> <dt>

<span id="_security_symmetric_key_gly"></span><span id="_SECURITY_SYMMETRIC_KEY_GLY"></span>**chiave simmetrica**
</dt> <dd>

Chiave privata usata con un algoritmo di crittografia simmetrico, ovvero un algoritmo che usa la stessa chiave sia per la crittografia che per la decrittografia. Tale chiave deve essere nota a tutte le parti che comunicano.

</dd> <dt>

<span id="_security_system_access_control_list_gly"></span><span id="_SECURITY_SYSTEM_ACCESS_CONTROL_LIST_GLY"></span>**elenco di controllo di accesso di sistema**
</dt> <dd>

(SACL) ACL che controlla la generazione di messaggi di controllo per i tentativi di accesso a un oggetto a protezione diretta. La possibilità di ottenere o impostare l'elenco SACL di un oggetto è controllata da un privilegio generalmente mantenuto solo dagli amministratori di sistema.

Vedere anche elenco [*di controllo di accesso*](a-gly.md), elenco di controllo di accesso [*discrezionale*](d-gly.md), [*privilegio*](p-gly.md).

</dd> <dt>

<span id="_security_system_program_interface_gly"></span><span id="_SECURITY_SYSTEM_PROGRAM_INTERFACE_GLY"></span>**interfaccia del programma di sistema**
</dt> <dd>

Set di funzioni fornito da un [*provider del servizio di*](c-gly.md) crittografia (CSP) che implementa le funzioni di un'applicazione.

</dd> </dl>

 

 



