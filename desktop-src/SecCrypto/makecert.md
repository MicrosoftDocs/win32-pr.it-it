---
description: Crea un certificato X.509, firmato dalla chiave radice di test o da un'altra chiave specificata, che associa il nome alla parte pubblica della coppia di chiavi. Il certificato viene salvato in un file, in un archivio certificati di sistema o in entrambi.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: Makecert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff9fb79b5db5a6a71eee981166742b4e1680184
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471927"
---
# <a name="makecert"></a>Makecert

> [!Note]  
> MakeCert è deprecato. Per creare certificati autofirmati, usare il cmdlet di PowerShell [New-SelfSignedCertificate.](/powershell/module/pki/new-selfsignedcertificate)

 

Lo strumento MakeCert crea un certificato [*X.509,*](../secgloss/x-gly.md) firmato dalla chiave radice di test o da un'altra chiave specificata, che associa il nome alla parte pubblica della coppia di chiavi. Il certificato viene salvato in un file, in un archivio certificati di sistema o in entrambi. Lo strumento viene installato nella \\ cartella Bin del percorso di installazione di Microsoft Windows Software Development Kit (SDK).

Lo strumento MakeCert usa la sintassi di comando seguente:

**MakeCert** \[ *Opzioni di base* \| *ExtendedOptions* \] *OutputFile*

*OutputFile* è il nome del file in cui verrà scritto il certificato. È possibile omettere *OutputFile* se il certificato non deve essere scritto in un file.

## <a name="options"></a>Opzioni

MakeCert include opzioni di base ed estese. Le opzioni di base sono quelle più frequentemente usate nella creazione di certificati. Le opzioni estese offrono una maggiore flessibilità.

Le opzioni per MakeCert sono suddivise anche in tre gruppi funzionali:

-   Opzioni di base specifiche della tecnologia dell'archivio certificati.
-   Opzioni estese specifiche della tecnologia SPC-file e della chiave privata.
-   Opzioni estese applicabili alla tecnologia SPC-file, chiave privata e archivio certificati.

Le opzioni fornite nelle tabelle seguenti possono essere usate solo con Internet Explorer 4.0 o versione successiva.




