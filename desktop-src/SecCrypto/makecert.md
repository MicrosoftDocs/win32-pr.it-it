---
description: Crea un certificato X. 509, firmato dalla chiave radice del test o da un'altra chiave specificata, che associa il nome alla parte pubblica della coppia di chiavi. Il certificato viene salvato in un file, in un archivio certificati di sistema o in entrambi.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980ba379688f2dc61c44b06d66ed5255e5b2e988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307692"
---
# <a name="makecert"></a>MakeCert

> [!Note]  
> MakeCert è deprecato. Per creare certificati autofirmati, usare il cmdlet di PowerShell [New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate).

 

Lo strumento MakeCert crea un certificato [*X. 509*](../secgloss/x-gly.md) , firmato dalla chiave radice del test o da un'altra chiave specificata, che associa il nome alla parte pubblica della coppia di chiavi. Il certificato viene salvato in un file, in un archivio certificati di sistema o in entrambi. Lo strumento viene installato nella \\ cartella bin del percorso di installazione di Microsoft Windows Software Development Kit (SDK).

Lo strumento MakeCert usa la sintassi del comando seguente:

**Makecert** \[ *BasicOptions* \| *ExtendedOptions* \] *Outputfile*

*Outputfile* è il nome del file in cui verrà scritto il certificato. È possibile omettere *outputfile* se il certificato non deve essere scritto in un file.

## <a name="options"></a>Opzioni

MakeCert include opzioni di base ed estese. Le opzioni di base sono quelle più frequentemente usate nella creazione di certificati. Le opzioni estese offrono una maggiore flessibilità.

Le opzioni per MakeCert sono divise anche in tre gruppi funzionali:

-   Opzioni di base specifiche solo per la tecnologia dell'archivio certificati.
-   Opzioni estese specifiche solo per la tecnologia del file SPC e della chiave privata.
-   Opzioni estese applicabili alla tecnologia del file SPC, della chiave privata e dell'archivio certificati.

