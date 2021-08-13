---
description: Crea un certificato X.509, firmato dalla chiave radice di test o da un'altra chiave specificata, che associa il nome alla parte pubblica della coppia di chiavi. Il certificato viene salvato in un file, in un archivio certificati di sistema o in entrambi.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: Makecert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd9f15f942fb6dd7c4c831cb33552b6f59ec2cd6cf9cac9654386d6adc27649
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425741"
---
# <a name="makecert"></a>Makecert

> [!Note]  
> MakeCert è deprecato. Per creare certificati autofirmati, usare il cmdlet di PowerShell [New-SelfSignedCertificate.](/powershell/module/pki/new-selfsignedcertificate)

 

Lo strumento MakeCert crea un certificato [*X.509,*](../secgloss/x-gly.md) firmato dalla chiave radice di test o da un'altra chiave specificata, che associa il nome alla parte pubblica della coppia di chiavi. Il certificato viene salvato in un file, in un archivio certificati di sistema o in entrambi. Lo strumento viene installato nella cartella Bin del percorso di \\ installazione di Microsoft Windows Software Development Kit (SDK).

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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opzione di base</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>-a</strong> <strong></strong> <em>Algoritmo</em></td>
<td><a href="/windows/desktop/SecGloss/h-gly"><em>Algoritmo</em></a> hash. Deve essere impostato su <strong>SHA-1</strong> o <strong>MD5</strong> (impostazione predefinita). Per informazioni su MD5, vedere <a href="/windows/desktop/SecGloss/m-gly"><em>MD5.</em></a></td>
</tr>
<tr class="even">
<td><strong>-b</strong> <strong></strong> <em>DateStart</em></td>
<td>Data in cui il certificato diventa valido per la prima volta. Il valore predefinito è quando viene creato il certificato. Il formato di <em>DateStart</em> è mm/gg/aaaa.</td>
</tr>
<tr class="odd">
<td><strong>-cy</strong> <strong></strong> <em>Tipi di certificato</em></td>
<td>Tipo di certificato. <em>CertificateTypes può</em> essere <strong>l'entità finale</strong> o l'autorità <strong>per</strong> l'autorità <a href="/windows/desktop/SecGloss/c-gly"><em>di certificazione</em></a>.</td>
</tr>
<tr class="even">
<td><strong>-e</strong> <strong></strong> <em>DateEnd</em></td>
<td>Data di fine del periodo di validità. Il valore predefinito è l'anno 2039.</td>
</tr>
<tr class="odd">
<td><strong>-eku</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> ...</td>
<td>Inserisce nel certificato un elenco di uno o più identificatori OID <a href="/windows/desktop/SecGloss/e-gly"><em>(Key Usage</em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>Object</em></a> Identifier) delimitati da virgole e migliorati. Ad esempio, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserisce l'OID di autenticazione client. Per le definizioni degli OID consentiti, vedere il file Wincrypt.h in CryptoAPI 2.0.</td>
</tr>
<tr class="even">
<td><strong>-h</strong> <strong></strong> <em>NumChildren</em></td>
<td>Altezza massima dell'albero sotto questo certificato.</td>
</tr>
<tr class="odd">
<td><strong>-l</strong> <strong></strong> <em>Collegamento criteri</em></td>
<td>Collegamento alle informazioni sui criteri dell'agenzia SPC (ad esempio, un URL).</td>
</tr>
<tr class="even">
<td><strong>-m</strong> <strong></strong> <em>nMonths</em></td>
<td>Durata del periodo di validità.</td>
</tr>
<tr class="odd">
<td><strong>-n</strong> <strong>&quot;</strong> <em>Nome</em><strong>&quot;</strong></td>
<td>Nome del certificato dell'editore. Questo nome deve essere conforme allo standard <a href="/windows/desktop/SecGloss/x-gly"><em>X.500.</em></a> Il metodo più semplice è usare il &quot; formato CN=<em>MyName.</em> &quot; Ad esempio: <strong>-n &quot; CN=Test &quot; </strong>.</td>
</tr>
<tr class="even">
<td><strong>-nscp</strong></td>
<td>È necessario includere l'estensione di autenticazione client Netscape.</td>
</tr>
<tr class="odd">
<td><strong>-pe</strong></td>
<td>Contrassegna la chiave privata come esportabile.</td>
</tr>
<tr class="even">
<td><strong>-r</strong></td>
<td>Crea un certificato autofirmato.</td>
</tr>
<tr class="odd">
<td><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></td>
<td>Nome file del certificato con la chiave pubblica del soggetto esistente da usare.</td>
</tr>
<tr class="even">
<td><strong>-sk</strong> <strong></strong> <em>Chiave oggetto</em></td>
<td>Posizione del contenitore di chiavi dell'oggetto che contiene la <a href="/windows/desktop/SecGloss/p-gly"><em>chiave privata</em></a>. Se non esiste alcun contenitore di chiavi, ne viene creato uno. Se non si <strong>usa l'opzione -sk</strong> o <strong>-sv,</strong> per impostazione predefinita viene creato e usato un contenitore di chiavi predefinito.</td>
</tr>
<tr class="odd">
<td><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></td>
<td>Specifica della chiave del soggetto. <em>SubjectKeySpec</em> deve essere uno dei tre valori possibili:<br/>
<ul>
<li><strong>Firma</strong> (AT_SIGNATURE specifica della chiave)</li>
<li><strong>Exchange</strong> (AT_KEYEXCHANGE specifica della chiave)</li>
<li>Numero intero, ad esempio <strong>3</strong></li>
</ul>
Per altre informazioni, vedere la nota che segue questa tabella.<br/></td>
</tr>
<tr class="even">
<td><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></td>
<td>Provider CryptoAPI per l'oggetto. Il valore predefinito è il provider dell'utente. Per informazioni sui provider CryptoAPI, vedere la documentazione CryptoAPI 2.0.</td>
</tr>
<tr class="odd">
<td><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></td>
<td>Percorso del Registro di sistema dell'archivio certificati del soggetto. <em>SubjectCertStoreLocation</em> deve essere <strong>LocalMachine</strong> (chiave del Registro di sistema HKEY_LOCAL_MACHINE) o <strong>CurrentUser</strong> (chiave del Registro di sistema HKEY_CURRENT_USER). <strong>CurrentUser</strong> è l'impostazione predefinita.</td>
</tr>
<tr class="even">
<td><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></td>
<td>Nome dell'archivio certificati del soggetto in cui verrà archiviato il certificato generato.</td>
</tr>
<tr class="odd">
<td><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></td>
<td>Nome del file con estensione pvk dell'oggetto. Se non si <strong>usa l'opzione -sk</strong> o <strong>-sv,</strong> per impostazione predefinita viene creato e usato un contenitore di chiavi predefinito.</td>
</tr>
<tr class="even">
<td><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></td>
<td>Tipo di provider CryptoAPI per subject. Il valore predefinito <a href="/windows/desktop/SecGloss/p-gly"><em>è PROV_RSA_FULL</em></a>. Per informazioni sui tipi di provider CryptoAPI, vedere la documentazione CryptoAPI 2.0 cryptoapi.</td>
</tr>
<tr class="odd">
<td><strong>-#</strong><strong></strong> <em>SerialNumber</em></td>
<td>Numero di serie del certificato. Il valore massimo è 2^31. Il valore predefinito è un valore generato dallo strumento che è garantito come univoco.</td>
</tr>
<tr class="even">
<td><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></td>
<td>Tipo di <a href="/windows/desktop/SecGloss/c-gly"><em>autorità di certificazione</em></a>. <em>CertificateAuthority</em> deve essere impostato su <strong>commerciale</strong> (per i certificati che devono essere usati da editori di software commerciali) o su singolo <strong>(per</strong> i certificati che devono essere usati da singoli editori di software).</td>
</tr>
<tr class="odd">
<td><strong>-?</strong></td>
<td>Visualizza le opzioni di base.</td>
</tr>
<tr class="even">
<td><strong>-!</strong></td>
<td>Visualizza le opzioni estese.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Se l'opzione **-sky** key specification viene usata in Internet Explorer versione 4.0 o successiva, la specifica deve corrispondere alla specifica della chiave indicata dal [*file*](../secgloss/p-gly.md) di chiave privata o dal contenitore di [*chiavi private*](../secgloss/k-gly.md). Se non si usa l'opzione di specifica della chiave, verrà usata la specifica della chiave indicata dal file di chiave privata o dal contenitore di chiavi private. Se nel contenitore di chiavi è presente più di una specifica di chiave, MakeCert tenterà prima di tutto di usare la specifica della chiave AT \_ SIGNATURE. Se l'operazione non riesce, MakeCert tenterà di usare AT \_ KEYEXCHANGE. Poiché la maggior parte degli utenti ha una chiave AT SIGNATURE o una chiave AT KEYEXCHANGE, questa opzione non deve essere usata \_ nella maggior parte dei \_ casi.

 

