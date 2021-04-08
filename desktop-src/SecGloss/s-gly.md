---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera S.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e9d7672-2314-45c8-8178-5a0afcfd0c50
title: S (Glossario sulla sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975df9e3638f12ba7f3766d6119685fba1fa599b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967877"
---
# <a name="s-security-glossary"></a>S (Glossario sulla sicurezza)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) S [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_s_mime_gly"></span><span id="_SECURITY_S_MIME_GLY"></span>**S/MIME**
</dt> <dd>

Vedere *Secure/Multipurpose Internet Mail Extensions*.

</dd> <dt>

<span id="_security_sacl_gly"></span><span id="_SECURITY_SACL_GLY"></span>**SACL**
</dt> <dd>

Vedere *l'elenco di controllo di accesso di sistema*.

</dd> <dt>

<span id="_security_salt_value_gly"></span><span id="_SECURITY_SALT_VALUE_GLY"></span>**valore Salt**
</dt> <dd>

Dati casuali a volte inclusi come parte di una chiave di sessione. Quando viene aggiunto a una chiave di sessione, i dati Salt non crittografati vengono posizionati davanti ai dati della chiave crittografata. Vengono aggiunti valori Salt per aumentare il lavoro necessario per montare un attacco di forza bruta (Dictionary) contro i dati crittografati con una crittografia a chiave simmetrica. I valori Salt vengono generati chiamando **CryptGenRandom**.

</dd> <dt>

<span id="_security_sam_gly"></span><span id="_SECURITY_SAM_GLY"></span>**SAM**
</dt> <dd>

Vedere *gestione degli account di sicurezza*.

</dd> <dt>

<span id="_security_sanitized_name_gly"></span><span id="_SECURITY_SANITIZED_NAME_GLY"></span>**nome purificato**
</dt> <dd>

Il formato di un nome dell'autorità di certificazione (CA) usato nei nomi di file, ad esempio per un [*elenco di revoche di certificati*](c-gly.md), e nelle chiavi del registro di sistema. Il processo di purificazione del nome della CA è necessario per rimuovere i caratteri non validi per i nomi file, i nomi delle chiavi del registro di sistema o i valori dei nomi distinti oppure che non sono validi per motivi specifici della tecnologia. In Servizi certificati, il processo di purificazione converte qualsiasi carattere non valido nel nome comune della CA in una rappresentazione di 5 caratteri nel formato **.** _xxxx_, dove **!** viene usato come carattere di escape e *xxxx* rappresenta quattro numeri interi esadecimali che identificano in modo univoco il carattere da convertire.

</dd> <dt>

<span id="security.s_1_gly"></span><span id="SECURITY.S_1_GLY"></span>**FIRMA**
</dt> <dd>

Vedere la *sequenza di attenzione sicura*.

</dd> <dt>

<span id="_security_scard_defaultreaders_gly"></span><span id="_SECURITY_SCARD_DEFAULTREADERS_GLY"></span>**$ DefaultReaders spaventato**
</dt> <dd>

Un gruppo di lettori terminal che contiene tutti i lettori assegnati a tale terminale, tuttavia, non è riservato per questo utilizzo specifico.

</dd> <dt>

<span id="_security_scard_allreaders_gly"></span><span id="_SECURITY_SCARD_ALLREADERS_GLY"></span>**$ AllReaders spaventato**
</dt> <dd>

Un gruppo di lettori smart card a livello di sistema che include tutti i lettori introdotti per la Smart Card Resource Manager. I Reader vengono aggiunti automaticamente al gruppo quando vengono introdotti al sistema.

</dd> <dt>

<span id="_security_scard_autoallocate_gly"></span><span id="_SECURITY_SCARD_AUTOALLOCATE_GLY"></span>**\_allocato automaticamente**
</dt> <dd>

Costante di sistema della smart card che indica al gestore di risorse della smart card di allocare memoria sufficiente, restituendo un puntatore al buffer allocato anziché compilare un buffer fornito dall'utente. Il buffer restituito deve infine essere liberato chiamando **SCardFreeMemory**.

</dd> <dt>

<span id="_security_scep_gly"></span><span id="_SECURITY_SCEP_GLY"></span>**SCEP**
</dt> <dd>

Vedere *Simple Certificate Enrollment Protocol*

</dd> <dt>

<span id="_security_schannel_gly"></span><span id="_SECURITY_SCHANNEL_GLY"></span>**Schannel**
</dt> <dd>

Un pacchetto di sicurezza che fornisce l'autenticazione tra client e server.

</dd> <dt>

<span id="_security_secure_attention_sequence_gly"></span><span id="_SECURITY_SECURE_ATTENTION_SEQUENCE_GLY"></span>**sequenza di attenzione sicura**
</dt> <dd>

FIRMA Sequenza di chiavi che avvia il processo di accesso o di disconnessione. La sequenza predefinita è CTRL + ALT + CANC.

</dd> <dt>

<span id="_security_secure_electronic_transaction_gly"></span><span id="_SECURITY_SECURE_ELECTRONIC_TRANSACTION_GLY"></span>**Transazione elettronica sicura**
</dt> <dd>

SET Protocollo per le transazioni elettroniche sicure su Internet.

</dd> <dt>

<span id="_security_secure_hash_algorithm_gly"></span><span id="_SECURITY_SECURE_HASH_ALGORITHM_GLY"></span>**Algoritmo hash sicuro**
</dt> <dd>

Sha Algoritmo di hash che genera un digest del messaggio. SHA è utilizzato insieme a molte tecnologie, fra cui l'algoritmo Digital Signature Algorithm (DSA) dello standard Digital Signature Standard (DSS). CryptoAPI fa riferimento a questo algoritmo mediante l'identificatore (CALG \_ SHA), il nome (SHA) e la classe ( \_ hash della classe ALG) dell'algoritmo \_ . Esistono quattro versioni di SHA: SHA-1, SHA-256, SHA-384 e SHA-512. SHA-1 genera un digest del messaggio a 160 bit. SHA-256, SHA-384 e SHA-512 generano rispettivamente un digest del messaggio a 256, 384 e 512 bit. SHA è stato sviluppato dall'istituto National Institute of Standards and Technology (NIST) e dall'agenzia National Security Agency (NSA).

</dd> <dt>

<span id="_security_secure_hash_standard_gly"></span><span id="_SECURITY_SECURE_HASH_STANDARD_GLY"></span>**Secure hash standard**
</dt> <dd>

Standard progettato da NIST e NSA. Questo standard definisce l'algoritmo Secure Hash Algorithm (SHA-1) da usare con Digital Signature Standard (DSS).

Vedere anche *Secure Hash Algorithm*.

</dd> <dt>

<span id="_security_secure_sockets_layer_protocol_gly"></span><span id="_SECURITY_SECURE_SOCKETS_LAYER_PROTOCOL_GLY"></span>**Protocollo Secure Sockets Layer**
</dt> <dd>

SSL Protocollo per proteggere le comunicazioni di rete mediante una combinazione di tecnologia chiave pubblica e privata.

</dd> <dt>

<span id="_security_secure_multipurpose_internet_mail_extensions_gly"></span><span id="_SECURITY_SECURE_MULTIPURPOSE_INTERNET_MAIL_EXTENSIONS_GLY"></span>**Sicurezza/Multipurpose Internet Mail Extensions**
</dt> <dd>

(S/MIME) Standard di sicurezza della posta elettronica che usa la crittografia a chiave pubblica.

</dd> <dt>

<span id="_security_security_accounts_manager_gly"></span><span id="_SECURITY_SECURITY_ACCOUNTS_MANAGER_GLY"></span>**Gestione account di protezione**
</dt> <dd>

Sam Servizio Windows utilizzato durante il processo di accesso. SAM gestisce le informazioni sull'account utente, inclusi i gruppi a cui appartiene un utente.

</dd> <dt>

<span id="_security_security_context_gly"></span><span id="_SECURITY_SECURITY_CONTEXT_GLY"></span>**contesto di sicurezza**
</dt> <dd>

Attributi o regole di sicurezza correntemente applicati. Esempi di contesti di sicurezza sono l'utente connesso correntemente al computer o il codice PIN immesso da un utente di smart card. Per l'interfaccia SSPI, un contesto di sicurezza è una struttura non trasparente di dati che contiene dati di sicurezza relativi a una connessione, ad esempio una chiave di sessione o un'indicazione della durata della sessione.

</dd> <dt>

<span id="_security_security_descriptor_gly"></span><span id="_SECURITY_SECURITY_DESCRIPTOR_GLY"></span>**descrittore di sicurezza**
</dt> <dd>

Struttura e dati associati che contengono le informazioni di sicurezza per un oggetto a protezione diretta. Un descrittore di sicurezza identifica il proprietario e il gruppo primario dell'oggetto. Può inoltre contenere un DACL che controlla l'accesso all'oggetto e un SACL che controlla la registrazione dei tentativi di accesso all'oggetto.

Vedere anche [*descrittore di sicurezza assoluto*](a-gly.md), [*elenco di controllo di accesso discrezionale*](d-gly.md), *descrittore di sicurezza autonomi*, *elenco di controllo di accesso di sistema*.

</dd> <dt>

<span id="_security_security_identifier_gly"></span><span id="_SECURITY_SECURITY_IDENTIFIER_GLY"></span>**ID di sicurezza**
</dt> <dd>

SID Struttura di dati di lunghezza variabile che identifica gli account utente, gruppo e computer. Quando l'account viene creato per la prima volta, viene emesso un SID univoco per ogni account di una rete. I processi interni di Windows fanno riferimento al SID di un account anziché al nome dell'utente o del gruppo dell'account.

</dd> <dt>

<span id="_security_security_package_gly"></span><span id="_SECURITY_SECURITY_PACKAGE_GLY"></span>**pacchetto di sicurezza**
</dt> <dd>

Implementazione del software di un protocollo di sicurezza. I pacchetti di sicurezza sono contenuti in dll Security Support Provider o dll del pacchetto di Security Support Provider/autenticazione.

</dd> <dt>

<span id="_security_security_protocol_gly"></span><span id="_SECURITY_SECURITY_PROTOCOL_GLY"></span>**protocollo di sicurezza**
</dt> <dd>

Specifica che definisce gli oggetti dati correlati alla sicurezza e le regole relative alla modalità di utilizzo degli oggetti per mantenere la sicurezza in un sistema di computer.

</dd> <dt>

<span id="_security_security_principal_gly"></span><span id="_SECURITY_SECURITY_PRINCIPAL_GLY"></span>**entità di sicurezza**
</dt> <dd>

Entità riconosciuta dal sistema di sicurezza. Le entità di sicurezza possono essere utenti o processi autonomi.

</dd> <dt>

<span id="_security_security_support_provider_gly"></span><span id="_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY"></span>**Security Support Provider**
</dt> <dd>

SSP Una libreria di collegamento dinamico (DLL) che implementa l'interfaccia SSPI rendendo disponibili per le applicazioni uno o più pacchetti di sicurezza. Ogni pacchetto di sicurezza fornisce associazioni tra le chiamate di funzione dell'interfaccia SSPI di un'applicazione e le funzioni di un modello di sicurezza effettivo. I pacchetti di sicurezza supportano i protocolli di sicurezza, ad esempio l'autenticazione Kerberos e Microsoft LAN Manager.

</dd> <dt>

<span id="_security_security_support_provider_interface_gly"></span><span id="_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY"></span>**Interfaccia Security Support Provider**
</dt> <dd>

SSPI Interfaccia comune tra le applicazioni a livello di trasporto, ad esempio Microsoft Remote Procedure Call (RPC) e i provider di sicurezza, ad esempio la sicurezza distribuita di Windows. L'interfaccia SSPI consente a un'applicazione a livello di trasporto di chiamare uno dei diversi provider di sicurezza per ottenere una connessione autenticata. Queste chiamate non richiedono una conoscenza approfondita dei dettagli del protocollo di sicurezza.

</dd> <dt>

<span id="_security_self_relative_security_descriptor_gly"></span><span id="_SECURITY_SELF_RELATIVE_SECURITY_DESCRIPTOR_GLY"></span>**descrittore di sicurezza relativo**
</dt> <dd>

Descrittore di sicurezza che archivia tutte le informazioni di sicurezza in un blocco di memoria contiguo.

Vedere anche *descrittore di sicurezza*.

</dd> <dt>

<span id="_security_serialize_gly"></span><span id="_SECURITY_SERIALIZE_GLY"></span>**serializzare**
</dt> <dd>

Processo di conversione dei dati in una stringa di uno e zero in modo che possa essere trasmesso in modo seriale. La codifica è parte di questo processo.

</dd> <dt>

<span id="_security_serialized_certificate_store_format_gly"></span><span id="_SECURITY_SERIALIZED_CERTIFICATE_STORE_FORMAT_GLY"></span>**Formato dell'archivio certificati serializzato**
</dt> <dd>

SST Il formato dell'archivio certificati serializzato è l'unico formato che conserva tutte le proprietà dell'archivio certificati. È utile nei casi in cui le radici sono state configurate con proprietà EKU personalizzate e si desidera spostarle in un altro computer.

</dd> <dt>

<span id="_security_server_gly"></span><span id="_SECURITY_SERVER_GLY"></span>**Server**
</dt> <dd>

Computer che risponde ai comandi da un computer client. Il client e il server collaborano per eseguire la funzionalità di applicazione distributiva.

Vedere anche [*client*](c-gly.md).

</dd> <dt>

<span id="_security_server_certificate_gly"></span><span id="_SECURITY_SERVER_CERTIFICATE_GLY"></span>**certificato server**
</dt> <dd>

Fa riferimento a un certificato utilizzato per l'autenticazione server, ad esempio l'autenticazione di un server Web in un Web browser. Quando un client del browser Web tenta di accedere a un server Web protetto, il server invia il certificato al browser per consentire la verifica dell'identità del server.

</dd> <dt>

<span id="_security_server_gated_cryptography_gly"></span><span id="_SECURITY_SERVER_GATED_CRYPTOGRAPHY_GLY"></span>**crittografia gestita dal server**
</dt> <dd>

SGC Estensione di *Secure Sockets Layer* (SSL) che consente alle organizzazioni, ad esempio istituti finanziari, che hanno versioni di esportazione di Internet Information Services (IIS) di usare la crittografia avanzata, ad esempio la crittografia a 128 bit.

</dd> <dt>

<span id="_security_service_principal_name_gly"></span><span id="_SECURITY_SERVICE_PRINCIPAL_NAME_GLY"></span>**nome dell'entità servizio**
</dt> <dd>

SPN Nome con cui un client identifica in modo univoco un'istanza di un servizio. Se si installano più istanze di un servizio in computer distribuiti in una foresta, a ogni istanza deve essere associato un nome SPN distinto. Un'istanza del servizio specificata può avere più SPN se sono presenti più nomi che i client possono usare per l'autenticazione

</dd> <dt>

<span id="_security_service_provider_smart_card__gly"></span><span id="_SECURITY_SERVICE_PROVIDER_SMART_CARD__GLY"></span>**provider di servizi (smart card)**
</dt> <dd>

Componente del sottosistema di smart card che fornisce l'accesso a servizi Smart Card specifici tramite interfacce COM.

Vedere anche [*provider di servizi primario*](p-gly.md).

</dd> <dt>

<span id="_security_session_gly"></span><span id="_SECURITY_SESSION_GLY"></span>**sessione**
</dt> <dd>

Scambio di messaggi protetto mediante un solo elemento di materiale per le chiavi. Ad esempio, le sessioni SSL utilizzano un'unica chiave per proteggere lo scambio di più messaggi.

</dd> <dt>

<span id="_security_session_key_gly"></span><span id="_SECURITY_SESSION_KEY_GLY"></span>**chiave di sessione**
</dt> <dd>

Chiave crittografica relativamente breve, spesso negoziata da un client e da un server basato su un segreto condiviso. La durata della chiave di sessione è vincolata dalla sessione a cui è associata. Una chiave di sessione deve essere sufficientemente forte da sostenere la crittanalisi per la durata della sessione. Quando vengono trasmesse, le chiavi di sessione vengono in genere protette con chiavi di scambio delle chiavi, che in genere sono chiavi asimmetriche, in modo che solo il destinatario previsto possa accedervi. Le chiavi di sessione possono essere derivate da valori hash chiamando la funzione **CryptDeriveKey** .

</dd> <dt>

<span id="_security_session_key_derivation_scheme_gly"></span><span id="_SECURITY_SESSION_KEY_DERIVATION_SCHEME_GLY"></span>**schema di derivazione della chiave di sessione**
</dt> <dd>

Specifica quando una chiave viene derivata da un hash. I metodi utilizzati dipendono dal tipo CSP.

</dd> <dt>

<span id="_security_set_gly"></span><span id="_SECURITY_SET_GLY"></span>**SET**
</dt> <dd>

Vedere *Secure Electronic Transaction*.

</dd> <dt>

<span id="_security_sha_gly"></span><span id="_SECURITY_SHA_GLY"></span>**SHA**
</dt> <dd>

Nome della CryptoAPI per l'algoritmo hash sicuro, SHA-1. Altri algoritmi di hashing includono [*MD2*](m-gly.md), [*MD4*](m-gly.md)e [*MD5*](m-gly.md).

Vedere anche *Secure Hash Algorithm*.

</dd> <dt>

<span id="_security_shs_gly"></span><span id="_SECURITY_SHS_GLY"></span>**SHS**
</dt> <dd>

Vedere *Secure hash standard*.

</dd> <dt>

<span id="_security_sid_gly"></span><span id="_SECURITY_SID_GLY"></span>**SID**
</dt> <dd>

Vedere *identificatore di sicurezza*.

</dd> <dt>

<span id="_security_signature_and_data_verification_functions_gly"></span><span id="_SECURITY_SIGNATURE_AND_DATA_VERIFICATION_FUNCTIONS_GLY"></span>**funzioni per la firma e la verifica dei dati**
</dt> <dd>

Funzioni di messaggio semplificate utilizzate per firmare i messaggi in uscita e verificare l'autenticità delle firme applicate nei messaggi ricevuti e nei dati correlati.

Vedere *funzioni di messaggio semplificate*.

</dd> <dt>

<span id="_security_signature_certificate_gly"></span><span id="_SECURITY_SIGNATURE_CERTIFICATE_GLY"></span>**certificato di firma**
</dt> <dd>

Certificato che contiene una chiave pubblica usata per verificare le firme digitali.

</dd> <dt>

<span id="_security_signature_file_gly"></span><span id="_SECURITY_SIGNATURE_FILE_GLY"></span>**file di firma**
</dt> <dd>

File contenente la firma di un [*provider del servizio di crittografia*](c-gly.md) (CSP) specifico. Il file della firma è necessario per garantire che CryptoAPI riconosca il CSP. Questa firma viene convalidata periodicamente da CryptoAPI per verificare che il CSP non sia stato alterato.

</dd> <dt>

<span id="_security_signature_functions_gly"></span><span id="_SECURITY_SIGNATURE_FUNCTIONS_GLY"></span>**funzioni di firma**
</dt> <dd>

Funzioni usate per creare e verificare le firme digitali.

Vedere anche *funzioni di messaggio semplificate*.

</dd> <dt>

<span id="_security_signature_key_pair_gly"></span><span id="_SECURITY_SIGNATURE_KEY_PAIR_GLY"></span>**coppia di chiavi di firma**
</dt> <dd>

Coppia di chiavi pubblica/privata utilizzata per autenticare i messaggi (firma digitale). Le coppie di chiavi di firma vengono create chiamando **CryptGenKey**.

Vedere anche [*coppia di chiavi di scambio*](e-gly.md).

</dd> <dt>

<span id="_security_signature_private_key_gly"></span><span id="_SECURITY_SIGNATURE_PRIVATE_KEY_GLY"></span>**chiave privata della firma**
</dt> <dd>

Chiave privata di una coppia di chiavi di firma.

Vedere *coppia di chiavi di firma*.

</dd> <dt>

<span id="_security_signed_and_enveloped_data_gly"></span><span id="_SECURITY_SIGNED_AND_ENVELOPED_DATA_GLY"></span>**dati firmati e bustati**
</dt> <dd>

Tipo di contenuto dei dati definito da PKCS \# 7. Questo tipo di dati è costituito da contenuto crittografato di qualsiasi tipo, chiavi di crittografia del contenuto crittografate per uno o più destinatari e hash di messaggi con crittografia doppia per uno o più firmatari. La crittografia doppia è costituita da una crittografia con la chiave privata di un firmatario seguita da una crittografia con la chiave di crittografia del contenuto.

</dd> <dt>

<span id="_security_signed_data_gly"></span><span id="_SECURITY_SIGNED_DATA_GLY"></span>**dati firmati**
</dt> <dd>

Tipo di contenuto dei dati definito da PKCS \# 7. Questo tipo di dati è costituito da qualsiasi tipo di contenuto più hash di messaggi crittografati (digest) del contenuto per zero o più firmatari. Gli hash risultanti possono essere utilizzati per confermare chi ha firmato il messaggio. Questi hash confermano inoltre che il messaggio originale non è stato modificato dopo la firma del messaggio.

</dd> <dt>

<span id="_security_simple_certificate_enrollment_protocol_gly"></span><span id="_SECURITY_SIMPLE_CERTIFICATE_ENROLLMENT_PROTOCOL_GLY"></span>**Simple Certificate Enrollment Protocol**
</dt> <dd>

SCEP Acronimo che sta per Simple Certificate Enrollment Protocol. Il protocollo è attualmente uno standard Internet bozza che definisce la comunicazione tra i dispositivi di rete e un'autorità di registrazione (RA) per la registrazione del certificato. Per ulteriori informazioni, vedere il [white paper sull'implementazione di Microsoft SCEP](https://www.scribd.com/document/31941679/Microsoft-SCEP-Implementation-Whitepaper).

</dd> <dt>

<span id="_security_simple_key_blob_gly"></span><span id="_SECURITY_SIMPLE_KEY_BLOB_GLY"></span>**BLOB di chiavi semplice**
</dt> <dd>

Chiave di sessione crittografata con la chiave pubblica di scambio chiave dell'utente di destinazione. Questo tipo di BLOB di chiavi viene usato durante l'archiviazione di una chiave di sessione o la trasmissione di una chiave di sessione a un altro utente. Un BLOB di chiavi viene creato chiamando **CryptExportKey**.

</dd> <dt>

<span id="_security_simplified_message_functions_gly"></span><span id="_SECURITY_SIMPLIFIED_MESSAGE_FUNCTIONS_GLY"></span>**funzioni di messaggio semplificate**
</dt> <dd>

Funzioni di gestione dei messaggi, ad esempio le funzioni di crittografia, decrittografia, firma e verifica della firma del messaggio. Funzioni di messaggio semplificate operano a un livello superiore rispetto alle funzioni di crittografia di base o alle funzioni di messaggio di basso livello. Le funzioni di messaggio semplificate eseguono il wrapping di diverse funzioni di crittografia, messaggio di basso livello e di certificato di base in una singola funzione che esegue un'attività specifica in modo specifico, ad esempio la crittografia di un \# messaggio PKCS 7 o la firma di un messaggio.

Vedere anche [*funzioni di messaggio di basso livello*](l-gly.md).

</dd> <dt>

<span id="_security_single_sign_on_gly"></span><span id="_SECURITY_SINGLE_SIGN_ON_GLY"></span>**Single Sign-on**
</dt> <dd>

SSO La possibilità di collegare un account Microsoft (ad esempio un account Microsoft Outlook.com) con un account locale, in modo che un accesso consenta all'utente di usare altre applicazioni che supportano l'accesso con la loro account Microsoft.

</dd> <dt>

<span id="_security_sip_gly"></span><span id="_SECURITY_SIP_GLY"></span>**SIP**
</dt> <dd>

Vedere *pacchetto dell'interfaccia dell'oggetto*.

</dd> <dt>

<span id="_security_site_certificate_gly"></span><span id="_SECURITY_SITE_CERTIFICATE_GLY"></span>**certificato del sito**
</dt> <dd>

Sia i certificati del server che i certificati dell' [*autorità di certificazione*](c-gly.md) (CA) sono talvolta denominati certificati del sito. Quando si fa riferimento a un certificato del server, il certificato identifica il server Web che presenta il certificato. Quando si fa riferimento a un certificato della CA, il certificato identifica la CA che rilascia i certificati di autenticazione server e/o client ai server e ai client che richiedono questi certificati.

</dd> <dt>

<span id="_security_skipjack_gly"></span><span id="_SECURITY_SKIPJACK_GLY"></span>**Skipjack**
</dt> <dd>

Algoritmo di crittografia specificato come parte della famiglia di crittografia di fortezza. Skipjack è una crittografia simmetrica con una lunghezza di chiave fissa di 80 bit. Skipjack è un algoritmo Classificato creato dal Stati Uniti National Security Agency (NSA). I dettagli tecnici dell'algoritmo Skipjack sono Secret.

</dd> <dt>

<span id="_security_smart_card_gly"></span><span id="_SECURITY_SMART_CARD_GLY"></span>**Smart Card**
</dt> <dd>

Una scheda di circuito integrato di proprietà di un singolo o di un gruppo le cui informazioni devono essere protette in base alle assegnazioni di proprietà specifiche. Fornisce il proprio controllo di accesso fisico; senza il sottosistema smart card che posiziona il controllo di accesso aggiuntivo sulla smart card. Una smart card è una scheda di plastica che contiene un circuito integrato compatibile con ISO 7816.

</dd> <dt>

<span id="_security_smart_card_common_dialog_gly"></span><span id="_SECURITY_SMART_CARD_COMMON_DIALOG_GLY"></span>**finestra di dialogo comune Smart Card**
</dt> <dd>

Una finestra di dialogo comune che assiste l'utente nella selezione e nell'individuazione di una smart card. Funziona con i servizi di gestione di database e di lettura delle smart card per aiutare l'applicazione e, se necessario, l'utente per identificare la smart card da usare per uno scopo specifico.

</dd> <dt>

<span id="_security_smart_card_database_gly"></span><span id="_SECURITY_SMART_CARD_DATABASE_GLY"></span>**database smart card**
</dt> <dd>

Database utilizzato da Resource Manager per gestire le risorse. Contiene un elenco di smart card note, interfacce e provider di servizi primari di ogni scheda e lettori di smart card e gruppi di lettori noti.

</dd> <dt>

<span id="_security_smart_card_subsystem_gly"></span><span id="_SECURITY_SMART_CARD_SUBSYSTEM_GLY"></span>**sottosistema Smart Card**
</dt> <dd>

Sottosistema utilizzato per fornire un collegamento tra i lettori di smart card e le applicazioni compatibili con smart card.

</dd> <dt>

<span id="_security_software_publisher_certificate_gly"></span><span id="_SECURITY_SOFTWARE_PUBLISHER_CERTIFICATE_GLY"></span>**Certificato autore del software**
</dt> <dd>

SPC \#Oggetto dati con segno PKCS 7 contenente certificati X. 509.

</dd> <dt>

<span id="_security_spc_gly"></span><span id="_SECURITY_SPC_GLY"></span>**SPC**
</dt> <dd>

Vedere *certificato autore del software*.

</dd> <dt>

<span id="_security_spn_gly"></span><span id="_SECURITY_SPN_GLY"></span>**SPN**
</dt> <dd>

Vedere *nome dell'entità servizio*.

</dd> <dt>

<span id="_security_ssl_gly"></span><span id="_SECURITY_SSL_GLY"></span>**SSL**
</dt> <dd>

Vedere *protocollo Secure Sockets Layer*.

</dd> <dt>

<span id="_security_ssl3_client_authentication_algorithm_gly"></span><span id="_SECURITY_SSL3_CLIENT_AUTHENTICATION_ALGORITHM_GLY"></span>**Algoritmo di autenticazione client SSL3**
</dt> <dd>

Algoritmo utilizzato per l'autenticazione client in Secure Sockets Layer (SSL) versione 3. Nel protocollo SSL3, una concatenazione di un hash MD5 e di un hash SHA-1 viene firmata con una chiave privata RSA. CryptoAPI e i provider di servizi di crittografia avanzati e di base Microsoft supportano SSL3 con il tipo di hash CALG \_ SSL3 \_ SHAMD5.

</dd> <dt>

<span id="_security_ssl3_protocol_gly"></span><span id="_SECURITY_SSL3_PROTOCOL_GLY"></span>**Protocollo SSL3**
</dt> <dd>

Versione 3 del protocollo Secure Sockets Layer (SSL).

</dd> <dt>

<span id="_security_sso_gly"></span><span id="_SECURITY_SSO_GLY"></span>**SSO**
</dt> <dd>

Vedere *Single Sign-on*.

</dd> <dt>

<span id="_security_ssp_gly"></span><span id="_SECURITY_SSP_GLY"></span>**SSP**
</dt> <dd>

Vedere *Security Support Provider*.

</dd> <dt>

<span id="_security_sspi_gly"></span><span id="_SECURITY_SSPI_GLY"></span>**SSPI**
</dt> <dd>

Vedere *Security Support Provider Interface*.

</dd> <dt>

<span id="_security_sst_gly"></span><span id="_SECURITY_SST_GLY"></span>**SST**
</dt> <dd>

Vedere *formato di archivio certificati serializzato*.

</dd> <dt>

<span id="_security_state_gly"></span><span id="_SECURITY_STATE_GLY"></span>**stato**
</dt> <dd>

Set di tutti i valori salvati in modo permanente associati a un'entità di crittografia, ad esempio una chiave o un hash. Questo set può includere elementi quali il [*vettore di inizializzazione*](i-gly.md) (IV) utilizzato, l'algoritmo utilizzato oppure il valore dell'entità già calcolata.

</dd> <dt>

<span id="_security_stream_cipher_gly"></span><span id="_SECURITY_STREAM_CIPHER_GLY"></span>**crittografia di flusso**
</dt> <dd>

Crittografia che esegue la crittografia seriale dei dati, un bit alla volta.

Vedere anche [*crittografia a blocchi*](b-gly.md).

</dd> <dt>

<span id="_security_subauthentication_package_gly"></span><span id="_SECURITY_SUBAUTHENTICATION_PACKAGE_GLY"></span>**pacchetto di sottoautenticazione**
</dt> <dd>

DLL facoltativa che fornisce funzionalità di autenticazione aggiuntive, in genere estendendo l'algoritmo di autenticazione. Se viene installato un pacchetto di sottoautenticazione, il pacchetto di autenticazione chiamerà il pacchetto di sottoautenticazione prima di restituire il risultato dell'autenticazione all'autorità di sicurezza locale (LSA).

Vedere anche [*autorità di sicurezza locale*](l-gly.md).

</dd> <dt>

<span id="_security_subject_interface_package_gly"></span><span id="_SECURITY_SUBJECT_INTERFACE_PACKAGE_GLY"></span>**pacchetto dell'interfaccia soggetto**
</dt> <dd>

SIP Specifica proprietaria di Microsoft per un livello software che consente alle applicazioni di creare, archiviare, recuperare e verificare la firma di un oggetto. Gli argomenti comprendono, ma non sono limitati a, immagini eseguibili portatili (exe), immagini cabinet (CAB), file flat e file di catalogo. Ogni tipo di oggetto usa un subset di dati diverso per il calcolo hash e richiede una procedura diversa per l'archiviazione e il recupero. Pertanto, ogni tipo di oggetto ha una specifica del pacchetto dell'interfaccia del soggetto univoca.

</dd> <dt>

<span id="_security_suite_b_gly"></span><span id="_SECURITY_SUITE_B_GLY"></span>**Suite B**
</dt> <dd>

Set di algoritmi di crittografia dichiarati in modo aperto dall'agenzia di sicurezza nazionale degli Stati Uniti come parte del programma di modernizzazione di crittografia.

</dd> <dt>

<span id="_security_supplemental_credentials_gly"></span><span id="_SECURITY_SUPPLEMENTAL_CREDENTIALS_GLY"></span>**credenziali aggiuntive**
</dt> <dd>

Credenziali da utilizzare per l'autenticazione di un' *entità di sicurezza* in domini di sicurezza esterni.

Vedere anche [*credenziali primarie*](p-gly.md).

</dd> <dt>

<span id="_security_symmetric_algorithm_gly"></span><span id="_SECURITY_SYMMETRIC_ALGORITHM_GLY"></span>**algoritmo simmetrico**
</dt> <dd>

Algoritmo di crittografia che in genere usa una singola chiave, spesso definita chiave di sessione, per la crittografia e la decrittografia. Gli algoritmi simmetrici possono essere divisi in due categorie, algoritmi di flusso e algoritmi di blocco, denominati anche [*crittografia a blocchi*](b-gly.md)e di *flusso* .

</dd> <dt>

<span id="_security_symmetric_encryption_gly"></span><span id="_SECURITY_SYMMETRIC_ENCRYPTION_GLY"></span>**crittografia simmetrica**
</dt> <dd>

Crittografia che utilizza un'unica chiave sia per la crittografia sia per la decrittografia. La crittografia simmetrica è preferibile quando si esegue la crittografia di notevoli quantità di dati. Alcuni degli algoritmi di crittografia simmetrica più comuni sono [*RC2*](r-gly.md), [*RC4*](r-gly.md)e [*Data Encryption Standard*](d-gly.md) (des).

Vedere anche [*crittografia a chiave pubblica*](p-gly.md).

</dd> <dt>

<span id="_security_symmetric_key_gly"></span><span id="_SECURITY_SYMMETRIC_KEY_GLY"></span>**chiave simmetrica**
</dt> <dd>

Chiave privata utilizzata con un algoritmo di crittografia simmetrico, ovvero un algoritmo che utilizza la stessa chiave sia per la crittografia che per la decrittografia. Tale chiave deve essere nota a tutte le parti che comunicano.

</dd> <dt>

<span id="_security_system_access_control_list_gly"></span><span id="_SECURITY_SYSTEM_ACCESS_CONTROL_LIST_GLY"></span>**elenco di controllo di accesso di sistema**
</dt> <dd>

SACL Elenco ACL che controlla la generazione di messaggi di controllo per i tentativi di accesso a un oggetto a protezione diretta. La possibilità di ottenere o impostare il SACL di un oggetto viene controllata da un privilegio generalmente contenuto solo dagli amministratori di sistema.

Vedere anche [*elenco di controllo di accesso*](a-gly.md), elenco di controllo di [*accesso discrezionale*](d-gly.md), [*privilegio*](p-gly.md).

</dd> <dt>

<span id="_security_system_program_interface_gly"></span><span id="_SECURITY_SYSTEM_PROGRAM_INTERFACE_GLY"></span>**interfaccia del programma di sistema**
</dt> <dd>

Set di funzioni fornito da un [*provider del servizio di crittografia*](c-gly.md) (CSP) che implementa le funzioni di un'applicazione.

</dd> </dl>

 

 