Le opzioni fornite nelle tabelle seguenti possono essere utilizzate solo con Internet Explorer 4,0 o versione successiva.



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
<td><strong>-a</strong> <strong></strong> <em>Algoritmo</em> di</td>
<td>Algoritmo <a href="/windows/desktop/SecGloss/h-gly"><em>hash</em></a> . Deve essere impostato su <strong>SHA-1</strong> o <strong>MD5</strong> (impostazione predefinita). Per informazioni su MD5, vedere <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</td>
</tr>
<tr class="even">
<td><strong>-b</strong> <strong></strong> <em>DateStart</em></td>
<td>Data in cui il certificato diventa prima valido. Il valore predefinito è quando viene creato il certificato. Il formato di <em>dateStart</em> è mm/gg/aaaa.</td>
</tr>
<tr class="odd">
<td><strong>-CY</strong> <strong></strong> <em>CertificateTypes</em></td>
<td>Tipo di certificato. <em>CertificateTypes</em> può essere <strong>end</strong> per l'entità finale o l' <strong>autorità</strong> per l' <a href="/windows/desktop/SecGloss/c-gly"><em>autorità di certificazione</em></a>.</td>
</tr>
<tr class="even">
<td><strong>-e</strong> <strong></strong> <em>DateEnd</em></td>
<td>Data di fine del periodo di validità. Il valore predefinito è l'anno 2039.</td>
</tr>
<tr class="odd">
<td><strong>-EKU</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> ...</td>
<td>Inserisce nel certificato un elenco di uno o più <a href="/windows/desktop/SecGloss/e-gly"><em></em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>identificatori di oggetto</em></a> con valori delimitati da virgole (OID). Ad esempio, <strong>-EKU 1.3.6.1.5.5.7.3.2</strong> inserisce l'OID di autenticazione client. Per le definizioni dei OID consentiti, vedere il file Wincrypt. h in CryptoAPI 2.0.</td>
</tr>
<tr class="even">
<td><strong>-h</strong> <strong></strong> <em>NumChildren</em></td>
<td>Altezza massima dell'albero al di sotto del certificato.</td>
</tr>
<tr class="odd">
<td><strong>-l</strong> <strong></strong> <em>PolicyLink</em></td>
<td>Collegamento alle informazioni sui criteri dell'Agenzia SPC, ad esempio un URL.</td>
</tr>
<tr class="even">
<td><strong>-m</strong> <strong></strong> <em>nMonths</em></td>
<td>Durata del periodo di validità.</td>
</tr>
<tr class="odd">
<td><strong>-n</strong> <strong>&quot;</strong> <em>Nome</em><strong>&quot;</strong></td>
<td>Nome del certificato dell'autore. Questo nome deve essere conforme allo standard <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> . Il metodo più semplice consiste nell'usare il &quot; formato CN =<em>nome</em> &quot; . Ad esempio: <strong>-n &quot; CN = test &quot; </strong>.</td>
</tr>
<tr class="even">
<td><strong>-nscp</strong></td>
<td>È necessario includere l'estensione di autenticazione client Netscape.</td>
</tr>
<tr class="odd">
<td><strong>-PE</strong></td>
<td>Contrassegna la chiave privata come esportabile.</td>
</tr>
<tr class="even">
<td><strong>-r</strong></td>
<td>Crea un certificato autofirmato.</td>
</tr>
<tr class="odd">
<td><strong>-SC</strong> <strong></strong> <em>SubjectCertFile</em></td>
<td>Nome del file del certificato con la chiave pubblica del soggetto esistente da usare.</td>
</tr>
<tr class="even">
<td><strong>-SK</strong> <strong></strong> <em>SubjectKey</em></td>
<td>Posizione del contenitore di chiavi del soggetto che include la <a href="/windows/desktop/SecGloss/p-gly"><em>chiave privata</em></a>. Se non esiste alcun contenitore di chiavi, ne viene creato uno. Se non si usa l'opzione <strong>-SK</strong> o <strong>-SV</strong> , viene creato e usato per impostazione predefinita un contenitore di chiavi predefinito.</td>
</tr>
<tr class="odd">
<td><strong>-Sky</strong> <strong></strong> <em>SubjectKeySpec</em></td>
<td>Specifica della chiave dell'oggetto. <em>SubjectKeySpec</em> deve essere uno dei tre valori possibili:<br/>
<ul>
<li><strong>Firma</strong> (specifica chiave AT_SIGNATURE)</li>
<li><strong>Exchange</strong> (specifica chiave AT_KEYEXCHANGE)</li>
<li>Integer, ad esempio <strong>3</strong></li>
</ul>
Per ulteriori informazioni, vedere la nota che segue questa tabella.<br/></td>
</tr>
<tr class="even">
<td><strong>-SP</strong> <strong></strong> <em>SubjectProviderName</em></td>
<td>Provider CryptoAPI per l'oggetto. Il valore predefinito è il provider dell'utente. Per informazioni sui provider CryptoAPI, vedere la documentazione CryptoAPI 2.0.</td>
</tr>
<tr class="odd">
<td><strong>-Sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></td>
<td>Percorso del registro di sistema dell'archivio certificati dell'oggetto. <em>SubjectCertStoreLocation</em> deve essere <strong>LocalMachine</strong> (chiave del registro di sistema HKEY_LOCAL_MACHINE) o <strong>CurrentUser</strong> (chiave del registro di sistema HKEY_CURRENT_USER). <strong>CurrentUser</strong> è il valore predefinito.</td>
</tr>
<tr class="even">
<td><strong>-SS</strong> <strong></strong> <em>SubjectCertStoreName</em></td>
<td>Nome dell'archivio certificati dell'oggetto in cui verrà archiviato il certificato generato.</td>
</tr>
<tr class="odd">
<td><strong>-SV</strong> <strong></strong> <em>SubjectKeyFile</em></td>
<td>Nome del file con estensione PVK dell'oggetto. Se non si usa l'opzione <strong>-SK</strong> o <strong>-SV</strong> , viene creato e usato per impostazione predefinita un contenitore di chiavi predefinito.</td>
</tr>
<tr class="even">
<td><strong>-SY</strong> <strong></strong> <em>nSubjectProviderType</em></td>
<td>Tipo di provider CryptoAPI per subject. Il valore predefinito è <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Per informazioni sui tipi di provider CryptoAPI, vedere la documentazione CryptoAPI 2.0.</td>
</tr>
<tr class="odd">
<td><strong>-#</strong><strong></strong> <em>SerialNumber</em></td>
<td>Numero di serie del certificato. Il valore massimo è 2 ^ 31. Il valore predefinito è un valore generato dallo strumento che garantisce l'univocità.</td>
</tr>
<tr class="even">
<td><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></td>
<td>Tipo di <a href="/windows/desktop/SecGloss/c-gly"><em>autorità di certificazione</em></a>. <em>CertificateAuthority</em> deve essere impostato su <strong>Commercial</strong> (per i certificati utilizzati dagli editori di software commerciale) o su <strong>singoli</strong> (per i certificati che devono essere utilizzati da autori di software singoli).</td>
</tr>
<tr class="odd">
<td><strong>-?</strong></td>
<td>Consente di visualizzare le opzioni di base.</td>
</tr>
<tr class="even">
<td><strong>-!</strong></td>
<td>Consente di visualizzare le opzioni estese.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Se in Internet Explorer versione 4,0 o successiva viene utilizzata l'opzione di specifica della chiave **-Sky** , la specifica deve corrispondere alla specifica della chiave indicata dal file di [*chiave privata*](../secgloss/p-gly.md) o dal [*contenitore di chiavi*](../secgloss/k-gly.md)private. Se non si utilizza l'opzione relativa alla specifica della chiave, verrà utilizzata la specifica della chiave indicata dal file di chiave privata o dal contenitore di chiavi private. Se il contenitore di chiavi contiene più di una specifica chiave, MakeCert tenterà innanzitutto di usare la \_ specifica della chiave di firma. Se l'operazione ha esito negativo, MakeCert tenterà di utilizzare in caso di scambio delle corrispondenze \_ . Poiché la maggior parte degli utenti ha una chiave di \_ firma o una chiave di scambio delle chiavi \_ , questa opzione non deve essere utilizzata nella maggior parte dei casi.

 