Le opzioni seguenti sono disponibili solo per [*i file SPC (Software Publisher Certificate)*](../secgloss/s-gly.md) e la tecnologia della chiave privata.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opzione SPC e chiave privata</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></td>
<td>Percorso del certificato dell'autorità emittente.</td>
</tr>
<tr class="even">
<td><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></td>
<td>Percorso del contenitore di chiavi dell'autorità emittente. Il valore predefinito è la chiave radice di test.</td>
</tr>
<tr class="odd">
<td><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></td>
<td>Specifica della chiave dell'autorità emittente, che deve essere uno dei tre valori possibili:<br/>
<ul>
<li><strong>Firma</strong> (AT_SIGNATURE specifica della chiave)</li>
<li><strong>Exchange</strong> (AT_KEYEXCHANGE della chiave)</li>
<li>Intero, ad esempio <strong>3</strong></li>
</ul>
Per altre informazioni, vedere la nota che segue questa tabella.<br/></td>
</tr>
<tr class="even">
<td><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></td>
<td>Provider CryptoAPI per l'autorità di emittente. Il valore predefinito è il provider dell'utente. Per informazioni sui provider CryptoAPI, vedere la documentazione CryptoAPI 2.0 di crittografia.</td>
</tr>
<tr class="odd">
<td><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></td>
<td>File di chiave privata dell'autorità emittente. Il valore predefinito è la radice di test.</td>
</tr>
<tr class="even">
<td><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></td>
<td>Tipo di provider CryptoAPI per l'autorità di emittente. Il valore predefinito è <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Per informazioni sui tipi di provider CryptoAPI, vedere la documentazione CryptoAPI 2.0.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Se l'opzione **-iky** key specification viene usata in Internet Explorer 4.0 o versioni successive, la specifica deve corrispondere alla specifica della chiave indicata dal [*file*](../secgloss/p-gly.md) di chiave privata o dal contenitore [*di chiavi private*](../secgloss/k-gly.md). Se l'opzione di specifica della chiave non viene usata, verrà usata la specifica della chiave indicata dal file di chiave privata o dal contenitore di chiavi private. Se nel contenitore di chiavi è presente più di una specifica di chiave, MakeCert tenterà prima di tutto di usare la specifica della chiave AT \_ SIGNATURE. Se l'operazione non riesce, MakeCert tenterà di usare AT \_ KEYEXCHANGE. Poiché la maggior parte degli utenti ha una chiave AT SIGNATURE o una chiave AT KEYEXCHANGE, questa opzione non deve essere usata \_ nella maggior parte dei \_ casi.

 