| Opzione di base | Descrizione | 
|--------------|-------------|
| <strong>-a</strong> <strong></strong> <em>Algoritmo</em> | <a href="/windows/desktop/SecGloss/h-gly"><em>Algoritmo</em></a> hash. Deve essere impostato su <strong>SHA-1</strong> o <strong>MD5</strong> (impostazione predefinita). Per informazioni su MD5, vedere <a href="/windows/desktop/SecGloss/m-gly"><em>MD5.</em></a> | 
| <strong>-b</strong> <strong></strong> <em>DateStart</em> | Data in cui il certificato diventa valido per la prima volta. Il valore predefinito è quando viene creato il certificato. Il formato di <em>DateStart</em> è mm/gg/aaaa. | 
| <strong>-cy</strong> <strong></strong> <em>Tipi di certificato</em> | Tipo di certificato. <em>CertificateTypes può</em> essere <strong>l'entità finale</strong> o l'autorità <strong>per</strong> l'autorità <a href="/windows/desktop/SecGloss/c-gly"><em>di certificazione</em></a>. | 
| <strong>-e</strong> <strong></strong> <em>DateEnd</em> | Data di fine del periodo di validità. Il valore predefinito è l'anno 2039. | 
| <strong>-eku</strong> <strong></strong> <em>OID1</em><strong>,</strong><em>OID2</em> ... | Inserisce nel certificato un elenco di uno o più identificatori OID <a href="/windows/desktop/SecGloss/e-gly"><em>(Key Usage</em></a><a href="/windows/desktop/SecGloss/o-gly"><em>Object</em></a> Identifier) delimitati da virgole e migliorati. Ad esempio, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserisce l'OID di autenticazione client. Per le definizioni degli OID consentiti, vedere il file Wincrypt.h in CryptoAPI 2.0. | 
| <strong>-h</strong> <strong></strong> <em>NumChildren</em> | Altezza massima dell'albero sotto questo certificato. | 
| <strong>-l</strong> <strong></strong> <em>Collegamento criteri</em> | Collegamento alle informazioni sui criteri dell'agenzia SPC (ad esempio, un URL). | 
| <strong>-m</strong> <strong></strong> <em>nMonths</em> | Durata del periodo di validità. | 
| <strong>-n</strong><strong>"</strong><em>Nome</em><strong>"</strong> | Nome del certificato dell'editore. Questo nome deve essere conforme allo standard <a href="/windows/desktop/SecGloss/x-gly"><em>X.500.</em></a> Il metodo più semplice è usare il formato "CN=<em>MyName".</em> Ad esempio: <strong>-n "CN=Test"</strong>. | 
| <strong>-nscp</strong> | È necessario includere l'estensione di autenticazione client Netscape. | 
| <strong>-pe</strong> | Contrassegna la chiave privata come esportabile. | 
| <strong>-r</strong> | Crea un certificato autofirmato. | 
| <strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em> | Nome file del certificato con la chiave pubblica del soggetto esistente da usare. | 
| <strong>-sk</strong> <strong></strong> <em>Chiave oggetto</em> | Posizione del contenitore di chiavi dell'oggetto che contiene la <a href="/windows/desktop/SecGloss/p-gly"><em>chiave privata</em></a>. Se non esiste alcun contenitore di chiavi, ne viene creato uno. Se non si <strong>usa l'opzione -sk</strong> o <strong>-sv,</strong> per impostazione predefinita viene creato e usato un contenitore di chiavi predefinito. | 
| <strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em> | Specifica della chiave del soggetto. <em>SubjectKeySpec</em> deve essere uno dei tre valori possibili:<br /><ul><li><strong>Firma</strong> (AT_SIGNATURE specifica della chiave)</li><li><strong>Exchange</strong> (specifica AT_KEYEXCHANGE chiave)</li><li>Numero intero, ad esempio <strong>3</strong></li></ul>Per altre informazioni, vedere la nota che segue questa tabella.<br /> | 
| <strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em> | Provider CryptoAPI per l'oggetto. Il valore predefinito è il provider dell'utente. Per informazioni sui provider CryptoAPI, vedere la documentazione CryptoAPI 2.0. | 
| <strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em> | Percorso del Registro di sistema dell'archivio certificati del soggetto. <em>SubjectCertStoreLocation</em> deve essere <strong>LocalMachine</strong> (chiave del Registro di sistema HKEY_LOCAL_MACHINE) o <strong>CurrentUser</strong> (chiave del Registro di HKEY_CURRENT_USER). <strong>CurrentUser</strong> è l'impostazione predefinita. | 
| <strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em> | Nome dell'archivio certificati del soggetto in cui verrà archiviato il certificato generato. | 
| <strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em> | Nome del file con estensione pvk dell'oggetto. Se non si <strong>usa l'opzione -sk</strong> o <strong>-sv,</strong> per impostazione predefinita viene creato e usato un contenitore di chiavi predefinito. | 
| <strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em> | Tipo di provider CryptoAPI per subject. Il valore predefinito <a href="/windows/desktop/SecGloss/p-gly"><em>è PROV_RSA_FULL</em></a>. Per informazioni sui tipi di provider CryptoAPI, vedere la documentazione CryptoAPI 2.0. | 
| <strong>-#</strong><strong></strong><em>Serialnumber</em> | Numero di serie del certificato. Il valore massimo è 2^31. Il valore predefinito è un valore generato dallo strumento che è garantito come univoco. | 
| <strong>-$</strong><strong></strong><em>CertificateAuthority</em> | Tipo di <a href="/windows/desktop/SecGloss/c-gly"><em>autorità di certificazione</em></a>. <em>CertificateAuthority</em> deve essere impostato su <strong>commerciale</strong> (per i certificati che devono essere usati da editori di software commerciali) o su singolo <strong>(per</strong> i certificati che devono essere usati da singoli editori di software). | 
| <strong>-?</strong> | Visualizza le opzioni di base. | 
| <strong>-!</strong> | Visualizza le opzioni estese. | 




 

> [!Note]  
> Se l'opzione **-sky** key specification viene usata in Internet Explorer versione 4.0 o successiva, la specifica deve corrispondere alla specifica della chiave indicata dal [*file*](../secgloss/p-gly.md) di chiave privata o dal contenitore di [*chiavi private*](../secgloss/k-gly.md). Se non si usa l'opzione di specifica della chiave, verrà usata la specifica della chiave indicata dal file di chiave privata o dal contenitore di chiavi private. Se nel contenitore di chiavi è presente più di una specifica di chiave, MakeCert tenterà prima di tutto di usare la specifica della chiave AT \_ SIGNATURE. Se l'operazione non riesce, MakeCert tenterà di usare AT \_ KEYEXCHANGE. Poiché la maggior parte degli utenti ha una chiave AT SIGNATURE o una chiave AT KEYEXCHANGE, questa opzione non deve essere usata \_ nella maggior parte dei \_ casi.

 