Le opzioni seguenti sono destinate solo ai file del [*certificato di pubblicazione software*](../secgloss/s-gly.md) (SPC) e alla tecnologia di chiave privata.



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
<td><strong>-IC</strong> <strong></strong> <em>IssuerCertFile</em></td>
<td>Posizione del certificato dell'autorità emittente.</td>
</tr>
<tr class="even">
<td><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></td>
<td>Percorso del contenitore di chiavi dell'autorità emittente. Il valore predefinito è la chiave radice del test.</td>
</tr>
<tr class="odd">
<td><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></td>
<td>Specifica della chiave dell'autorità emittente, che deve essere uno dei tre valori possibili:<br/>
<ul>
<li><strong>Firma</strong> (specifica chiave AT_SIGNATURE)</li>
<li><strong>Exchange</strong> (specifica chiave AT_KEYEXCHANGE)</li>
<li>Integer, ad esempio <strong>3</strong></li>
</ul>
Per ulteriori informazioni, vedere la nota che segue questa tabella.<br/></td>
</tr>
<tr class="even">
<td><strong>-IP</strong> <strong></strong> <em>IssuerProviderName</em></td>
<td>Provider CryptoAPI per l'emittente. Il valore predefinito è il provider dell'utente. Per informazioni sui provider CryptoAPI, vedere la documentazione CryptoAPI 2.0.</td>
</tr>
<tr class="odd">
<td><strong>-IV</strong> <strong></strong> <em>IssuerKeyFile</em></td>
<td>File di chiave privata dell'autorità emittente. Il valore predefinito è la radice del test.</td>
</tr>
<tr class="even">
<td><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></td>
<td>Tipo di provider CryptoAPI per Issuer. Il valore predefinito è <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Per informazioni sui tipi di provider CryptoAPI, vedere la documentazione CryptoAPI 2.0.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Se si usa l'opzione di specifica della chiave **-iky** in Internet Explorer 4,0 o versione successiva, la specifica deve corrispondere alla specifica della chiave indicata dal file di [*chiave privata*](../secgloss/p-gly.md) o dal [*contenitore di chiavi*](../secgloss/k-gly.md)private. Se non si utilizza l'opzione relativa alla specifica della chiave, verrà utilizzata la specifica della chiave indicata dal file di chiave privata o dal contenitore di chiavi private. Se il contenitore di chiavi contiene più di una specifica chiave, MakeCert tenterà innanzitutto di usare la \_ specifica della chiave di firma. Se l'operazione ha esito negativo, MakeCert tenterà di utilizzare in caso di scambio delle corrispondenze \_ . Poiché la maggior parte degli utenti ha una chiave di \_ firma o una chiave di scambio delle chiavi \_ , questa opzione non deve essere utilizzata nella maggior parte dei casi.

 

Le opzioni seguenti sono destinate solo alla tecnologia dell' [*archivio certificati*](../secgloss/c-gly.md) .



| Opzione archivio certificati          | Descrizione                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-** *IssuerCertFile* IC          | File che contiene il certificato dell'autorità emittente. MakeCert effettuerà la ricerca nell'archivio certificati per un certificato con una corrispondenza esatta.                                                                                                                                                                                                        |
| **-in** *IssuerNameString*        | Nome comune del certificato dell'autorità emittente. MakeCert effettuerà la ricerca nell'archivio certificati per un certificato il cui nome comune include *IssuerNameString*.                                                                                                                                                                                  |
| **-** *IssuerCertStoreLocation* IR | Percorso del registro di sistema dell'archivio certificati dell'autorità emittente. *IssuerCertStoreLocation* deve essere **LocalMachine** (chiave del registro di sistema HKEY \_ Local \_ computer) o **CURRENTUSER** (chiave del registro di sistema HKEY \_ Current \_ User). **CurrentUser** è il valore predefinito.                                                                                                |
| **-è** *IssuerCertStoreName*     | Archivio certificati dell'autorità emittente che include il certificato dell'autorità emittente e le informazioni sulla chiave privata associata. Se è presente più di un certificato nell'archivio, è necessario che l'utente lo identifichi in modo univoco utilizzando l'opzione **-IC** o **-in** . Se il certificato nell'archivio certificati non è identificato in modo univoco, MakeCert avrà esito negativo. |



 

 

 
