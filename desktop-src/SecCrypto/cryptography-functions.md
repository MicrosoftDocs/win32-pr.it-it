---
description: Elenca le funzioni fornite da CryptoAPI.
ms.assetid: 9a65f73d-6f8c-4271-a2d0-d91ad952f9c6
title: 'Funzioni di crittografia '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91338c4a1cea62e2ecc4a2fa1f7254f303ef9b2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104132206"
---
# <a name="cryptography-functions"></a>Funzioni di crittografia 

Le funzioni di crittografia sono classificate in base all'utilizzo come indicato di seguito:

-   [Funzioni CryptXML](#cryptxml-functions)
-   [Funzioni di firma](#signer-functions)
-   [Funzioni di crittografia di base](#base-cryptography-functions)
    -   [Funzioni del provider di servizi](#service-provider-functions)
    -   [Funzioni di generazione e scambio di chiavi](#key-generation-and-exchange-functions)
    -   [Funzioni di codifica e decodifica di oggetti](#object-encoding-and-decoding-functions)
    -   [Funzioni di crittografia e decrittografia dei dati](#data-encryption-and-decryption-functions)
    -   [Funzioni di firma digitale e hash](#hash-and-digital-signature-functions)
-   [Funzioni di archivio certificati e certificati](#certificate-and-certificate-store-functions)
    -   [Funzioni dell'archivio certificati](#certificate-and-certificate-store-functions)
    -   [Funzioni di manutenzione dell'archivio certificati e certificati](#certificate-and-certificate-store-maintenance-functions)
    -   [Funzioni per i certificati](#certificate-functions)
    -   [Funzioni dell'elenco di revoche di certificati](#certificate-revocation-list-functions)
    -   [Funzioni elenco certificati attendibili](#certificate-trust-list-functions)
    -   [Funzioni di proprietà estese](#extended-property-functions)
-   [Funzioni MakeCert](#makecert-functions)
-   [Funzioni di verifica certificati](#certificate-verification-functions)
    -   [Funzioni di verifica con scopi consentiti](#verification-functions-using-ctls)
    -   [Funzioni di verifica della catena di certificati](#certificate-chain-verification-functions)
-   [Funzioni di messaggio](#message-functions)
    -   [Funzioni di messaggio di basso livello](#low-level-message-functions)
    -   [Funzioni di messaggio semplificate](#simplified-message-functions)
-   [Funzioni ausiliarie](#auxiliary-functions)
    -   [Funzioni Gestione dati](#data-management-functions)
    -   [Funzioni di conversione dei dati](#data-conversion-functions)
    -   [Funzioni di utilizzo chiavi avanzate](#enhanced-key-usage-functions)
    -   [Funzioni identificatore di chiave](#key-identifier-functions)
    -   [Funzioni di supporto OID](#oid-support-functions)
    -   [Funzioni di recupero di oggetti remoti](#remote-object-retrieval-functions)
    -   [Funzioni PFX](#pfx-functions)
-   [Funzioni di backup e ripristino di Servizi certificati](#certificate-services-backup-and-restore-functions)
-   [Funzioni di callback](#callback-functions)
-   [Funzioni di definizione Catalogo](#catalog-definition-functions)
-   [Funzioni di catalogo](#catalog-functions)
-   [Funzioni WinTrust](#wintrust-functions)
-   [Funzioni del localizzatore di oggetti](#object-locator-functions)

## <a name="cryptxml-functions"></a>Funzioni CryptXML

Le funzioni XML di crittografia forniscono un'API per la creazione e la rappresentazione di firme digitali mediante dati in formato XML. Per informazioni sulle firme in formato XML, vedere la XML-Signature la sintassi e la specifica di elaborazione in <https://go.microsoft.com/fwlink/p/?linkid=139649> .



| Funzione                                                                          | Descrizione                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_SHAFinal**](a-shafinal.md)                                                 | Calcola l'hash finale dei dati immessi dalla funzione MD5Update.                                                                                                                                                                                                                                           |
| [**\_SHAInit**](a-shainit.md)                                                   | Avvia l'hashing di un flusso di dati.                                                                                                                                                                                                                                                                       |
| [**\_SHAUpdate**](a-shaupdate.md)                                               | Aggiunge dati a un oggetto hash specificato.                                                                                                                                                                                                                                                                            |
| [**CryptXmlCreateReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlcreatereference)                        | Crea un riferimento a una firma XML.                                                                                                                                                                                                                                                                         |
| [**CryptXmlAddObject**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmladdobject)                                    | Aggiunge l'elemento **oggetto** alla firma nel contesto del documento aperto per la codifica.                                                                                                                                                                                                                        |
| [**CryptXmlClose**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose)                                            | Chiude un handle di oggetto XML crittografico.                                                                                                                                                                                                                                                                        |
| [**CryptXmlDigestReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmldigestreference)                        | Utilizzato da un'applicazione per digerire il riferimento risolto. Questa funzione applica le trasformazioni prima di aggiornare il digest.                                                                                                                                                                                            |
| [**CryptXmlDllCloseDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)                          | Libera il \_ digest XML Crypt \_ allocato dalla funzione [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest) .                                                                                                                                                                                               |
| [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)                        | Crea un oggetto digest per il metodo specificato.                                                                                                                                                                                                                                                                |
| [**CryptXmlDllCreateKey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)                              | Analizza l'elemento del **valore** di chiave e crea un handle di crittografia API: Next Generation (CNG) BCrypt per verificare una firma.                                                                                                                                                                                   |
| [**CryptXmlDllDigestData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)                            | Inserisce i dati nel digest.                                                                                                                                                                                                                                                                                       |
| [**CryptXmlDllEncodeAlgorithm**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)                  | Codifica gli elementi **SignatureMethod** o **DigestMethod** per gli algoritmi agile con parametri predefiniti.                                                                                                                                                                                                           |
| [**CryptXmlDllEncodeKeyValue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)                    | Codifica un elemento del **valore** di un valore.                                                                                                                                                                                                                                                                                  |
| [**CryptXmlDllFinalizeDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)                    | Recupera il valore del digest.                                                                                                                                                                                                                                                                                      |
| [**CryptXmlDllGetAlgorithmInfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)                | Decodifica l'algoritmo XML e restituisce informazioni sull'algoritmo.                                                                                                                                                                                                                                           |
| [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)                        | Recupera un puntatore alle funzioni di estensione crittografica per l'algoritmo specificato.                                                                                                                                                                                                                        |
| [**CryptXmlDllSignData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)                                | Firma i dati.                                                                                                                                                                                                                                                                                                      |
| [**CryptXmlDllVerifySignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)                  | Verifica una firma.                                                                                                                                                                                                                                                                                            |
| [**CryptXmlEncode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlencode)                                          | Codifica i dati della firma utilizzando la funzione di callback del writer XML specificata.                                                                                                                                                                                                                                       |
| [**CryptXmlGetAlgorithmInfo**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetalgorithminfo)                      | Decodifica la \_ struttura dell'algoritmo XML Crypt \_ e restituisce informazioni sull'algoritmo.                                                                                                                                                                                                                         |
| [**CryptXmlGetDocContext**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetdoccontext)                            | Restituisce il contesto del documento specificato dall'handle fornito.                                                                                                                                                                                                                                                   |
| [**CryptXmlGetReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetreference)                              | Restituisce l'elemento di **riferimento** specificato dall'handle fornito.                                                                                                                                                                                                                                              |
| [**CryptXmlGetSignature**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetsignature)                              | Restituisce un elemento della **firma** XML.                                                                                                                                                                                                                                                                            |
| [**CryptXmlGetStatus**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetstatus)                                    | Restituisce una struttura di [**\_ \_ stato Crypt XML**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_status) che contiene informazioni sullo stato relative all'oggetto specificato dall'handle fornito.                                                                                                                                                           |
| [**CryptXmlGetTransforms**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgettransforms)                            | Restituisce informazioni sul motore della catena di trasformazione predefinito.                                                                                                                                                                                                                                                    |
| [**CryptXmlImportPublicKey**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlimportpublickey)                        | Importa la chiave pubblica specificata dall'handle fornito.                                                                                                                                                                                                                                                         |
| [**CryptXmlOpenToEncode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentoencode)                              | Apre una firma digitale XML per codificare e restituisce un handle dell'elemento della **firma** aperta. L'handle incapsula un contesto di documento con una sola struttura di [**\_ \_ firma XML Crypt**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) e rimane aperto fino a quando non viene chiamata la funzione [**CryptXmlClose**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose) . |
| [**CryptXmlOpenToDecode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentodecode)                              | Apre una firma digitale XML da decodificare e restituisce l'handle del contesto del documento che incapsula una struttura della [**\_ \_ firma XML di crittografia**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) . Il contesto del documento può includere uno o più elementi **Signature** .                                                                 |
| [**CryptXmlSetHMACSecret**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsethmacsecret)                            | Imposta il segreto HMAC sull'handle prima di chiamare la funzione [**CryptXmlSign**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign) o [**CryptXmlVerify**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature) .                                                                                                                                                        |
| [**CryptXmlSign**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign)                                              | Crea una firma crittografica di un elemento **SignedInfo** .                                                                                                                                                                                                                                                   |
| [**CryptXmlVerifySignature**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature)                        | Esegue una convalida della firma crittografica di un elemento **SignedInfo** .                                                                                                                                                                                                                                       |
| [*\_callback di \_ \_ scrittura XML Crypt PFN \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_write_callback)            | Crea una trasformazione per un provider di dati specificato.                                                                                                                                                                                                                                                               |
| [*PFN \_ crypt \_ XML \_ Crea \_ trasformazione*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_create_transform)        | Scrive i dati XML di crittografia.                                                                                                                                                                                                                                                                                   |
| [*\_lettura del \_ \_ provider di dati XML Crypt \_ PFN \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_read)   | Legge i dati XML crittografici.                                                                                                                                                                                                                                                                                    |
| [*\_chiusura del \_ \_ provider di dati XML Crypt \_ PFN \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_close) | Rilascia il provider di dati XML crittografico.                                                                                                                                                                                                                                                                    |
| [*informazioni su PFN \_ crypt \_ XML \_ enum \_ \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_enum_alg_info)             | Enumera le voci di [**\_ \_ \_ informazioni dell'algoritmo XML Crypt**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm_info) predefinite e registrate.                                                                                                                                                                                                    |



 

## <a name="signer-functions"></a>Funzioni di firma

Fornisce funzioni per la firma e il timestamp dei dati.



| Funzione                                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SignerFreeSignerContext**](signerfreesignercontext.md) | Libera una struttura del [**\_ contesto del firmatario**](signer-context.md) allocata da una chiamata precedente alla funzione [**SignerSignEx**](signersignex.md) .                                                                                                                                                                                                                                                                      |
| [**SignError**](signerror.md)                             | Chiama la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) e converte il codice restituito in un valore **HRESULT**.                                                                                                                                                                                                                                                                                                            |
| [**SignerSign**](signersign.md)                           | Firma il file specificato.                                                                                                                                                                                                                                                                                                                                                                                           |
| [**SignerSignEx**](signersignex.md)                       | Firma il file specificato e restituisce un puntatore ai dati firmati.                                                                                                                                                                                                                                                                                                                                                  |
| [**SignerSignEx2**](signersignex2.md)                     | Firma e timestamp del file specificato, consentendo più firme nidificate.                                                                                                                                                                                                                                                                                                                                      |
| [**SignerTimeStamp**](signertimestamp.md)                 | Timestamp dell'oggetto specificato. Questa funzione supporta l'indicatore di data e ora Authenticode. Per eseguire il timestamp dell'infrastruttura a chiave pubblica (RFC 3161) X. 509, usare la funzione [**SignerTimeStampEx2**](signertimestampex2.md) .                                                                                                                                                                                       |
| [**SignerTimeStampEx**](signertimestampex.md)             | Timestamp l'oggetto specificato e, facoltativamente, restituisce un puntatore a una struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene un puntatore a un [*BLOB*](../secgloss/b-gly.md). Questa funzione supporta l'indicatore di data e ora Authenticode. Per eseguire il timestamp dell'infrastruttura a chiave pubblica (RFC 3161) X. 509, usare la funzione [**SignerTimeStampEx2**](signertimestampex2.md) . |
| [**SignerTimeStampEx2**](signertimestampex2.md)           | Timestamp l'oggetto specificato e, facoltativamente, restituisce un puntatore a una struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene un puntatore a un [*BLOB*](../secgloss/b-gly.md). Questa funzione può essere usata per eseguire l'infrastruttura a chiave pubblica X. 509, conforme a RFC 3161, timestamp.                                                                                     |
| [**SignerTimeStampEx3**](signertimestampex3.md)           | Timestamp l'oggetto specificato e supporta l'impostazione di timestamp su più firme.                                                                                                                                                                                                                                                                                                                          |



 

## <a name="base-cryptography-functions"></a>Funzioni di crittografia di base

Le funzioni di crittografia di base forniscono il mezzo più flessibile per lo sviluppo di applicazioni di crittografia. Tutte le comunicazioni con un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) si verificano tramite queste funzioni.

Un CSP è un modulo indipendente che esegue tutte le operazioni di crittografia. È necessario almeno un CSP con ogni applicazione che usa funzioni di crittografia. Una singola applicazione può occasionalmente usare più di un CSP.

Se viene utilizzato più di un CSP, è possibile specificare quello da utilizzare nelle chiamate alla funzione di crittografia CryptoAPI. Un CSP, il provider di crittografia di base Microsoft, è incluso in [*CryptoAPI*](../secgloss/c-gly.md). Questo CSP viene utilizzato come provider predefinito da molte delle funzioni CryptoAPI se non è specificato alcun altro CSP.

Ogni CSP fornisce un'implementazione diversa del supporto crittografico fornito a CryptoAPI. Alcune forniscono algoritmi crittografici più avanzati; altri contengono componenti hardware, ad esempio [*Smart Card*](../secgloss/s-gly.md). Inoltre, alcuni DSN possono occasionalmente comunicare direttamente con gli utenti, ad esempio quando le [*firme digitali*](../secgloss/d-gly.md) vengono eseguite utilizzando la [*chiave privata della firma*](../secgloss/s-gly.md)dell'utente.

Le funzioni di crittografia di base si trovano nei gruppi generali seguenti:

-   Funzioni del provider di servizi
-   Funzioni di generazione e scambio di chiavi
-   Funzioni di codifica e decodifica di oggetti
-   Funzioni di crittografia e decrittografia dei dati
-   Funzioni di firma digitale e hash

### <a name="service-provider-functions"></a>Funzioni del provider di servizi

Per connettere e disconnettere un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP), le applicazioni utilizzano le funzioni di servizio seguenti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta"><strong>CryptAcquireContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Acquisisce un handle per il <a href="/windows/desktop/SecGloss/k-gly"><em>contenitore di chiavi</em></a> dell'utente corrente all'interno di un particolare CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcontextaddref"><strong>CryptContextAddRef</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Incrementa il <a href="/windows/desktop/SecGloss/r-gly"><em>conteggio dei riferimenti</em></a> in un handle <a href="hcryptprov.md"><strong>HCRYPTPROV</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidersa"><strong>CryptEnumProviders</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Enumera i provider in un computer.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidertypesa"><strong>CryptEnumProviderTypes</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Enumera i tipi di provider supportati nel computer.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultprovidera"><strong>CryptGetDefaultProvider</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Determina il CSP predefinito per l'utente corrente o per il computer per un tipo di provider specificato.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam"><strong>CryptGetProvParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Recupera i parametri che governano le operazioni di un CSP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>CryptInstallDefaultContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Installa un contesto <a href="hcryptprov.md"><strong>HCRYPTPROV</strong></a> acquisito in precedenza da utilizzare come contesto predefinito.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext"><strong>CryptReleaseContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Rilascia l'handle acquisito dalla funzione <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta"><strong>CryptAcquireContext</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera"><strong>CryptSetProvider</strong></a> e <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetproviderexa"> <strong>CryptSetProviderEx</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Specifica il CSP predefinito dell'utente per un particolare tipo CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam"><strong>CryptSetProvParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Specifica gli attributi di un CSP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptuninstalldefaultcontext"><strong>CryptUninstallDefaultContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Rimuove un contesto predefinito precedentemente installato da <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>CryptInstallDefaultContext</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="freecryptprovfromcertex.md"><strong>FreeCryptProvFromCertEx</strong></a></td>
<td>Rilascia l'handle a un <a href="/windows/desktop/SecGloss/c-gly"><em>provider del servizio di crittografia</em></a> (CSP) o a una chiave Cryptography API: Next Generation (CNG).</td>
</tr>
</tbody>
</table>



 

### <a name="key-generation-and-exchange-functions"></a>Funzioni di generazione e scambio di chiavi

Le funzioni di generazione e scambio di chiave [*scambiano chiavi*](../secgloss/e-gly.md) con altri utenti e creano, configurano ed eliminano le [*chiavi crittografiche*](../secgloss/c-gly.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey"><strong>CryptDeriveKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Crea una chiave derivata da una password.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey"><strong>CryptDestroyKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Elimina definitivamente una chiave.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey"><strong>CryptDuplicateKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Esegue una copia esatta di una chiave, incluso lo <a href="/windows/desktop/SecGloss/s-gly"><em>stato</em></a> della chiave.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey"><strong>CryptExportKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Trasferisce una chiave dal CSP in un <a href="/windows/desktop/SecGloss/k-gly"><em>BLOB di chiavi</em></a> nello spazio di memoria dell'applicazione.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey"><strong>CryptGenKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Crea una chiave casuale.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom"><strong>CryptGenRandom</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Genera dati casuali.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam"><strong>CryptGetKeyParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Recupera i parametri di una chiave.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey"><strong>CryptGetUserKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Ottiene un handle per lo scambio di chiave o la chiave di firma.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey"><strong>CryptImportKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Trasferisce una chiave da un <a href="/windows/desktop/SecGloss/k-gly"><em>BLOB di chiavi</em></a> a un CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Specifica i parametri di una chiave.</td>
</tr>
</tbody>
</table>



 

### <a name="object-encoding-and-decoding-functions"></a>Funzioni di codifica e decodifica di oggetti

Si tratta di funzioni di codifica e decodifica generalizzate. Vengono usati per codificare e decodificare i [*certificati*](../secgloss/c-gly.md), gli [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL), [*le richieste di certificati e le*](../secgloss/c-gly.md)estensioni del certificato.

| Funzione                                           | Descrizione                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)     | Decodifica una struttura di tipo *lpszStructType*.                                                                                                    |
| [**CryptDecodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) | Decodifica una struttura di tipo *lpszStructType*. [**CryptDecodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) supporta l'opzione di allocazione della memoria con una sola sessione. |
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)     | Codifica una struttura di tipo *lpszStructType*.                                                                                                    |
| [**CryptEncodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) | Codifica una struttura di tipo *lpszStructType*. [**CryptEncodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) supporta l'opzione di allocazione della memoria con una sola sessione. |



 

### <a name="data-encryption-and-decryption-functions"></a>Funzioni di crittografia e decrittografia dei dati

Le funzioni seguenti supportano le operazioni di crittografia e decrittografia. [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) e [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) richiedono una [*chiave crittografica*](../secgloss/c-gly.md) prima di essere chiamata. Questa operazione viene eseguita tramite la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)o [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) . L'algoritmo di crittografia viene specificato al momento della creazione della chiave. [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) può impostare parametri di crittografia aggiuntivi.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt"><strong>CryptDecrypt</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Decrittografa una sezione di <a href="/windows/desktop/SecGloss/c-gly"><em>testo crittografato</em></a> utilizzando la chiave di crittografia specificata.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt"><strong>CryptEncrypt</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Crittografa una sezione di <a href="/windows/desktop/SecGloss/p-gly"><em>testo non crittografato</em></a> utilizzando la chiave di crittografia specificata.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></td>
<td>Esegue la crittografia dei dati in una struttura <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>Data_Blob</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>CryptProtectMemory</strong></a></td>
<td>Consente di crittografare la memoria per proteggere le informazioni riservate.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></td>
<td>Esegue un controllo di decrittografia e integrità dei dati in un <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>Data_Blob</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectmemory"><strong>CryptUnprotectMemory</strong></a></td>
<td>Decrittografa la memoria crittografata con <a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>CryptProtectMemory</strong></a>.</td>
</tr>
</tbody>
</table>



 

### <a name="hash-and-digital-signature-functions"></a>Funzioni di firma digitale e hash

Queste funzioni elaborano [*hash*](../secgloss/h-gly.md) di dati e creano e verificano anche le [*firme digitali*](../secgloss/d-gly.md). Gli hash sono noti anche come digest del messaggio.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash"><strong>CryptCreateHash</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Crea un oggetto hash vuoto.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash"><strong>CryptDestroyHash</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Elimina definitivamente un oggetto hash.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatehash"><strong>CryptDuplicateHash</strong></a></td>
<td>Duplica un oggetto hash.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam"><strong>CryptGetHashParam</strong></a></td>
<td>Recupera un parametro dell'oggetto hash.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata"><strong>CryptHashData</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Consente di eseguire l'hashing di un blocco di dati, aggiungendolo all'oggetto hash specificato.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey"><strong>CryptHashSessionKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Consente di eseguire l'hashing di una chiave di sessione e di aggiungerla all'oggetto hash specificato.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam"><strong>CryptSetHashParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Imposta un parametro dell'oggetto hash.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha"><strong>CryptSignHash</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Firma l'oggetto hash specificato.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>CryptUIWizDigitalSign</strong></a></td>
<td>Visualizza una procedura guidata che firma digitalmente un documento o un <a href="/windows/desktop/SecGloss/b-gly"><em>BLOB</em></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizfreedigitalsigncontext"><strong>CryptUIWizFreeDigitalSignContext</strong></a></td>
<td>Rilascia un puntatore a una struttura <a href="/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_context"><strong>CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea"><strong>CryptVerifySignature</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Verifica una firma digitale, dato un handle per l'oggetto hash.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc"><strong>PFNCFILTERPROC</strong></a></td>
<td>Filtra i certificati visualizzati nella creazione guidata firma digitale visualizzata dalla funzione <a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>CryptUIWizDigitalSign</strong></a> .</td>
</tr>
</tbody>
</table>



 

## <a name="certificate-and-certificate-store-functions"></a>Funzioni di archivio certificati e certificati

Le funzioni di archivio certificati e certificati gestiscono l'utilizzo, l'archiviazione e il recupero di [*certificati*](../secgloss/c-gly.md), [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL) ed elenchi di certificati [*attendibili*](../secgloss/c-gly.md) (scopi consentiti). Queste funzioni sono divise nei gruppi seguenti:

-   Funzioni dell'archivio certificati
-   Funzioni di manutenzione dell'archivio certificati e certificati
-   Funzioni per i certificati
-   Funzioni dell'elenco di revoche di certificati
-   Funzioni elenco certificati attendibili
-   Funzioni di proprietà estese
-   Funzioni MakeCert

### <a name="certificate-store-functions"></a>Funzioni dell'archivio certificati

Un sito utente può, nel tempo, raccogliere molti certificati. In genere, un sito dispone di certificati per l'utente del sito, nonché per altri certificati che descrivono gli individui e le entità con cui l'utente comunica. Per ogni entità può essere presente più di un certificato. Per ogni singolo certificato, dovrebbe essere presente una catena di verifica dei certificati che fornisce un ritorno a un [*certificato radice*](../secgloss/r-gly.md)attendibile. Gli [*archivi certificati*](../secgloss/c-gly.md) e le relative funzioni forniscono funzionalità per archiviare, recuperare, enumerare, verificare e utilizzare le informazioni archiviate nei certificati.

| Funzione                                                               | Descrizione                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection)           | Aggiunge un archivio certificati di pari livello a un archivio certificati della raccolta.                                                                                                                                                                                                                                                                       |
| [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)                               | Chiude un handle dell'archivio certificati.                                                                                                                                                                                                                                                                                                        |
| [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore)                           | Consente a un'applicazione di ricevere una notifica in caso di differenza tra il contenuto di un archivio memorizzato nella cache e il contenuto dell'archivio salvato in modo permanente nell'archivio. Fornisce inoltre la desincronizzazione dell'archivio memorizzato nella cache, se necessario, e fornisce un mezzo per eseguire il commit delle modifiche apportate nell'archivio memorizzato nella cache per l'archiviazione permanente.<br/> |
| [**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore)                       | Duplica un handle di archivio incrementando il [*conteggio dei riferimenti*](../secgloss/r-gly.md).                                                                                                                                                                                            |
| [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore)                 | Enumera gli archivi fisici per un archivio di sistema specificato.                                                                                                                                                                                                                                                                              |
| [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)                     | Enumera tutti gli archivi di sistema disponibili.                                                                                                                                                                                                                                                                                                   |
| [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation)     | Enumera tutti i percorsi che dispongono di un archivio di sistema disponibile.                                                                                                                                                                                                                                                                      |
| [**CertGetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty)                   | Ottiene una proprietà dell'archivio.                                                                                                                                                                                                                                                                                                                    |
| [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)                                 | Apre un archivio certificati utilizzando un tipo di provider di archiviazione specificato.                                                                                                                                                                                                                                                                          |
| [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)                     | Apre un archivio certificati di sistema basato su un protocollo del sottosistema.                                                                                                                                                                                                                                                                           |
| [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore)         | Aggiunge un archivio fisico a una raccolta di archivi di sistema del registro di sistema.                                                                                                                                                                                                                                                                              |
| [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore)             | Registra un archivio di sistema.                                                                                                                                                                                                                                                                                                                 |
| [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection) | Rimuove un archivio certificati di pari livello da un archivio di raccolta.                                                                                                                                                                                                                                                                              |
| [**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore)                                 | Salva l'archivio certificati.                                                                                                                                                                                                                                                                                                              |
| [**CertSetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty)                   | Imposta una proprietà dell'archivio.                                                                                                                                                                                                                                                                                                                    |
| [**CertUnregisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore)     | Rimuove un archivio fisico da una raccolta di archivi di sistema specificata.                                                                                                                                                                                                                                                                        |
| [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore)         | Annulla la registrazione di un archivio di sistema specificato.                                                                                                                                                                                                                                                                                                     |
| [**CryptUIWizExport**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizexport)                           | Viene presentata una procedura guidata che consente di esportare un certificato, un elenco di certificati attendibili (CTL), un elenco di revoche di certificati (CRL) o un archivio certificati.                                                                                                                                                                                                      |
| [**CryptUIWizImport**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizimport)                           | Viene presentata una procedura guidata che importa un certificato, un elenco di certificati attendibili (CTL), un elenco di revoche di certificati (CRL) o un archivio certificati.                                                                                                                                                                                                      |



 

### <a name="certificate-and-certificate-store-maintenance-functions"></a>Funzioni di manutenzione dell'archivio certificati e certificati

CryptoAPI fornisce un set di funzioni di manutenzione dell'archivio certificati e certificati generali.

| Funzione                                                                                                                              | Descrizione                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CertAddSerializedElementToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore)                                                            | Aggiunge l'elemento del certificato o del CRL serializzato all'archivio.                                   |
| [**CertCreateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext)                                                                                        | Crea il contesto specificato dai byte codificati. Il nuovo contesto non viene inserito in un archivio. |
| [**CertEnumSubjectInSortedCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsubjectinsortedctl)                                                                      | Enumera il TrustedSubjects in un contesto CTL ordinato.                                        |
| [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl)                                                                                  | Trova l'oggetto specificato in un elenco di scopi consentiti.                                                          |
| [**CertFindSubjectInSortedCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinsortedctl)                                                                      | Trova l'oggetto specificato in un elenco di scopi consentiti ordinato.                                                   |
| [**OpenPersonalTrustDBDialog**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialog) e [ **OpenPersonalTrustDBDialogEx**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialogex) | Consente di visualizzare la finestra di dialogo **certificati** .                                                      |



 

### <a name="certificate-functions"></a>Funzioni per i certificati

La maggior parte delle funzioni di [*certificato*](../secgloss/c-gly.md) dispone di funzioni correlate per gestire [*CRL*](../secgloss/c-gly.md) e [*scopi consentiti*](../secgloss/c-gly.md). Per ulteriori informazioni sulle funzioni CRL e CTL correlate, vedere funzioni elenco di revoche di certificati e funzioni elenco certificati attendibili.

| Funzione                                                                             | Descrizione                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddCertificateContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)         | Aggiunge un contesto del certificato all'archivio certificati.                                                                                                                                                                                            |
| [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)               | Aggiunge un collegamento in un archivio certificati a un contesto di certificato in un archivio diverso.                                                                                                                                                               |
| [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)         | Converte il certificato codificato in un contesto di certificato, quindi aggiunge il contesto all'archivio certificati.                                                                                                                                  |
| [**CertAddRefServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)                 | Incrementa il conteggio dei riferimenti per un handle di **\_ \_ \_ risposta OCSP del server HCERT** .                                                                                                                                                                 |
| [**CertAddRefServerOcspResponseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponsecontext)   | Incrementa il conteggio dei riferimenti per una struttura del [**\_ \_ \_ \_ contesto di risposta OCSP del server CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_server_ocsp_response_context) .                                                                                                              |
| [**CertCloseServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)                   | Chiude un handle di risposta del server OCSP ( [*Online Certificate Status Protocol*](../secgloss/o-gly.md) ).                                               |
| [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)                 | Crea un contesto del certificato da un certificato codificato. Il contesto creato non viene inserito in un archivio certificati.                                                                                                                               |
| [**CertCreateSelfSignCertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreateselfsigncertificate)               | Crea un certificato autofirmato.                                                                                                                                                                                                              |
| [**CertDeleteCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)             | Elimina un certificato dall'archivio certificati.                                                                                                                                                                                               |
| [**CertDuplicateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext)           | Duplica un contesto del certificato incrementando il [*conteggio dei riferimenti*](../secgloss/r-gly.md).                                                                                           |
| [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)                   | Enumera i contesti di certificato nell'archivio certificati.                                                                                                                                                                                   |
| [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)                     | Trova il primo, o successivo, contesto del certificato nell'archivio certificati che soddisfa un criterio di ricerca.                                                                                                                                           |
| [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)                     | Libera un contesto del certificato.                                                                                                                                                                                                                    |
| [**CertGetIssuerCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore)       | Ottiene un contesto del certificato dall'archivio certificati per la prima o la successiva autorità emittente del certificato del soggetto specificato.                                                                                                                      |
| [**CertGetServerOcspResponseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)         | Recupera un contesto di risposta del protocollo di [*stato del certificato in linea*](../secgloss/o-gly.md) (OCSP) non di blocco e di tempo valido per l'handle specificato. |
| [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore)     | Recupera dall'archivio certificati il contesto del certificato dell'oggetto, che viene identificato in modo univoco dall'emittente e dal numero di serie.                                                                                                                  |
| [**CertGetValidUsages**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetvalidusages)                                     | Restituisce una matrice di utilizzi costituiti dall'intersezione degli utilizzi validi per tutti i certificati in una matrice di certificati.                                                                                                               |
| [**CertOpenServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)                     | Apre un handle per una risposta del [*protocollo di stato del certificato online*](../secgloss/o-gly.md) (OCSP) associata a una catena di certificati del server.       |
| [**CertRetrieveLogoOrBiometricInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-certretrievelogoorbiometricinfo)           | Esegue un recupero URL del logo o delle informazioni biometriche specificate nell'estensione del certificato **szOID \_ logotipo \_ ext** o **szOID \_ biometrico \_ ext** .                                                                                  |
| [**CertSelectCertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea)                               | Visualizza una finestra di dialogo che consente all'utente di selezionare i certificati da un set di certificati che corrispondono a un determinato criterio.                                                                                                                       |
| [**CertSelectCertificateChains**](/windows/desktop/api/Wincrypt/nf-wincrypt-certselectcertificatechains)                   | Recupera le catene di certificati in base ai criteri di selezione specificati.                                                                                                                                                                             |
| [**CertSelectionGetSerializedBlob**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-certselectiongetserializedblob)             | Funzione helper utilizzata per recuperare un [*BLOB*](../secgloss/b-gly.md) di certificati serializzati da una struttura [**di \_ \_ input CERT SELECTUI**](/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cert_selectui_input) .                                               |
| [**CertSerializeCertificateStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecertificatestoreelement) | Serializza un certificato codificato del contesto del certificato e una rappresentazione codificata delle relative proprietà.                                                                                                                                         |
| [**CertVerifySubjectCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifysubjectcertificatecontext)   | Esegue i controlli di verifica abilitati sul certificato soggetto utilizzando l'emittente.                                                                                                                                                           |
| [**CryptUIDlgCertMgr**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgcertmgr)                                       | Visualizza una finestra di dialogo che consente all'utente di gestire i certificati.                                                                                                                                                                              |
| [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)                   | Visualizza una finestra di dialogo che consente a un utente di selezionare un certificato.                                                                                                                                                                               |
| [**CryptUIDlgSelectCertificateFromStore**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgselectcertificatefromstore) | Visualizza una finestra di dialogo che consente di selezionare un certificato da un archivio specificato.                                                                                                                                                        |
| [**CryptUIDlgViewCertificate**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea)                       | Visualizza una finestra di dialogo in cui viene visualizzato un certificato specificato.                                                                                                                                                                                    |
| [**CryptUIDlgViewContext**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext)                               | Visualizza un certificato, un CRL o un CTL.                                                                                                                                                                                                            |
| [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)                         | Visualizza una finestra di dialogo contenente le informazioni sul firmatario per un messaggio firmato.                                                                                                                                                                |
| [**GetFriendlyNameOfCert**](/windows/desktop/api/CryptDlg/nf-cryptdlg-getfriendlynameofcerta)                               | Recupera il nome visualizzato per un certificato.                                                                                                                                                                                                   |
| [**RKeyCloseKeyService**](rkeyclosekeyservice.md)                                   | Chiude un handle del servizio Key.                                                                                                                                                                                                                    |
| [**RKeyOpenKeyService**](rkeyopenkeyservice.md)                                     | Apre un handle del servizio chiave in un computer remoto.                                                                                                                                                                                                |
| [**RKeyPFXInstall**](rkeypfxinstall.md)                                             | Installa un certificato in un computer remoto.                                                                                                                                                                                                    |



 

### <a name="certificate-revocation-list-functions"></a>Funzioni dell'elenco di revoche di certificati

Queste funzioni gestiscono l'archiviazione e il recupero degli [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL).

| Funzione                                                             | Descrizione                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddCRLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)         | Aggiunge un contesto CRL all'archivio certificati.                                                                                                                                          |
| [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)               | Aggiunge un collegamento in un archivio a un contesto CRL in un archivio diverso.                                                                                                                         |
| [**CertAddEncodedCRLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)         | Converte l'elenco CRL codificato in un contesto CRL, quindi aggiunge il contesto all'archivio certificati.                                                                                        |
| [**CertCreateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)                 | Crea un contesto CRL da un CRL codificato. Il contesto creato non viene inserito in un archivio certificati.                                                                                     |
| [**CertDeleteCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)             | Elimina un elenco di revoche di certificati dall'archivio certificati.                                                                                                                                             |
| [**CertDuplicateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)           | Duplica un contesto CRL incrementando il conteggio dei [*riferimenti*](../secgloss/r-gly.md).                                         |
| [**CertEnumCRLsInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlsinstore)                   | Enumera i contesti CRL in un archivio.                                                                                                                                               |
| [**CertFindCertificateInCRL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateincrl)         | Esegue la ricerca dell'elenco di revoche di [*certificati*](../secgloss/c-gly.md) (CRL) per il certificato specificato. |
| [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)                     | Trova il primo, o successivo, contesto CRL nell'archivio certificati che corrisponde a un criterio specifico.                                                                                     |
| [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)                     | Libera un contesto CRL.                                                                                                                                                                  |
| [**CertGetCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlfromstore)                   | Ottiene il primo, o successivo, il contesto CRL dall'archivio certificati per il certificato dell'autorità emittente specificato.                                                                                 |
| [**CertSerializeCRLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecrlstoreelement) | Serializza il CRL codificato del contesto CRL e le relative proprietà.                                                                                                                          |



 

### <a name="certificate-trust-list-functions"></a>Funzioni elenco certificati attendibili

Queste funzioni gestiscono l'archiviazione e il recupero degli [*elenchi di certificati attendibili*](../secgloss/c-gly.md) (scopi consentiti).

| Funzione                                                               | Descrizione                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**CertAddCTLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)           | Aggiunge un contesto CTL all'archivio certificati.                                                                         |
| [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)                 | Aggiunge un collegamento in un archivio a un contesto CRL in un archivio diverso.                                                        |
| [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)           | Converte l'elenco di scopi consentiti codificato in un contesto CTL, quindi aggiunge il contesto all'archivio certificati.                       |
| [**CertCreateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext)                   | Crea un contesto CTL da un elenco di certificati attendibili codificati. Il contesto creato non viene inserito in un archivio certificati. |
| [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)               | Elimina un elenco di scopi consentiti dall'archivio certificati.                                                                            |
| [**CertDuplicateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext)             | Duplica un contesto CTL incrementando il conteggio dei riferimenti.                                                        |
| [**CertEnumCTLsInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlsinstore)                     | Enumera i contesti CTL nell'archivio certificati.                                                                |
| [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)                       | Trova il primo, o successivo, contesto CTL nell'archivio certificati che corrisponde a un criterio specifico.                     |
| [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext)                       | Libera un contesto dell'elenco di scopi consentiti.                                                                                                 |
| [**CertModifyCertificatesToTrust**](/windows/desktop/api/CryptDlg/nf-cryptdlg-certmodifycertificatestotrust) | Modifica il set di certificati in un CTL per uno scopo specifico.                                                       |
| [**CertSerializeCTLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializectlstoreelement)   | Serializza il CTL codificato del contesto CTL e le relative proprietà.                                                         |



 

### <a name="extended-property-functions"></a>Funzioni di proprietà estese

Le funzioni seguenti funzionano con le proprietà estese di certificati, CRL e scopi consentiti.

| Funzione                                                                             | Descrizione                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**CertEnumCertificateContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatecontextproperties) | Enumera le proprietà per il contesto del certificato specificato. |
| [**CertEnumCRLContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlcontextproperties)                 | Enumera le proprietà per il contesto CRL specificato.         |
| [**CertEnumCTLContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlcontextproperties)                 | Enumera le proprietà per il contesto CTL specificato.         |
| [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty)       | Recupera le proprietà del certificato.                                |
| [**CertGetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)                       | Recupera le proprietà CRL.                                        |
| [**CertGetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)                       | Recupera le proprietà CTL.                                        |
| [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty)       | Imposta le proprietà del certificato.                                     |
| [**CertSetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)                       | Imposta le proprietà CRL.                                             |
| [**CertSetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)                       | Imposta le proprietà CTL.                                             |



 

## <a name="makecert-functions"></a>Funzioni MakeCert

Le funzioni seguenti supportano lo strumento [Makecert](makecert.md) .



| Funzione                                                                               | Descrizione                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FreeCryptProvFromCert**](freecryptprovfromcert.md)                                 | Rilascia l'handle a un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) ed eventualmente elimina il contenitore temporaneo creato dalla funzione [**GetCryptProvFromCert**](getcryptprovfromcert.md) . |
| [**GetCryptProvFromCert**](getcryptprovfromcert.md)                                   | Ottiene un handle per un CSP e una specifica della chiave per un contesto del certificato.                                                                                                                                                                                                                                |
| [**PvkFreeCryptProv**](pvkfreecryptprov.md)                                           | Rilascia l'handle a un CSP ed eventualmente elimina il contenitore temporaneo creato dalla funzione [**PvkGetCryptProv**](pvkgetcryptprov.md) .                                                                                                                                                          |
| [**PvkGetCryptProv**](pvkgetcryptprov.md)                                             | Ottiene un handle per un CSP in base a un nome di file di [*chiave privata*](../secgloss/p-gly.md) o a un nome del contenitore di chiavi.                                                                                                                                          |
| [**PvkPrivateKeyAcquireContextFromMemory**](pvkprivatekeyacquirecontextfrommemory.md) | Crea un contenitore temporaneo nel CSP e carica una chiave privata dalla memoria nel contenitore.                                                                                                                                                                                                         |
| [**PvkPrivateKeySave**](pvkprivatekeysave.md)                                         | Salva una chiave privata e la relativa [*chiave pubblica*](../secgloss/p-gly.md) corrispondente in un file specificato.                                                                                                                                                          |
| [**SignError**](signerror.md)                                                         | Chiama [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) e converte il codice restituito in un valore **HRESULT**.                                                                                                                                                                                                              |



 

## <a name="certificate-verification-functions"></a>Funzioni di verifica certificati

I certificati vengono verificati tramite [*scopi consentiti*](../secgloss/c-gly.md) o catene di certificati. Per entrambe le funzioni sono disponibili le funzioni seguenti:

-   Funzioni di verifica con scopi consentiti
-   Funzioni di verifica della catena di certificati

### <a name="verification-functions-using-ctls"></a>Funzioni di verifica con scopi consentiti

Queste funzioni usano scopi consentiti nel processo di verifica. Funzioni aggiuntive per l'uso di scopi consentiti sono disponibili in funzioni elenco certificati attendibili e funzioni di proprietà estese.

Le funzioni seguenti usano scopi consentiti direttamente per la verifica.

| Funzione                                                         | Descrizione                                  |
|------------------------------------------------------------------|----------------------------------------------|
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)                 | Verifica l'utilizzo di un elenco di scopi consentiti.                 |
| [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl)     | Codifica e firma un CTL come messaggio.        |
| [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner) | Recupera e verifica un elenco di scopi consentiti da un messaggio. |
| [**CryptMsgSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgsignctl)                       | Firma un messaggio contenente un elenco di scopi consentiti.         |



 

### <a name="certificate-chain-verification-functions"></a>Funzioni di verifica della catena di certificati

Le catene di certificati sono compilate per fornire informazioni di attendibilità sui singoli certificati.

| Nome funzione                                                                                                    | Descrizione                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertCreateCertificateChainEngine**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatechainengine)                                     | Crea un nuovo motore di catena non predefinito per un'applicazione.                                                                                                                                                          |
| [**CertCreateCTLEntryFromCertificateContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlentryfromcertificatecontextproperties) | Crea una voce CTL i cui attributi sono le proprietà del contesto del certificato.                                                                                                                                      |
| [**CertDuplicateCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatechain)                                           | Duplica una catena di certificati incrementando il [*conteggio dei riferimenti*](../secgloss/r-gly.md) della catena e restituendo un puntatore alla catena.                    |
| [**CertFindChainInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindchaininstore)                                                             | Trova il primo, o successivo, contesto della catena di certificati in un archivio.                                                                                                                                                     |
| [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain)                                                     | Libera una catena di certificati riducendo il relativo conteggio dei riferimenti.                                                                                                                                                          |
| [**CertFreeCertificateChainEngine**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainengine)                                         | Libera un motore della catena di certificati non predefinito.                                                                                                                                                                        |
| [**CertFreeCertificateChainList**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainlist)                                             | Libera la matrice di puntatori ai contesti di catena.                                                                                                                                                                      |
| [**CertGetCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatechain)                                                       | Compila un contesto della catena a partire da un certificato finale e tornando a un [*certificato radice*](../secgloss/r-gly.md)attendibile, se possibile.                |
| [**CertIsValidCRLForCertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certisvalidcrlforcertificate)                                             | Controlla un [*elenco di revoche*](../secgloss/c-gly.md) di certificati per determinare se il certificato è stato revocato. |
| [**CertSetCertificateContextPropertiesFromCTLEntry**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextpropertiesfromctlentry)       | Imposta le proprietà nel contesto del certificato usando gli attributi nella voce CTL.                                                                                                                                   |
| [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycertificatechainpolicy)                                     | Verifica una catena di certificati per verificarne la validità, inclusa la rispettiva conformità con i criteri di validità specificati.                                                                                            |



 

## <a name="message-functions"></a>Funzioni di messaggio

Le funzioni di messaggio [*CryptoAPI*](../secgloss/c-gly.md) sono costituite da due gruppi di funzioni: funzioni di messaggio di basso livello e [*funzioni di messaggio semplificate*](../secgloss/s-gly.md).

Le funzioni di messaggio di basso livello creano e funzionano direttamente con \# i messaggi PKCS 7. Queste funzioni codificano \# i dati PKCS 7 per la trasmissione e decodifica \# i dati PKCS 7 ricevuti. Inoltre, decrittografano e verificano le firme dei messaggi ricevuti. Per una panoramica dei \# messaggi standard e di basso livello PKCS 7, vedere [messaggi di basso livello](low-level-messages.md).

Le funzioni di messaggio semplificate sono a un livello superiore e incapsulano diverse funzioni di messaggio e funzioni di certificato di basso livello in funzioni singole che eseguono un'attività specifica in modo specifico. Queste funzioni riducono il numero di chiamate di funzione necessarie per eseguire un'attività, semplificando così l'uso di CryptoAPI. Per una panoramica dei messaggi semplificati, vedere [messaggi semplificati](simplified-messages.md).

-   Funzioni di messaggio di basso livello
-   Funzioni di messaggio semplificate

### <a name="low-level-message-functions"></a>Funzioni di messaggio di basso livello

Le funzioni di messaggio di basso livello offrono le funzionalità necessarie per codificare i dati per la trasmissione e per decodificare \# i messaggi PKCS 7 ricevuti. Viene inoltre fornita la funzionalità per decrittografare e verificare le firme dei messaggi ricevuti. L'utilizzo di queste funzioni di messaggio di basso livello nella maggior parte delle applicazioni non è consigliato. Per la maggior parte delle applicazioni, è preferibile l'uso di funzioni di messaggio semplificate, che incapsulano diverse funzioni di messaggio di basso livello in una singola chiamata di funzione.

| Funzione                                                                                   | Descrizione                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength)                   | Calcola la lunghezza di un messaggio crittografico codificato.                                                                                                                                                                     |
| [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)                                                     | Chiude un handle di un messaggio crittografico.                                                                                                                                                                                    |
| [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)                                                 | Esegue una funzione di controllo speciale dopo l' [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) finale di un messaggio crittografico codificato o decodificato.                                                                                   |
| [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign)                                         | Controfirma una firma già esistente in un messaggio.                                                                                                                                                                       |
| [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded)                           | Controfirma una firma già esistente (SignerInfo codificata, in base a quanto definito da PKCS \# 7).                                                                                                                                       |
| [**CryptMsgDuplicate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgduplicate)                                             | Duplica un handle di messaggio crittografico incrementando il [*conteggio dei riferimenti*](../secgloss/r-gly.md). Il conteggio dei riferimenti tiene traccia della durata del messaggio. |
| [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)                                               | Acquisisce un parametro dopo la codifica o la decodifica di un messaggio crittografico.                                                                                                                                                       |
| [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)                                       | Apre un messaggio crittografico per la decodifica.                                                                                                                                                                                    |
| [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)                                       | Apre un messaggio crittografico per la codifica.                                                                                                                                                                                    |
| [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)                                                   | Aggiorna il contenuto di un messaggio crittografico.                                                                                                                                                                               |
| [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded)     | Verifica un [*controfirma*](../secgloss/c-gly.md) in termini di struttura SignerInfo (come definito da PKCS \# 7).                                                   |
| [**CryptMsgVerifyCountersignatureEncodedEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencodedex) | Verifica che il parametro *pbSignerInfoCounterSignature* contenga l' [*hash*](../secgloss/h-gly.md) crittografato del campo **EncryptedDigest** della struttura del parametro *pbSignerInfo* .   |



 

### <a name="simplified-message-functions"></a>Funzioni di messaggio semplificate

le [*funzioni di messaggio semplificate*](../secgloss/s-gly.md) eseguono il wrapping delle funzioni di messaggio di basso livello in una singola funzione per eseguire un'attività specifica.

| Funzione                                                                               | Descrizione                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptDecodeMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodemessage)                                       | Decodifica un messaggio crittografico.                                                                                                                                                                                                                                             |
| [**CryptDecryptAndVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature) | Decrittografa il messaggio specificato e verifica il firmatario.                                                                                                                                                                                                                     |
| [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)                                     | Decrittografa il messaggio specificato.                                                                                                                                                                                                                                              |
| [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage)                                     | Crittografa il messaggio per il destinatario o i destinatari.                                                                                                                                                                                                                        |
| [**CryptGetMessageCertificates**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagecertificates)                     | Restituisce l' [*archivio certificati*](../secgloss/c-gly.md) che contiene i certificati e i [*CRL*](../secgloss/c-gly.md)del messaggio. |
| [**CryptGetMessageSignerCount**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagesignercount)                       | Restituisce il conteggio dei firmatari nel messaggio firmato.                                                                                                                                                                                                                          |
| [**CryptHashMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashmessage)                                           | Crea un hash del messaggio.                                                                                                                                                                                                                                               |
| [**CryptSignAndEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencryptmessage)                       | Firma il messaggio e quindi lo crittografa per il destinatario o i destinatari.                                                                                                                                                                                                     |
| [**CryptSignMessageWithKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessagewithkey)                             | Firma un messaggio utilizzando la chiave privata del CSP specificata nei parametri della funzione.                                                                                                                                                                                       |
| [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)                                           | Firma il messaggio.                                                                                                                                                                                                                                                           |
| [**CryptVerifyDetachedMessageHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagehash)               | Verifica un messaggio con hash che contiene un hash scollegato.                                                                                                                                                                                                                     |
| [**CryptVerifyDetachedMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagesignature)     | Verifica un messaggio firmato che contiene una firma o firme scollegate.                                                                                                                                                                                                  |
| [**CryptVerifyMessageHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagehash)                               | Verifica un messaggio con hash.                                                                                                                                                                                                                                                   |
| [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)                     | Verifica un messaggio firmato.                                                                                                                                                                                                                                                   |
| [**CryptVerifyMessageSignatureWithKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignaturewithkey)       | Verifica la firma di un messaggio firmato utilizzando le informazioni sulla chiave pubblica specificate.                                                                                                                                                                                             |



 

## <a name="auxiliary-functions"></a>Funzioni ausiliarie

Le funzioni ausiliarie sono raggruppate nel modo seguente:

-   Funzioni Gestione dati
-   Funzioni di conversione dei dati
-   Funzioni di utilizzo chiavi avanzate
-   Funzioni identificatore di chiave
-   Funzioni di supporto OID
-   Funzioni di recupero di oggetti remoti
-   Funzioni PFX

### <a name="data-management-functions"></a>Funzioni Gestione dati

Le funzioni CryptoAPI seguenti gestiscono i dati e i certificati.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificate"><strong>CertCompareCertificate</strong></a></td>
<td>Confronta due certificati per determinare se sono identici.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificatename"><strong>CertCompareCertificateName</strong></a></td>
<td>Confronta due nomi di certificato per determinare se sono identici.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcompareintegerblob"><strong>CertCompareIntegerBlob</strong></a></td>
<td>Confronta due <a href="/windows/desktop/SecGloss/b-gly"><em>BLOB</em></a>Integer.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparepublickeyinfo"><strong>CertComparePublicKeyInfo</strong></a></td>
<td>Confronta due <a href="/windows/desktop/SecGloss/p-gly"><em>chiavi pubbliche</em></a> per determinare se sono identiche.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindattribute"><strong>CertFindAttribute</strong></a></td>
<td>Trova il primo attributo identificato dal relativo <a href="/windows/desktop/SecGloss/o-gly"><em>identificatore di oggetto</em></a> (OID).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindextension"><strong>CertFindExtension</strong></a></td>
<td>Trova la prima estensione identificata dal relativo OID.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindrdnattr"><strong>CertFindRDNAttr</strong></a></td>
<td>Trova il primo attributo <a href="/windows/desktop/SecGloss/r-gly"><em>RDN</em></a> identificato dal relativo OID nell'elenco nome dei <em>nomi distinti relativi</em>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetintendedkeyusage"><strong>CertGetIntendedKeyUsage</strong></a></td>
<td>Acquisisce i byte di utilizzo della chiave previsti dal certificato.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetpublickeylength"><strong>CertGetPublicKeyLength</strong></a></td>
<td>Acquisisce la lunghezza in bit della chiave pubblica/privata dal <a href="/windows/desktop/SecGloss/p-gly"><em>BLOB della chiave pubblica</em></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisrdnattrsincertificatename"><strong>CertIsRDNAttrsInCertificateName</strong></a></td>
<td>Confronta gli attributi nel nome del <a href="/windows/desktop/SecGloss/c-gly"><em>certificato</em></a> con il <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn"><strong>CERT_RDN</strong></a> specificato per determinare se tutti gli attributi sono inclusi in tale nome.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisstronghashtosign"><strong>CertIsStrongHashToSign</strong></a></td>
<td>Determina se l'algoritmo hash specificato e la chiave pubblica nel certificato di firma possono essere utilizzati per eseguire una firma sicura.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrlrevocation"><strong>CertVerifyCRLRevocation</strong></a></td>
<td>Verifica che il certificato dell'oggetto non sia presente nell' <a href="/windows/desktop/SecGloss/c-gly"><em>elenco di revoche di certificati</em></a> (CRL).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrltimevalidity"><strong>CertVerifyCRLTimeValidity</strong></a></td>
<td>Verifica la validità dell'ora di un CRL.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation"><strong>CertVerifyRevocation</strong></a></td>
<td>Verifica che il certificato dell'oggetto non sia presente nel CRL.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifytimevalidity"><strong>CertVerifyTimeValidity</strong></a></td>
<td>Verifica la validità dell'ora di un certificato.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyvaliditynesting"><strong>CertVerifyValidityNesting</strong></a></td>
<td>Verifica che la validità dell'ora dell'oggetto venga annidata entro la validità del tempo dell'emittente.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8"><strong>CryptExportPKCS8</strong></a></td>
<td>Questa funzione è stata sostituita dalla funzione <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>CryptExportPKCS8Ex</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>CryptExportPKCS8Ex</strong></a></td>
<td>Esporta la chiave privata nel formato #8 PKCS.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>CryptExportPublicKeyInfo</strong></a></td>
<td>Esporta le informazioni sulla chiave pubblica associate alla chiave privata corrispondente del provider.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex"><strong>CryptExportPublicKeyInfoEx</strong></a></td>
<td>Esporta le informazioni sulla chiave pubblica associate alla chiave privata corrispondente del provider. Questa funzione differisce da <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>CryptExportPublicKeyInfo</strong></a> in quanto l'utente può specificare l'algoritmo a chiave pubblica, eseguendo l'override del valore predefinito fornito dal CSP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfofrombcryptkeyhandle"><strong>CryptExportPublicKeyInfoFromBCryptKeyHandle</strong></a></td>
<td>Esporta le informazioni sulla chiave pubblica associate alla chiave privata corrispondente di un provider.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindcertificatekeyprovinfo"><strong>CryptFindCertificateKeyProvInfo</strong></a></td>
<td>Enumera i provider di crittografia e i relativi <a href="/windows/desktop/SecGloss/k-gly"><em>contenitori di chiavi</em></a> per trovare la chiave privata corrispondente alla chiave pubblica di un certificato.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindlocalizedname"><strong>CryptFindLocalizedName</strong></a></td>
<td>Trova il nome localizzato per un nome specificato, ad esempio, trova il nome localizzato per il nome del punto vendita del sistema radice.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate"><strong>CryptHashCertificate</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Viene eseguito l'hashing del contenuto codificato.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate2"><strong>CryptHashCertificate2</strong></a></td>
<td>Genera un hash per un blocco di dati tramite un provider hash di Cryptography API: Next Generation (CNG).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashpublickeyinfo"><strong>CryptHashPublicKeyInfo</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Calcola l'hash delle informazioni sulla chiave pubblica codificata.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashtobesigned"><strong>CryptHashToBeSigned</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Calcola l'hash dell'oggetto in &quot; modo da ottenere le informazioni firmate &quot; nel contenuto con segno codificato (<a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_signed_content_info"><strong>CERT_SIGNED_CONTENT_INFO</strong></a>).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8"><strong>CryptImportPKCS8</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Importa la <a href="/windows/desktop/SecGloss/p-gly"><em>chiave privata</em></a> nel formato #8 PKCS in un <a href="/windows/desktop/SecGloss/c-gly"><em>provider del servizio di crittografia</em></a> (CSP).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>CryptImportPublicKeyInfo</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Converte e importa le informazioni sulla chiave pubblica nel provider e restituisce un handle della chiave pubblica.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex"><strong>CryptImportPublicKeyInfoEx</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Converte e importa le informazioni sulla chiave pubblica nel provider e restituisce un handle della chiave pubblica. I parametri aggiuntivi (su quelli specificati da <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>CryptImportPublicKeyInfo</strong></a>) che possono essere usati per sostituire i valori predefiniti vengono forniti per completare <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info"><strong>CERT_PUBLIC_KEY_INFO</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2"><strong>CryptImportPublicKeyInfoEx2</strong></a></td>
<td>Importa una chiave pubblica in un provider asimmetrico CNG.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>CryptMemAlloc</strong></a></td>
<td>Alloca memoria per un buffer. Questa memoria viene utilizzata da tutte le funzioni crypt32. lib che restituiscono buffer allocati.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemfree"><strong>CryptMemFree</strong></a></td>
<td>Libera la memoria allocata da <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>CryptMemAlloc</strong></a> o <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>CryptMemRealloc</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>CryptMemRealloc</strong></a></td>
<td>Libera la memoria attualmente allocata per un buffer e alloca memoria per un nuovo buffer.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptqueryobject"><strong>CryptQueryObject</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Recupera le informazioni sul contenuto di un BLOB o di un file.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate"><strong>CryptSignAndEncodeCertificate</strong></a></td>
<td>Codifica l'oggetto &quot; in modo da ottenere le informazioni firmate &quot; , firma le informazioni codificate e codifica le informazioni codificate risultanti.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsigncertificate"><strong>CryptSignCertificate</strong></a></td>
<td>Firma l'oggetto in &quot; modo da ottenere le informazioni firmate &quot; nel contenuto firmato codificato.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>CryptSIPAddProvider</strong></a></td>
<td>Aggiunge un SIP (Subject Interface Package).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipcreateindirectdata"><strong>CryptSIPCreateIndirectData</strong></a></td>
<td>Restituisce una struttura di <a href="/windows/win32/api/mssip/ns-mssip-sip_indirect_data"><strong>SIP_INDIRECT_DATA</strong></a> contenente un <a href="/windows/desktop/SecGloss/h-gly"><em>hash</em></a> della struttura <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a> fornita, l'algoritmo digest e un attributo di codifica. L'hash può essere utilizzato come riferimento indiretto ai dati.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetcaps"><strong>CryptSIPGetCaps</strong></a></td>
<td>Recupera le funzionalità di un SIP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetsigneddatamsg"><strong>CryptSIPGetSignedDataMsg</strong></a></td>
<td>Recupera una firma Authenticode dal file.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipload"><strong>CryptSIPLoad</strong></a></td>
<td>Carica la libreria a collegamento dinamico che implementa un pacchetto dell'interfaccia del soggetto e assegna le funzioni di esportazione della libreria appropriate a una struttura <a href="/windows/win32/api/mssip/ns-mssip-sip_dispatch_info"><strong>SIP_DISPATCH_INFO</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipputsigneddatamsg"><strong>CryptSIPPutSignedDataMsg</strong></a></td>
<td>Archivia una firma Authenticode nel file di destinazione.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremoveprovider"><strong>CryptSIPRemoveProvider</strong></a></td>
<td>Rimuove un SIP aggiunto da una chiamata precedente alla funzione <a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>CryptSIPAddProvider</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremovesigneddatamsg"><strong>CryptSIPRemoveSignedDataMsg</strong></a></td>
<td>Rimuove una firma Authenticode specificata.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguid"><strong>CryptSIPRetrieveSubjectGuid</strong></a></td>
<td>Recupera un GUID basato sulle informazioni di intestazione in un file specificato.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguidforcatalogfile"><strong>CryptSIPRetrieveSubjectGuidForCatalogFile</strong></a></td>
<td>Recupera il GUID dell'oggetto associato al file specificato.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipverifyindirectdata"><strong>CryptSIPVerifyIndirectData</strong></a></td>
<td>Convalida i dati con hash indiretto rispetto al soggetto fornito.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptupdateprotectedstate"><strong>CryptUpdateProtectedState</strong></a></td>
<td>Esegue la migrazione delle chiavi master dell'utente corrente dopo che l' <a href="/windows/desktop/SecGloss/s-gly"><em>ID di sicurezza</em></a> (SID) dell'utente è stato modificato.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>CryptVerifyCertificateSignature</strong></a></td>
<td>Verifica la firma di un certificato del soggetto o di un <a href="/windows/desktop/SecGloss/c-gly"><em>CRL</em></a> usando le informazioni sulla chiave pubblica.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignatureex"><strong>CryptVerifyCertificateSignatureEx</strong></a></td>
<td>Una versione estesa di <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>CryptVerifyCertificateSignature</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-getencschannel"><strong>GetEncSChannel</strong></a></td>
<td>Archivia il contenuto della DLL Schannel crittografato in memoria.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nc-mssip-pcryptsipgetcaps"><strong>pCryptSIPGetCaps</strong></a></td>
<td>Implementato da un SIP per segnalare le funzionalità.</td>
</tr>
</tbody>
</table>



 

### <a name="data-conversion-functions"></a>Funzioni di conversione dei dati

Le funzioni CryptoAPI seguenti convertono i membri della struttura del certificato in forme diverse.

| Funzione                                           | Descrizione                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAlgIdToOID**](/windows/desktop/api/Wincrypt/nf-wincrypt-certalgidtooid)           | Converte un identificatore dell'algoritmo CryptoAPI ( \_ ID ALG) in una stringa di [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN. 1). |
| [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)     | Acquisisce l'oggetto o il nome dell'autorità emittente da un certificato e lo converte in una stringa di caratteri con terminazione null.                                                                                                                                                                                                               |
| [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra)             | Converte un [*BLOB*](../secgloss/b-gly.md) del nome del certificato in una stringa con terminazione zero.                                                                                                                                                                                                      |
| [**CertOIDToAlgId**](/windows/desktop/api/Wincrypt/nf-wincrypt-certoidtoalgid)           | Converte la stringa dell'identificatore di oggetto ASN. 1 nell'identificatore dell'algoritmo CSP.                                                                                                                                                                                                                                                 |
| [**CertRDNValueToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certrdnvaluetostra)     | Converte un valore di nome in una stringa a terminazione null.                                                                                                                                                                                                                                                                           |
| [**CertStrToName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certstrtonamea)             | Converte una stringa [*X. 500*](../secgloss/x-gly.md) con terminazione null in un nome di certificato codificato.                                                                                                                                                                                          |
| [**CryptBinaryToString**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptbinarytostringa) | Converte una sequenza binaria in una stringa formattata.                                                                                                                                                                                                                                                                          |
| [**CryptFormatObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptformatobject)     | Formatta i dati codificati e restituisce una stringa Unicode.                                                                                                                                                                                                                                                                          |
| [**CryptStringToBinary**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptstringtobinarya) | Converte una stringa formattata in una sequenza binaria.                                                                                                                                                                                                                                                                            |



 

### <a name="enhanced-key-usage-functions"></a>Funzioni di utilizzo chiavi avanzate

Le funzioni seguenti gestiscono l'estensione [*utilizzo chiavi avanzato*](../secgloss/e-gly.md) (EKU) e la proprietà estesa EKU dei certificati. L'estensione EKU e la proprietà estesa specificano e limitano gli utilizzi validi di un certificato. Le estensioni fanno parte del certificato stesso. Sono impostate dall'emittente del certificato e sono di sola lettura. Certificate-le proprietà estese sono valori associati a un certificato che può essere impostato in un'applicazione.

| Funzione                                                                             | Descrizione                                                                    |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**CertAddEnhancedKeyUsageIdentifier**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddenhancedkeyusageidentifier)       | Aggiunge un identificatore di utilizzo alla proprietà EKU di un certificato.                       |
| [**CertGetEnhancedKeyUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetenhancedkeyusage)                           | Acquisisce, da un certificato, informazioni sull'estensione EKU o sulla proprietà. |
| [**CertRemoveEnhancedKeyUsageIdentifier**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremoveenhancedkeyusageidentifier) | Rimuove l'identificatore di utilizzo dalla proprietà estesa EKU di un certificato.       |
| [**CertSetEnhancedKeyUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetenhancedkeyusage)                           | Imposta la proprietà EKU per un certificato.                                       |



 

### <a name="key-identifier-functions"></a>Funzioni identificatore di chiave

Le funzioni dell'identificatore di chiave consentono all'utente di creare, impostare, recuperare o individuare un identificatore di chiave o le relative proprietà.

Un identificatore di chiave è l'identificatore univoco di una [*coppia di chiavi pubblica/privata*](../secgloss/p-gly.md). Può essere qualsiasi identificatore univoco, ma in genere è l'hash SHA1 a 20 byte di una struttura di [**\_ informazioni sulla \_ chiave \_ pubblica del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info) codificato. Un identificatore di chiave può essere ottenuto tramite l'ID Prop dell'identificatore di chiave CERT del certificato \_ \_ \_ \_ . L'identificatore di chiave consente di utilizzare la [*coppia di chiavi*](../secgloss/k-gly.md) per crittografare o decrittografare i messaggi senza utilizzare il certificato.

Gli identificatori di chiave non sono associati a [*CRL*](../secgloss/c-gly.md) o a [*scopi consentiti*](../secgloss/c-gly.md).

Un identificatore di chiave può avere le stesse proprietà di un contesto del certificato. Per ulteriori informazioni, vedere [**CertCreateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatekeyidentifierfromcsp"><strong>CryptCreateKeyIdentifierFromCSP</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Crea un identificatore di chiave da un <a href="/windows/desktop/SecGloss/p-gly"><em>BLOB di chiave pubblica</em></a>del CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties"><strong>CryptEnumKeyIdentifierProperties</strong></a></td>
<td>Enumera gli identificatori di chiave e le relative proprietà.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyidentifierproperty"><strong>CryptGetKeyIdentifierProperty</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Acquisisce una proprietà specifica da un identificatore di chiave specificato.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyidentifierproperty"><strong>CryptSetKeyIdentifierProperty</strong></a></td>
<td><blockquote>
[!Important]<br />
Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le <a href="/windows/desktop/SecCNG/cng-portal">API di prossima generazione di crittografia.</a> Microsoft può rimuovere questa API nelle versioni future.
</blockquote>
<br/> Imposta una proprietà di un identificatore di chiave specificato.</td>
</tr>
</tbody>
</table>



 

### <a name="oid-support-functions"></a>Funzioni di supporto OID

Queste funzioni forniscono il supporto dell' [*identificatore di oggetto*](../secgloss/o-gly.md) (OID). Queste funzioni installano, registrano e inviano a OID e codificano funzioni specifiche del tipo.

Le funzioni CryptoAPI seguenti usano queste funzioni di supporto OID:

-   [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)
-   [**CryptEncodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex)
-   [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)
-   [**CryptDecodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex)
-   [**CertVerifyRevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation)
-   [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)

Per una panoramica di questo processo, vedere [estensione della funzionalità CryptoAPI](extending-cryptoapi-functionality.md).

Le funzioni seguenti funzionano con OID.

| Funzione                                                                       | Descrizione                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptEnumOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction)                           | Enumera le funzioni OID registrate identificate dal tipo di codifica, dal nome della funzione e dall'OID.                                                                                                                 |
| [**CryptEnumOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo)                                   | Enumera le informazioni OID registrate identificate dal relativo gruppo e chiama *pfnEnumOIDInfo* per le corrispondenze.                                                                                                       |
| [**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)                                   | Usa la chiave e il gruppo specificati per trovare le informazioni OID.                                                                                                                                                          |
| [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)             | Rilascia il numero di handle che è stato incrementato e restituito da [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress) o [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress). |
| [**CryptGetDefaultOIDDllList**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoiddlllist)                 | Acquisisce l'elenco di voci DLL predefinite registrate per il set di funzioni e il tipo di codifica specificati.                                                                                                              |
| [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress) | Acquisisce la prima o successiva funzione predefinita installata o carica la DLL che contiene la funzione predefinita.                                                                                                 |
| [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)               | Cerca nell'elenco delle funzioni installate un tipo di codifica e una corrispondenza OID. Se non viene trovata alcuna corrispondenza, viene eseguita la ricerca di una corrispondenza nel registro di sistema.                                                                  |
| [**CryptGetOIDFunctionValue**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionvalue)                   | Acquisisce il valore per il tipo di codifica, il nome della funzione, l'OID e il nome del valore specificati.                                                                                                                            |
| [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset)                     | Inizializza e restituisce un handle del set di funzioni OID identificato dal nome della funzione fornito.                                                                                                                 |
| [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress)       | Installa un set di indirizzi della funzione OID chiamabile.                                                                                                                                                                 |
| [**CryptRegisterDefaultOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisterdefaultoidfunction)     | Registra la DLL che contiene la funzione predefinita da chiamare per il tipo di codifica e il nome della funzione specificati.                                                                                               |
| [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction)                   | Registra la DLL che contiene la funzione da chiamare per il tipo di codifica, il nome della funzione e l'OID specificati.                                                                                                 |
| [**CryptRegisterOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidinfo)                           | Registra le informazioni sull'OID specificate nella struttura di [**\_ \_ Informazioni OID della Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_oid_info) , rendendole in modo permanente nel registro di sistema.                                                                                |
| [**CryptSetOIDFunctionValue**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetoidfunctionvalue)                   | Imposta il valore per il tipo di codifica, il nome della funzione, l'OID e il nome del valore specificati.                                                                                                                                |
| [**CryptUnregisterDefaultOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisterdefaultoidfunction) | Rimuove la registrazione per la DLL che contiene la funzione predefinita da chiamare per il tipo di codifica e il nome della funzione specificati.                                                                            |
| [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction)               | Rimuove la registrazione per la DLL che contiene la funzione da chiamare per il tipo di codifica, il nome della funzione e l'OID specificati.                                                                              |
| [**CryptUnregisterOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidinfo)                       | Rimuove la registrazione per le informazioni OID specificate.                                                                                                                                                        |



 

### <a name="remote-object-retrieval-functions"></a>Funzioni di recupero di oggetti remoti

Le funzioni seguenti consentono all'utente di recuperare un oggetto infrastruttura a chiave pubblica (PKI), acquisire l'URL di un certificato, un elenco di scopi consentiti o un CRL oppure estrarre un URL da un oggetto.

| Funzione                                                     | Descrizione                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**CryptGetObjectUrl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetobjecturl)               | Acquisisce l'URL dell'oggetto remoto da un certificato, un elenco di scopi consentiti o un CRL. |
| [**CryptRetrieveObjectByUrl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptretrieveobjectbyurla) | Recupera l'oggetto PKI da un percorso specificato da un URL.           |



 

### <a name="pfx-functions"></a>Funzioni PFX

Le funzioni seguenti supportano i [*BLOB*](../secgloss/b-gly.md)in formato pfx (Personal Information Exchange).

| Funzione                                             | Descrizione                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PFXExportCertStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstore)     | Le esportazioni dal certificato a cui si fa riferimento [*archiviano*](../secgloss/c-gly.md) i certificati e, se disponibili, le relative [*chiavi private*](../secgloss/p-gly.md)associate. |
| [**PFXExportCertStoreEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstoreex) | Le esportazioni dal certificato a cui si fa riferimento archiviano i certificati e, se disponibili, le relative chiavi private associate.                                                                                                                                                             |
| [**PFXImportCertStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfximportcertstore)     | Importa un BLOB PFX e restituisce l'handle di un archivio che contiene i certificati e le chiavi private associate.                                                                                                                                                            |
| [**PFXIsPFXBlob**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxispfxblob)                 | Tenta di decodificare il livello esterno di un BLOB come pacchetto PFX.                                                                                                                                                                                                                |
| [**PFXVerifyPassword**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxverifypassword)       | Tenta di decodificare il livello esterno di un BLOB come pacchetto PFX e di decrittografarlo con la password specificata.                                                                                                                                                                      |



 

## <a name="certificate-services-backup-and-restore-functions"></a>Funzioni di backup e ripristino di Servizi certificati

Servizi certificati include funzioni per il backup e il ripristino del database di Servizi certificati. Queste funzioni di backup e ripristino di Servizi certificati sono contenute in Certadm.dll. Diversamente dagli altri elementi API associati ai Servizi certificati, queste funzioni non sono incapsulate in un oggetto che può essere usato per chiamare i metodi della classe. Al contrario, le API di backup e ripristino vengono chiamate caricando prima la libreria Certadm.dll in memoria chiamando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e quindi determinando l'indirizzo delle funzioni chiamando [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Una volta terminata la chiamata alle funzioni di backup e ripristino di Servizi certificati, chiamare [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) per liberare Certadm.dll risorse dalla memoria.

> [!Note]
> Le funzioni di backup e ripristino fornite da Certadm.dll non eseguono il backup o il ripristino delle [*chiavi private*](../secgloss/p-gly.md)del servizio certificati. Per informazioni sul backup delle chiavi private dei servizi certificati, vedere [backup e ripristino della chiave privata Servizi certificati](backing-up-and-restoring-the-certificate-services-private-key.md).
> 
> Per chiamare le funzioni di backup e ripristino, è necessario disporre dei [*privilegi*](../secgloss/p-gly.md)di backup e ripristino. Per informazioni dettagliate, vedere [impostazione dei privilegi di backup e ripristino](setting-the-backup-and-restore-privileges.md).

 

> [!Note]  
> Se **CoInitializeEx** è stato chiamato in precedenza nello stesso thread usato per chiamare le API di backup e ripristino di Servizi certificati, il flag CoInit \_ ApartmentThreaded deve essere stato passato a **CoInitializeEx**. Ovvero, quando si usa lo stesso thread, non è possibile chiamare l'API di backup e ripristino di Servizi certificati se il thread ha passato in precedenza il flag CoInit \_ MULTIthreading in una chiamata a **CoInitializeEx**.

 

Le API di backup di Servizi certificati sono definite in certbcli. h. Tuttavia, quando si crea il programma, usare certsrv. h come file di inclusione.

Le API seguenti vengono esportate da Certadm.dll.

| Funzione                                                                         | Descrizione                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**CertSrvBackupClose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose)                                 | Chiude un file aperto.                                                                                                |
| [**CertSrvBackupEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend)                                     | Termina una sessione di backup.                                                                                                |
| [**CertSrvBackupFree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree)                                   | Libera un buffer allocato dalle API di backup e ripristino.                                                              |
| [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw)                 | Restituisce un elenco di file di log di cui è necessario eseguire il backup.                                                                |
| [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)           | Restituisce un elenco di file di database di cui è necessario eseguire il backup.                                                           |
| [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw)       | Recupera l'elenco dei nomi di file dinamici di Servizi certificati di cui è necessario eseguire il backup per il contesto di backup specificato. |
| [**CertSrvBackupOpenFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew)                           | Apre un file in preparazione per il backup.                                                                        |
| [**CertSrvBackupPrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew)                             | Prepara il database per il backup online.                                                                          |
| [**CertSrvBackupRead**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread)                                   | Legge il contenuto di un file aperto.                                                                                 |
| [**CertSrvBackupTruncateLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs)                   | Tronca i file di log.                                                                                              |
| [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew)                           | Determina se un server di Servizi certificati è online (in esecuzione attiva).                                        |
| [**CertSrvRestoreEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend)                                   | Termina una sessione di ripristino.                                                                                               |
| [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) | Recupera i percorsi di database (utilizzati per gli scenari di backup e ripristino).                                            |
| [**CertSrvRestorePrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew)                           | Avvia una sessione di ripristino.                                                                                             |
| [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw)                         | Registra un'operazione di ripristino.                                                                                        |
| [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete)         | Completa un'operazione di ripristino registrata in precedenza.                                                                  |
| [**CertSrvRestoreRegisterThroughFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterthroughfile)   | Registra un'operazione di ripristino.                                                                                        |
| [**CertSrvServerControl**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvservercontrolw)                             | Invia un comando di controllo all'istanza di Servizi certificati.                                                         |



 

## <a name="callback-functions"></a>Funzioni di callback

Le funzioni di callback in questa sezione vengono usate per registrare o installare i provider dell' [*archivio certificati*](../secgloss/c-gly.md) definiti dall'applicazione e per fornire funzionalità correlate tramite funzioni di callback. Le funzioni di callback sono implementate da un'applicazione e vengono chiamate dalle funzioni [*CryptoAPI*](../secgloss/c-gly.md) . Le funzioni di callback consentono all'applicazione di controllare, in parte, il modo in cui le funzioni CryptoAPI modificano i dati.

| Funzione di callback                                                                                                        | Uso                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertChainFindByIssuerCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_chain_find_by_issuer_callback)                                                   | Funzione di callback definita dall'applicazione che consente all'applicazione di filtrare i certificati che potrebbero essere aggiunti alla catena di certificati.                                                                                                                                                                                                     |
| [**CertDllOpenStoreProv**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func)                                                                     | Definisce la funzione Open del provider di archiviazione.                                                                                                                                                                                                                                                                                                     |
| [**CertEnumPhysicalStoreCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_physical_store)                                                   | Funzione di callback utilizzata dalla funzione [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) per formattare e presentare informazioni su ogni archivio fisico trovato.                                                                                                                                                                                 |
| [**CertEnumSystemStoreCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store)                                                       | Funzione di callback utilizzata dalla funzione [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore) per formattare e presentare informazioni su ogni archivio fisico trovato.                                                                                                                                                                                     |
| [**CertEnumSystemStoreLocationCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store_location)                                       | Funzione di callback utilizzata dalla funzione [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation) per formattare e presentare informazioni su ogni archivio fisico trovato.                                                                                                                                                                     |
| [**CertStoreProvCloseCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_close)                                                         | Determina cosa accade quando il [*conteggio dei riferimenti*](../secgloss/r-gly.md) di un archivio aperto diventa zero.                                                                                                                                                                                    |
| [**CertStoreProvControl**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_control)                                                                     | Consente a un'applicazione di ricevere una notifica quando esiste una differenza tra il contenuto di un archivio memorizzato nella cache in uso e il contenuto di tale archivio come salvato in modo permanente nell'archivio.                                                                                                                                                                   |
| [**CertStoreProvDeleteCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_cert)                                               | Determina le azioni da intraprendere prima che un certificato venga eliminato da un archivio certificati.                                                                                                                                                                                                                                                      |
| [**CertStoreProvDeleteCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_crl)                                                 | Determina le azioni da intraprendere prima che un [*elenco di revoche di certificati*](../secgloss/c-gly.md) (CRL) venga eliminato da un archivio certificati.                                                                                                                        |
| [**CertStoreProvDeleteCTL**](certstoreprovdeletectl.md)                                                                 | Determina se è possibile eliminare un elenco di scopi consentiti.                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvFindCert**](certstoreprovfindcert.md)                                                                   | Trova il primo certificato, o successivo, in un archivio che soddisfa i criteri specificati.                                                                                                                                                                                                                                                             |
| [**CertStoreProvFindCRL**](certstoreprovfindcrl.md)                                                                     | Trova il CRL primo o successivo in un archivio che soddisfa i criteri specificati.                                                                                                                                                                                                                                                                     |
| [**CertStoreProvFindCTL**](certstoreprovfindctl.md)                                                                     | Trova il primo, o successivo, CTL in un archivio che corrisponde ai criteri specificati.                                                                                                                                                                                                                                                                     |
| [**CertStoreProvFreeFindCert**](certstoreprovfreefindcert.md)                                                           | Libera un contesto del certificato trovato in precedenza.                                                                                                                                                                                                                                                                                                 |
| [**CertStoreProvFreeFindCRL**](certstoreprovfreefindcrl.md)                                                             | Libera un contesto CRL trovato in precedenza.                                                                                                                                                                                                                                                                                                         |
| [**CertStoreProvFreeFindCTL**](certstoreprovfreefindctl.md)                                                             | Libera un contesto CTL trovato in precedenza.                                                                                                                                                                                                                                                                                                         |
| [**CertStoreProvGetCertProperty**](certstoreprovgetcertproperty.md)                                                     | Recupera una proprietà specificata di un certificato.                                                                                                                                                                                                                                                                                              |
| [**CertStoreProvGetCRLProperty**](certstoreprovgetcrlproperty.md)                                                       | Recupera una proprietà specificata di un CRL.                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvGetCTLProperty**](certstoreprovgetctlproperty.md)                                                       | Recupera una proprietà specificata di un elenco di scopi consentiti.                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_cert)                                                   | Attualmente non utilizzato ma potrebbe essere esportato in CSP futuri.                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_crl)                                                     | Attualmente non utilizzato ma potrebbe essere esportato in CSP futuri.                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCTL**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_read_ctl)                                                                     | Leggere la copia del provider del contesto CTL e, se esiste, creare un nuovo contesto CTL.                                                                                                                                                                                                                                                     |
| [**CertStoreProvSetCertPropertyCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_cert_property)                                     | Determina le azioni da intraprendere prima di una chiamata a [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty) o [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty).                                                                                                                             |
| [**CertStoreProvSetCRLPropertyCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_crl_property)                                       | Determina le azioni da intraprendere prima di una chiamata a [**CertSetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty) o [**CertGetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty).                                                                                                                                                             |
| [**CertStoreProvSetCTLProperty**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_ctl_property)                                                       | Determina se una proprietà può essere impostata su un elenco di scopi consentiti.                                                                                                                                                                                                                                                                                            |
| [**CertStoreProvWriteCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_cert)                                                 | Determina le azioni da intraprendere prima di aggiungere un certificato a un archivio.                                                                                                                                                                                                                                                                        |
| [**CertStoreProvWriteCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_crl)                                                   | Determina le azioni da intraprendere prima di aggiungere un CRL a un archivio.                                                                                                                                                                                                                                                                                |
| [**CertStoreProvWriteCTL**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_ctl)                                                                   | Determina se un elenco di scopi consentiti può essere aggiunto all'archivio.                                                                                                                                                                                                                                                                                           |
| [**KEYID (CRYPT \_ enum) \_ \_ prop**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_keyid_prop)                                                                | Funzione di callback utilizzata dalla funzione [**CryptEnumKeyIdentifierProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties) .                                                                                                                                                                                                                          |
| [**CRYPT \_ enum \_ ( \_ funzione OID)**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_func)                                                            | Funzione di callback utilizzata dalla funzione [**CryptEnumOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction) .                                                                                                                                                                                                                                                  |
| [**\_ \_ informazioni Oid enum \_ enum**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_info)                                                                    | Funzione di callback utilizzata dalla funzione [**CryptEnumOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo) .                                                                                                                                                                                                                                                          |
| [**CryptGetSignerCertificateCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_get_signer_certificate)                                           | Funzione di callback utilizzata con la struttura del messaggio di verifica della Crypt per ottenere e verificare il certificato del firmatario di un messaggio. [**\_ \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para)                                                                                                                                                                                 |
| [**PCRYPT \_ Decrypt \_ \_ chiave privata \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_decrypt_private_key_func)                                           | Funzione di callback utilizzata dalla funzione [**CryptImportPKCS8**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8) .                                                                                                                                                                                                                                                          |
| [**PCRYPT \_ Crittografa \_ \_ chiave privata \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_encrypt_private_key_func)                                           | Funzione di callback utilizzata durante la creazione della struttura di [**\_ \_ \_ \_ informazioni chiave privata crittografata Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_encrypted_private_key_info) .                                                                                                                                                                                                          |
| [**PCRYPT \_ risolvere \_ HCRYPTPROV \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_resolve_hcryptprov_func)                                              | Funzione di callback utilizzata dalla funzione [**CryptImportPKCS8**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8) .                                                                                                                                                                                                                                                          |
| [**\_ \_ callback errore di analisi CDF \_ PFN \_**](/windows/win32/api/mscat/nc-mscat-pfn_cdf_parse_error_callback)                                                 | Funzione definita dall'utente chiamata per gli errori della funzione di definizione del catalogo durante l'analisi di un file di definizione del catalogo (CDF).                                                                                                                                                                                                                          |
| [**funzione \_ di \_ \_ ordinamento del contesto di creazione \_ del certificato PFN \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_create_context_sort_func)                                      | Chiamato per ogni voce di contesto ordinata quando viene creato un contesto.                                                                                                                                                                                                                                                                               |
| [**\_chiave di \_ \_ crittografia del \_ contenuto di importazione \_ \_ PFN CMSG CNG**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_content_encrypt_key)                         | Funzione di [*identificatore di oggetto*](../secgloss/o-gly.md) CNG (OID) installabile per l'importazione di una chiave di crittografia del contenuto già decrittografata (CEK).                                                                                                                                       |
| [**PFN \_ CMSG \_ - \_ chiave di importazione CNG \_ \_ accetta**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_agree)                                              | Importa una chiave di crittografia del contenuto per un destinatario di trasporto chiave di un messaggio in busta digitale.                                                                                                                                                                                                                                                       |
| [**\_ \_ \_ \_ transazione chiave importazione CNG CMSG \_ PFN**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_trans)                                              | Funzione installabile dell'OID CNG per l'importazione e la [*decrittografia*](../secgloss/d-gly.md) di una chiave di trasporto/destinatario crittografata, [*crittografia*](../secgloss/e-gly.md) del contenuto (CEK).                                                                   |
| [**\_accettazione della \_ chiave di esportazione CMSG \_ di PFN \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_agree)                                                       | Crittografa ed Esporta la chiave di crittografia del contenuto per un destinatario di un contratto chiave di un messaggio in busta digitale.                                                                                                                                                                                                                                        |
| [**PFN \_ CMSG \_ esportazione \_ chiave \_ Trans**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_trans)                                                       | Crittografa ed Esporta la chiave di crittografia del contenuto per un destinatario di trasporto chiave di un messaggio in busta digitale.                                                                                                                                                                                                                                        |
| [**\_elenco di \_ esportazione della \_ posta \_ PFN CMSG**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_mail_list)                                                       | Crittografa ed Esporta la chiave di crittografia del contenuto per un destinatario di una lista di distribuzione di un messaggio in busta digitale.                                                                                                                                                                                                                                         |
| [**PFN \_ CMSG \_ - \_ \_ chiave di crittografia contenuto gen \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_gen_content_encrypt_key)                                        | Genera la [*chiave simmetrica*](../secgloss/s-gly.md) utilizzata per crittografare il contenuto di un messaggio in busta digitale.                                                                                                                                                                                     |
| [**\_ \_ Accetto chiave di importazione CMSG \_ di \_ PFN**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_agree)                                                       | Importa una chiave di crittografia del contenuto per un destinatario di trasporto chiave di un messaggio in busta digitale.                                                                                                                                                                                                                                                       |
| [**\_ \_ trasporto chiave di importazione CMSG \_ di \_ PFN**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_trans)                                                       | Importa una chiave di crittografia del contenuto per un destinatario di trasporto chiave di un messaggio in busta digitale.                                                                                                                                                                                                                                                       |
| [**\_elenco di \_ messaggi di importazione PFN CMSG \_ \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_mail_list)                                                       | Importa una chiave di crittografia del contenuto per un destinatario di trasporto chiave di un messaggio in busta digitale.                                                                                                                                                                                                                                                       |
| [**PFN \_ crypt \_ Export \_ public \_ Key \_ info \_ EX2 \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_export_public_key_info_ex2_func)                    | Chiamato da [**CryptExportPublicKeyInfoEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex) per esportare un BLOB di chiave pubblica e codificarlo.                                                                                                                                                                                                                         |
| [**funzione \_ di \_ estrazione dei \_ parametri della \_ firma codificata \_ \_ PFN**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_extract_encoded_signature_parameters_func) | Chiamato per decodificare e restituire l'identificatore dell'algoritmo hash e, facoltativamente, i parametri della firma.                                                                                                                                                                                                                                            |
| [**PFN \_ crypt \_ Sign \_ e \_ Encode \_ hash \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_sign_and_encode_hash_func)                                 | Chiamato per firmare e codificare un hash calcolato.                                                                                                                                                                                                                                                                                                    |
| [**PFN \_ - \_ Verifica della \_ firma codificata di \_ \_ crypt**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_verify_encoded_signature_func)                          | Chiamato per decrittografare una firma codificata e confrontarla con un hash calcolato.                                                                                                                                                                                                                                                                     |
| [**PFN \_ import \_ public \_ Key \_ info \_ EX2 \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_import_public_key_info_ex2_func)                                 | Chiamato da [**CryptImportPublicKeyInfoEx2**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2) per decodificare l'identificatore dell' [*algoritmo a chiave pubblica*](../secgloss/p-gly.md) , caricare il provider dell'algoritmo e importare la [*coppia di chiavi*](../secgloss/k-gly.md). |
| [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md)                                                                       | Funzione di callback definita dall'utente che consente al chiamante della funzione [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) di gestire la visualizzazione dei certificati selezionati dall'utente per la visualizzazione.                                                                                                                               |
| [**PFNCMFILTERPROC**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmfilterproc)                                                                               | Filtra ogni certificato per decidere se verrà visualizzato nella finestra di dialogo di selezione del certificato visualizzata dalla funzione [**CertSelectCertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea) .                                                                                                                                                                |
| [**PFNCMHOOKPROC**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmhookproc)                                                                                   | Chiamato prima che i messaggi vengano elaborati dalla finestra di dialogo di selezione del certificato prodotta dalla funzione [**CertSelectCertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea) .                                                                                                                                                                                 |



 

## <a name="catalog-definition-functions"></a>Funzioni di definizione Catalogo

Queste funzioni vengono usate per creare un catalogo. Tutte queste funzioni vengono chiamate da [MakeCat](makecat.md).

| Funzione                                                                           | Descrizione                                                                                                               |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**CryptCATCDFClose**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfclose)                                       | Chiude un file di definizione del catalogo e libera la memoria per la struttura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) corrispondente. |
| [**CryptCATCDFEnumAttributesWithCDFTag**](cryptcatcdfenumattributeswithcdftag.md) | Enumera gli attributi dei file membro nella sezione **CatalogFiles** di un CDF.                                       |
| [**CryptCATCDFEnumCatAttributes**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfenumcatattributes)               | Enumera gli attributi a livello di catalogo all'interno della sezione **CatalogHeader** di un CDF.                                        |
| [**CryptCATCDFEnumMembersByCDFTagEx**](cryptcatcdfenummembersbycdftagex.md)       | Enumera i singoli membri del file nella sezione **CatalogFiles** di un CDF.                                          |
| [**CryptCATCDFOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfopen)                                         | Apre un CDF esistente per la lettura e l'inizializzazione di una struttura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .                         |



 

## <a name="catalog-functions"></a>Funzioni di catalogo

Queste funzioni vengono utilizzate per gestire un catalogo.

| Funzione                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptCATAdminAcquireContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext)                   | Acquisisce un handle per un contesto di amministratore del catalogo. Questo handle può essere utilizzato dalle chiamate successive alle funzioni [**CryptCATAdminAddCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog), [**CryptCATAdminEnumCatalogFromHash**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)e [**CryptCATAdminRemoveCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog) . |
| [**CryptCATAdminAcquireContext2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext2)                 | Acquisisce un handle per un contesto di amministratore del catalogo per un determinato algoritmo hash e criteri hash.                                                                                                                                                                                                                                   |
| [**CryptCATAdminAddCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog)                           | Aggiunge un catalogo al database del catalogo.                                                                                                                                                                                                                                                                                            |
| [**CryptCATAdminCalcHashFromFileHandle**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle)   | Calcola l'hash per un file.                                                                                                                                                                                                                                                                                                    |
| [**CryptCATAdminCalcHashFromFileHandle2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle2) | Calcola l'hash per un file utilizzando l'algoritmo specificato.                                                                                                                                                                                                                                                                   |
| [**CryptCATAdminEnumCatalogFromHash**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)         | Enumera i cataloghi che contengono un hash specificato.                                                                                                                                                                                                                                                                             |
| [**CryptCATAdminReleaseCatalogContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecatalogcontext)     | Rilascia un handle a un contesto del catalogo precedentemente restituito dalla funzione [**CryptCATAdminAddCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog) .                                                                                                                                                                                             |
| [**CryptCATAdminReleaseContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecontext)                   | Rilascia l'handle assegnato in precedenza dalla funzione [**CryptCATAdminAcquireContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext) .                                                                                                                                                                                                        |
| [**CryptCATAdminRemoveCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog)                     | Elimina un file di catalogo e rimuove la voce del catalogo dal database del catalogo di Windows.                                                                                                                                                                                                                                         |
| [**CryptCATAdminResolveCatalogPath**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminresolvecatalogpath)           | Recupera il percorso completo del catalogo specificato.                                                                                                                                                                                                                                                                       |
| [**CryptCATCatalogInfoFromContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcataloginfofromcontext)             | Recupera le informazioni del catalogo da un contesto del catalogo specificato.                                                                                                                                                                                                                                                                    |
| [**CryptCATClose**](/windows/desktop/api/Mscat/nf-mscat-cryptcatclose)                                               | Chiude un handle del catalogo aperto in precedenza dalla funzione [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) .                                                                                                                                                                                                                                    |
| [**CryptCATEnumerateAttr**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumerateattr)                               | Enumera gli attributi associati a un membro di un catalogo.                                                                                                                                                                                                                                                                   |
| [**CryptCATEnumerateCatAttr**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratecatattr)                         | Enumera gli attributi associati a un catalogo.                                                                                                                                                                                                                                                                               |
| [**CryptCATEnumerateMember**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratemember)                           | Enumera i membri di un catalogo.                                                                                                                                                                                                                                                                                               |
| [**CryptCATGetAttrInfo**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetattrinfo)                                   | Recupera le informazioni su un attributo di un membro di un catalogo.                                                                                                                                                                                                                                                                 |
| [**CryptCATGetMemberInfo**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetmemberinfo)                               | Recupera le informazioni sui membri dall'oggetto PKCS \# 7 del catalogo. Oltre a recuperare le informazioni sui membri per un tag di riferimento specificato, questa funzione apre un contesto del membro.                                                                                                                                                    |
| [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen)                                                 | Apre un catalogo e restituisce un handle di contesto al catalogo aperto.                                                                                                                                                                                                                                                                 |
| [**IsCatalogFile**](/windows/desktop/api/Mscat/nf-mscat-iscatalogfile)                                               | Recupera un valore booleano che indica se il file specificato è un file di catalogo.                                                                                                                                                                                                                                             |



 

## <a name="wintrust-functions"></a>Funzioni WinTrust

Le funzioni seguenti vengono usate per eseguire varie operazioni di trust.

| Funzione                                                                               | Descrizione                                                                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WintrustAddActionID**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid)                                     | Aggiunge un'azione del provider di attendibilità al sistema dell'utente.                                                                                                                   |
| [**WintrustGetRegPolicyFlags**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetregpolicyflags)                         | Recupera i flag dei criteri per un provider di criteri.                                                                                                                        |
| [**WintrustAddDefaultForUsage**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustadddefaultforusage)                       | Specifica l'identificatore di utilizzo predefinito e le informazioni di callback per un provider                                                                                       |
| [**WintrustGetDefaultForUsage**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetdefaultforusage)                       | Recupera l'identificatore di utilizzo predefinito e le informazioni di callback.                                                                                                     |
| [**WintrustLoadFunctionPointers**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustloadfunctionpointers)                   | Carica i punti di ingresso della funzione per un GUID di azione specificato.                                                                                                             |
| [**WintrustRemoveActionID**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustremoveactionid)                               | Rimuove un'azione aggiunta dalla funzione [**WintrustAddActionID**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid) .                                                                          |
| [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) | Imposta l'impostazione predefinita che determina se vengono inclusi gli hash di pagina durante la creazione di dati indiretti del pacchetto dell'interfaccia del soggetto (SIP) per i file eseguibili portabili. |
| [**WintrustSetRegPolicyFlags**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetregpolicyflags)                         | Imposta i flag dei criteri per un provider di criteri.                                                                                                                             |
| [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust)                                               | Esegue un'azione di verifica dell'attendibilità su un oggetto specificato.                                                                                                          |
| [**WinVerifyTrustEx**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrustex)                                           | Esegue un'azione di verifica dell'attendibilità su un oggetto specificato e accetta un puntatore a una \_ struttura di dati wintrust.                                                        |
| [**WTHelperCertCheckValidSignature**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertcheckvalidsignature)             | Verifica se una firma è valida.                                                                                                                                 |
| [**WTHelperCertFindIssuerCertificate**](wthelpercertfindissuercertificate.md)         | Trova un certificato dell'autorità emittente dagli archivi certificati specificati che corrisponde al certificato dell'oggetto specificato.                                                    |
| [**WTHelperCertIsSelfSigned**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertisselfsigned)                           | Verifica se un certificato è autofirmato.                                                                                                                         |
| [**WTHelperGetFileHash**](wthelpergetfilehash.md)                                     | Verifica la firma di un file firmato e ottiene il valore hash e l'identificatore dell'algoritmo per il file.                                                            |
| [**WTHelperGetProvCertFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovcertfromchain)                   | Recupera un certificato del provider di attendibilità dalla catena di certificati.                                                                                                   |
| [**WTHelperGetProvPrivateDataFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovprivatedatafromchain)     | Riceve una [**struttura \_ \_ PRIVDATA del provider di crittografia**](/windows/desktop/api/Wintrust/ns-wintrust-crypt_provider_privdata) dalla catena utilizzando l'ID del provider.                                           |
| [**WTHelperGetProvSignerFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovsignerfromchain)               | Recupera un firmatario o countersigner in base all'indice dalla catena.                                                                                                         |
| [**WTHelperProvDataFromStateData**](/windows/desktop/api/Wintrust/nf-wintrust-wthelperprovdatafromstatedata)                 | Recupera le informazioni sul provider di attendibilità da un handle specificato.                                                                                                        |



 

## <a name="object-locator-functions"></a>Funzioni del localizzatore di oggetti

Le funzioni di callback seguenti possono essere implementate da un provider personalizzato che deve essere chiamato dal pacchetto di sicurezza del canale sicuro (Schannel) per recuperare i certificati.



| Funzione                                                                                                             | Descrizione                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [**Scaricamento del provider di PFN \_ crypt \_ Object \_ Locator \_ \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_flush)                      | Specifica che un oggetto è stato modificato.                   |
| [**PFN \_ crypt \_ Object \_ Locator \_ provider \_ Get**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get)                          | Recupera un oggetto.                                    |
| [**PFN \_ crypt \_ Object \_ Locator \_ provider \_ versione**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_release)                  | Rilascia il provider.                                  |
| [**\_ \_ \_ \_ password gratuita del provider del localizzatore di oggetti \_ crypt \_ PFN**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_password)     | Rilascia la password utilizzata per crittografare una matrice di byte PFX. |
| [**\_provider PFN Crypt \_ Object \_ Locator \_ \_ gratuito**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free)                        | Rilascia l'oggetto restituito dal provider.           |
| [**\_ \_ \_ \_ identificatore libero del provider del localizzatore di oggetti \_ crypt \_ PFN**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_identifier) | Rilascia la memoria per un identificatore di oggetto.               |
| [**\_inizializzazione del provider PFN Crypt \_ Object \_ Locator \_ \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize)            | Inizializza il provider.                               |



 

 

 