Le opzioni seguenti sono disponibili solo per [*i file SPC (Software Publisher Certificate)*](../secgloss/s-gly.md) e la tecnologia della chiave privata.




| Opzione SPC e chiave privata | Descrizione | 
|----------------------------|-------------|
| <strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em> | Percorso del certificato dell'autorità emittente. | 
| <strong>-ik</strong> <strong></strong> <em>IssuerKey</em> | Percorso del contenitore di chiavi dell'autorità emittente. Il valore predefinito è la chiave radice di test. | 
| <strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em> | Specifica della chiave dell'autorità emittente, che deve essere uno dei tre valori possibili:<br /><ul><li><strong>Firma</strong> (AT_SIGNATURE specifica della chiave)</li><li><strong>Exchange</strong> (AT_KEYEXCHANGE della chiave)</li><li>Intero, ad esempio <strong>3</strong></li></ul>Per altre informazioni, vedere la nota che segue questa tabella.<br /> | 
| <strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em> | Provider CryptoAPI per l'autorità di emittente. Il valore predefinito è il provider dell'utente. Per informazioni sui provider CryptoAPI, vedere la documentazione CryptoAPI 2.0 cryptoapi. | 
| <strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em> | File di chiave privata dell'autorità emittente. Il valore predefinito è la radice di test. | 
| <strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em> | Tipo di provider CryptoAPI per l'autorità di emittente. Il valore predefinito è <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Per informazioni sui tipi di provider CryptoAPI, vedere la documentazione CryptoAPI 2.0. | 




 

> [!Note]  
> Se l'opzione **-iky** key specification viene usata in Internet Explorer 4.0 o versioni successive, la specifica deve corrispondere alla specifica della chiave indicata dal [*file*](../secgloss/p-gly.md) di chiave privata o dal contenitore [*di chiavi private*](../secgloss/k-gly.md). Se l'opzione di specifica della chiave non viene usata, verrà usata la specifica della chiave indicata dal file di chiave privata o dal contenitore di chiavi private. Se nel contenitore di chiavi è presente più di una specifica di chiave, MakeCert tenterà prima di tutto di usare la specifica della chiave AT \_ SIGNATURE. Se l'operazione non riesce, MakeCert tenterà di usare AT \_ KEYEXCHANGE. Poiché la maggior parte degli utenti ha una chiave AT SIGNATURE o una chiave AT KEYEXCHANGE, questa opzione non deve essere usata \_ nella maggior parte dei \_ casi.

 

Le opzioni seguenti sono solo per [*la tecnologia dell'archivio*](../secgloss/c-gly.md) certificati.



| Opzione archivio certificati          | Descrizione                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-ic** *IssuerCertFile*          | File che contiene il certificato dell'autorità emittente. MakeCert cerca nell'archivio certificati un certificato con una corrispondenza esatta.                                                                                                                                                                                                        |
| **-in** *IssuerNameString*        | Nome comune del certificato dell'autorità emittente. MakeCert cerca nell'archivio certificati un certificato il cui nome comune include *IssuerNameString*.                                                                                                                                                                                  |
| **-ir** *IssuerCertStoreLocation* | Percorso del Registro di sistema dell'archivio certificati dell'autorità di certificazione. *IssuerCertStoreLocation* deve essere **LocalMachine** (chiave del Registro di sistema HKEY LOCAL MACHINE) o CurrentUser (chiave del Registro di sistema \_ \_ HKEY CURRENT  \_ \_ USER). **CurrentUser** è l'impostazione predefinita.                                                                                                |
| **-is** *IssuerCertStoreName*     | Archivio certificati dell'autorità di certificazione che include il certificato dell'autorità di certificazione e le informazioni sulla chiave privata associata. Se nell'archivio sono presenti più certificati, l'utente deve identificarlo in modo univoco usando l'opzione **-ic** **o -in.** Se il certificato nell'archivio certificati non è identificato in modo univoco, MakeCert avrà esito negativo. |



 

 

 