Le opzioni seguenti sono solo per [*la tecnologia dell'archivio*](../secgloss/c-gly.md) certificati.



| Opzione archivio certificati          | Descrizione                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-ic** *IssuerCertFile*          | File che contiene il certificato dell'autorità emittente. MakeCert cerca nell'archivio certificati un certificato con una corrispondenza esatta.                                                                                                                                                                                                        |
| **-in** *IssuerNameString*        | Nome comune del certificato dell'autorità emittente. MakeCert cerca nell'archivio certificati un certificato il cui nome comune include *IssuerNameString*.                                                                                                                                                                                  |
| **-ir** *IssuerCertStoreLocation* | Percorso del Registro di sistema dell'archivio certificati dell'autorità di certificazione. *IssuerCertStoreLocation* deve essere **LocalMachine** (chiave del Registro di sistema HKEY LOCAL MACHINE) o CurrentUser (chiave del Registro di sistema \_ \_ HKEY CURRENT  \_ \_ USER). **CurrentUser** è l'impostazione predefinita.                                                                                                |
| **-is** *IssuerCertStoreName*     | Archivio certificati dell'autorità di certificazione che include il certificato dell'autorità di certificazione e le informazioni sulla chiave privata associata. Se nell'archivio sono presenti più certificati, l'utente deve identificarlo in modo univoco usando l'opzione **-ic** **o -in.** Se il certificato nell'archivio certificati non è identificato in modo univoco, MakeCert avrà esito negativo. |



 

 

 
