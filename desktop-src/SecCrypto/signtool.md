---
title: SignTool
description: SignTool è uno strumento da riga di comando che firma digitalmente i file, verifica le firme nei file e i file timestamp.
ms.assetid: aa59cb35-5fba-4ce8-97ea-fc767c83f88e
ms.topic: article
ms.date: 10/12/2020
ms.openlocfilehash: f7105e81b958e463612a5065003ed04c24b913f87f52d8d72bb7a708917ebbed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897956"
---
# <a name="signtool"></a>SignTool

SignTool è uno strumento da riga di comando che firma digitalmente i file, verifica le firme nei file e i file timestamp. Per informazioni sui motivi per cui la firma dei file è importante, vedere [Introduzione alla firma del codice.](cryptography-tools.md) Lo strumento viene installato nella cartella Bin del percorso di installazione di Microsoft Windows Software Development Kit (SDK), ad esempio \\ C:\Programmi (x86)\Windows Kits\10\bin\10.0.19041.0\x64\signtool.exe).

SignTool è disponibile come parte di Windows SDK, che è possibile scaricare da <https://developer.microsoft.com/windows/downloads/windows-10-sdk/> .

> [!Note]  
> Le build Windows 10 SDK, Windows 10 HLK, Windows 10 WDK e Windows 10 ADK **20236** e successive richiederanno ora di specificare l'algoritmo digest. Il comando SignTool sign richiede che le opzioni /fd e /td siano specificate rispettivamente durante la firma e `file digest algorithm` `timestamp digest algorithm` il timestamp. Verrà generato un avviso (codice di errore 0, inizialmente) se /fd non viene specificato durante la firma e se /td non viene specificato durante il timestamp. Nelle versioni successive di SignTool, l'avviso diventerà un errore. SHA256 è consigliato e considerato più sicuro di SHA1 dal settore.  


## <a name="syntax"></a>Sintassi  
  
```console  
signtool [command] [options] [file_name | ...]  
```  

## <a name="parameters"></a>Parametri  
  
|Argomento|Descrizione|  
|----|----|  
|`command`|Uno dei quattro comandi (`catdb`, `sign`, `Timestamp` o `Verify`) che specifica l'operazione da eseguire su un file. Per una descrizione di ogni comando, vedere la tabella successiva.|  
|`options`|Opzione che modifica un comando. Oltre alle opzioni globali `/q` e `/v`, ciascun comando supporta un set univoco di opzioni.|  
|`file_name`|Il percorso di un file da firmare.| 


I comandi seguenti sono supportati da SignTool.

|Comando|Descrizione|  
|----|----|  
|`Catdb`|Aggiunge o rimuove un file di catalogo da un database di cataloghi. I database dei cataloghi vengono usati per la ricerca automatica di file di catalogo e sono identificati dal GUID. Per un elenco delle opzioni supportate dal comando `catdb`, vedere [Opzioni del comando catdb](/dotnet/framework/tools/signtool-exe#catdb-command-options).|  
|`Sign`|Firma digitalmente i file. Le firme digitali impediscono la manomissione dei file e consentono agli utenti di verificare il firmatario in base a un certificato di firma. Per un elenco delle opzioni supportate dal comando `sign`, vedere [Opzioni del comando sign](/dotnet/framework/tools/signtool-exe#sign-command-options).|  
|`Timestamp`|Aggiunge un timestamp ai file. Per un elenco delle opzioni supportate dal comando `TimeStamp`, vedere [Opzioni del comando TimeStamp](/dotnet/framework/tools/signtool-exe#timestamp-command-options).|  
|`Verify`|Verifica la firma digitale dei file determinando se il certificato di firma è stato emesso da un'autorità attendibile, se è stato revocato e, facoltativamente, se è valido per criteri specifici. Per un elenco delle opzioni supportate dal comando `Verify`, vedere [Opzioni del comando Verify](/dotnet/framework/tools/signtool-exe#verify-command-options).|

 Le opzioni riportate di seguito si applicano a tutti i comandi dello strumento Firma.  
  
|Opzione globale|Descrizione|  
|----|----|  
|**/q**|Non visualizza alcun output se il comando viene eseguito correttamente e visualizza un output minimo se il comando ha esito negativo.|  
|**/v**|Visualizza un output dettagliato indipendentemente dall'esito del comando e visualizza messaggi di avviso.|  
|**/debug**|Visualizza le informazioni di debug.|  

 
## <a name="catdb-command-options"></a>Opzioni del comando Catdb  

 Nella tabella seguente vengono illustrate le opzioni utilizzabili con il comando `Catdb`.

| Opzione catdb | Descrizione |
|----|----| 
| **/d** | Specifica che il database del catalogo predefinito deve essere aggiornato. Se non si usa **né l'opzione /d** né **/g** , SignTool aggiorna il componente di sistema e il database dei driver. |
| **/g** *GUID* | Specifica che il database del catalogo identificato dal GUID deve essere aggiornato.|
| **/r** | Rimuove il catalogo specificato dal database del catalogo. Se questa opzione non viene specificata, SignTool aggiungerà il catalogo specificato al database del catalogo.|
| **/u** | Specifica che viene generato automaticamente un nome univoco per i file di catalogo aggiunti. Se necessario, i file di catalogo vengono rinominati per evitare conflitti con i nomi dei file di catalogo esistenti. Se questa opzione non viene specificata, SignTool sovrascrive qualsiasi catalogo esistente con lo stesso nome del catalogo da aggiungere.|

> [!Note]  
> I database del catalogo vengono usati per la ricerca automatica dei file di catalogo.


## <a name="sign-command-options"></a>Opzioni del comando Sign  

 Nella tabella seguente vengono illustrate le opzioni utilizzabili con il comando `sign`.  
  
|Opzioni del comando sign|Descrizione|  
|----|----| 
|`/a`|Seleziona automaticamente il miglior certificato di firma. Verranno trovati tutti i certificati validi che soddisfano tutte le condizioni specificate e verrà selezionato quello valido per il periodo più lungo. Se questa opzione non è presente, è prevista la presenza di un solo certificato di firma valido.|  
|`/ac`  *File*|Aggiunge un altro certificato dal *file* al blocco di firme.|  
|`/as`|Aggiunge questa firma. Se non è presente alcuna firma primaria, questa firma viene impostata come primaria.|  
|`/c`  *CertTemplateName*|Specifica un'estensione Microsoft, Certificate Template Name, per il certificato di firma.|  
|`/csp`  *CSPName*|Specifica il provider del servizio di crittografia (CSP) che contiene il contenitore di chiavi private.|  
|`/d`  *Desc*|Specifica una descrizione del contenuto firmato.|  
|`/dg`  *Percorso*|Genera il digest da firmare e i file PKCS7 non firmati. Il digest di output e i file PKCS7 saranno: *Path\FileName.dig* e *Path\FileName.p7u*. Per eseguire l'output di un file XML aggiuntivo, <strong>vedere /dxml</strong>.|  
|`/di`  *Percorso*|Crea la firma mediante l'inserimento del digest firmato nel file PKCS7 non firmato. I file digest e PKCS7 non firmati di input devono essere: *Path\FileName.dig.signed* e *Path\FileName.p7u*.|  
|`/dlib`  *DLL*|Specifica la DLL che implementa la <code>AuthenticodeDigestSign</code> funzione con cui firmare il digest. Questa opzione equivale a usare <strong>SignTool</strong> separatamente con le opzioni <strong>/dg</strong>, <strong>/ds</strong>e <strong>/di</strong> , ad eccezione del fatto che questa opzione richiama tutti e tre come un'unica operazione atomica.|  
|`/dmdf`  *Filename*|Se usato con <strong>l'opzione /dg,</strong> passa il contenuto del file alla <code>AuthenticodeDigestSign</code> funzione senza modifiche.|  
|`/ds`  |Firma solo il digest. Il file di input deve essere il digest generato <strong>dall'opzione /dg.</strong> Il file di output sarà: *File.signed.*|  
|`/du`  *URL*|Specifica un URL (Uniform Resource Locator) per la descrizione espansa del contenuto firmato.|  
|`/dxml`  |Se usato con <strong>l'opzione /dg,</strong> genera un file XML. Il file di output sarà: *Path\FileName.dig.xml*.|  
|`/f`  *SignCertFile*|Specifica il certificato di firma in un file. Se il file è nel formato PFX (Personal Information Exchange) ed è protetto da una password, usare l'opzione `/p` per specificare la password. Se il file non contiene chiavi private, usare le opzioni `/csp` e `/kc` per specificare il CSP e il nome del contenitore delle chiavi private.|  
|`/fd`*alg*|Specifica l'algoritmo digest file da usare per creare le firme del file. </br> **Nota:** Se durante la firma non viene specificata <strong>l'opzione /fd,</strong> viene generato un avviso. L'alg predefinito è SHA1, ma è consigliato SHA256.|
|`/fd`  *certHash*|Se si specifica la stringa certHash, per impostazione predefinita verrà usato l'algoritmo usato nel certificato di firma. </br> **Nota:** Disponibile solo nelle build Windows 10 kit 20236 e successive.|  
|`/i`  *IssuerName*|Specifica il nome dell'emittente del certificato di firma. Questo valore può essere una sottostringa dell'intero nome dell'emittente.|  
|`/kc`  *PrivKeyContainerName*|Specifica il nome del contenitore delle chiavi private.|  
|`/n`  *SubjectName*|Specifica il nome del soggetto del certificato di firma. Questo valore può essere una sottostringa dell'intero nome del soggetto.|  
|`/nph`|Se supportato, sopprime gli hash delle pagine per i file eseguibili. Il valore predefinito è determinato dalla variabile di ambiente SIGNTOOL_PAGE_HASHES e dalla versione di wintrust.dll. Questa opzione viene ignorata per i file non PE.|  
|`/p`  *Password*|Specifica la password da usare all'apertura di un file PFX (usare l'opzione `/f` per specificare un file PFX).|  
|`/p7` *Percorso*|Specifica di produrre un file PKCS (Public Key Cryptography Standards) #7 per ogni file di contenuto specificato. PKCS #7 file sono *denominati* path \\ *filename*.p7.|  
|`/p7ce` *Valore*|Specifica le opzioni per il contenuto PKCS #7 firmato. Impostare *Valore* su "Embedded" per incorporare il contenuto firmato nel file PKCS #7 o su "DetachedSignedData" per generare la parte di dati firmati di un file PKCS #7 scollegato. Se non si usa l'opzione `/p7ce`, il contenuto firmato è incorporato per impostazione predefinita.|  
|`/p7co` *\<OID>*|Specifica l'identificatore di oggetto (OID) tramite cui viene identificato il contenuto PKCS #7 firmato.|  
|`/ph`|Se supportato, genera gli hash delle pagine per i file eseguibili.|  
|`/r`  *RootSubjectName*|Specifica il nome del soggetto del certificato radice cui deve essere concatenato il certificato di firma. Questo valore può essere una sottostringa dell'intero nome del soggetto del certificato radice.|  
|`/s`  *StoreName*|Specifica l'archivio da aprire durante la ricerca del certificato. Se questa opzione non è specificata, viene aperto l'archivio `My`.|  
|`/sha1`  *Hash*|Specifica l'hash SHA1 del certificato di firma. Il valore hash SHA1 viene specificato in genere quando più certificati soddisfano i criteri specificati dalle opzioni rimanenti.|  
|`/sm`|Specifica di usare un archivio del computer anziché un archivio utente.|  
|`/t`  *URL*|Specifica l'URL del server di timestamp. Se questa opzione (o `/tr`) non è presente, al file firmato non verrà aggiunto il timestamp. Se l'aggiunta del timestamp non riesce, viene generato un avviso. Non è possibile usare questa opzione con l'opzione `/tr`.|  
|`/td`  *Alg*|Usata con l'opzione `/tr` per richiedere un algoritmo digest usato dal server di timestamp RFC 3161. </br> **Nota:** Viene generato un avviso se <strong>l'opzione /td</strong> non viene specificata durante il timestamp. L'alg predefinito è SHA1, ma è consigliato SHA256. <br/> <strong>L'opzione /td</strong> deve essere dichiarata dopo <strong>l'opzione /tr,</strong> non prima. Se <strong>l'opzione /td</strong> viene dichiarata prima dell'opzione <strong>/tr,</strong> il timestamp restituito deriva da un algoritmo SHA1 anziché dall'algoritmo SHA256 previsto. |
|`/tr`  *URL*|Specifica l'URL del server di timestamp RFC 3161. Se questa opzione (o `/t`) non è presente, al file firmato non verrà aggiunto il timestamp. Se l'aggiunta del timestamp non riesce, viene generato un avviso. Non è possibile usare questa opzione con l'opzione `/t`.|  
|`/u`  *Utilizzo*|Specifica l'utilizzo chiavi avanzato (EKU) che deve essere presente nel certificato di firma. Il valore di utilizzo può essere specificato tramite OID o stringa. L'utilizzo predefinito è "Firma codice" (1.3.6.1.5.5.7.3.3).|  
|`/uw`|Specifica l'utilizzo di "Verifica dei componenti di sistema Windows" (1.3.6.1.4.1.311.10.3.6).|  
  
 Per esempi di utilizzo, vedere [Using SignTool to Sign a File](using-signtool-to-sign-a-file.md) (Uso di SignTool per firmare un file).  
  

## <a name="timestamp-command-options"></a>Opzioni del comando TimeStamp  

 Nella tabella seguente vengono illustrate le opzioni utilizzabili con il comando `TimeStamp`.  
  
|Opzione TimeStamp|Descrizione|  
|----|----|  
|`/p7`|Aggiunge un timestamp ai file PKCS #7.|  
|`/t`  *URL*|Specifica l'URL del server di timestamp. È necessario che il file a cui viene aggiunto il timestamp sia stato precedentemente firmato. È richiesta l'opzione `/t` o `/tr`.|  
|`/td`  *Alg*|Usata con l'opzione `/tr` per richiedere un algoritmo digest usato dal server di timestamp RFC 3161. </br> **Nota:** Viene generato un avviso se <strong>l'opzione /td</strong> non viene specificata durante il timestamp. L'alg predefinito è SHA1, ma è consigliato SHA256. <br/> <strong>L'opzione /td</strong> deve essere dichiarata dopo <strong>l'opzione /tr,</strong> non prima. Se <strong>l'opzione /td</strong> viene dichiarata prima dell'opzione <strong>/tr,</strong> il timestamp restituito deriva da un algoritmo SHA1 anziché dall'algoritmo SHA256 previsto. |
|`/tp`*index*|Aggiunge un timestamp alla firma in corrispondenza di *indice*.|  
|`/tr`  *URL*|Specifica l'URL del server di timestamp RFC 3161. È necessario che il file a cui viene aggiunto il timestamp sia stato precedentemente firmato. È richiesta l'opzione `/tr` o `/t`.|  


## <a name="verify-command-options"></a>Verificare le opzioni del comando  

|Opzione Verify|Descrizione|
|----|----|
| **/a** | Specifica che tutti i metodi possono essere usati per verificare il file. Innanzitutto, viene effettuata una ricerca nei database dei cataloghi per determinare se il file è firmato in un catalogo. Se il file non è firmato in alcun catalogo, SignTool tenta di verificare la firma incorporata del file. Questa opzione è consigliata per la verifica di file che possono risultare firmati o non firmati all'interno di un catalogo. Esempi di file che possono o non possono essere firmati includono Windows file o driver. |
| **/ad** | Trova il catalogo usando il database dei cataloghi predefinito. |
| **/all** | Verifica tutte le firme in un file con più firme. |
| **/as** | Trova il catalogo usando il database dei cataloghi (driver) dei componenti del sistema. |
| **/ag** *CatDBGUID* | Trova il catalogo nel database del catalogo identificato dal **GUID**. |
| **/c** *CatFile* | Specifica il file di catalogo in base al nome. |
| **/d** | Stampare la descrizione e l'URL della descrizione.<br/> **Windows Vista e versioni precedenti:** Questo flag non è supportato.<br/> |
| **/ds** *Index* | Verifica la firma in una determinata posizione. |
| **/hash**{**SHA1** \| **SHA256**} | Specifica un algoritmo hash facoltativo da usare quando si cerca un file in un catalogo. |
| **/kp** | Esegue la verifica usando i criteri di firma del driver in modalità kernel x64. |
| **/ms** | Usa semantica di verifica multipla. Questo è il comportamento predefinito di una [**chiamata WinVerifyTrust.**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) |
| **/o** *Versione* | Verifica il file in base alla versione del sistema operativo. Il parametro version ha il formato seguente:<br/> *PlatformID***:**_VerMajor_*_._ *_VerMinor_*_._ * _BuildNumber_<br/> È consigliabile usare *l'opzione /o.* Se */o non* è specificato, SignTool può restituire risultati imprevisti. Ad esempio, se non si include l'opzione */o,* i cataloghi di sistema che vengono convalidati correttamente in un sistema operativo precedente potrebbero non essere convalidati correttamente in un sistema operativo più recente. |
| **/p7** | Verificare i file PKCS \# 7. Non vengono usati criteri esistenti per la convalida PKCS \# 7. La firma viene controllata e viene creata una catena per il certificato di firma. |
| **/pa** | Specifica che vengono usati i criteri di verifica dell'autenticazione predefiniti. Se **l'opzione /pa** non è specificata, SignTool usa i Windows di verifica del driver. Questa opzione non può essere usata con le **opzioni catdb.** |
| **/pg** *PolicyGUID* | Specifica i criteri di verifica in base **al GUID**. Il **GUID** corrisponde all'ActionID dei criteri di verifica. Questa opzione non può essere usata con le **opzioni catdb.** |
| **/ph** | Stampare e verificare i valori hash della pagina.<br/> **Windows Vista e versioni precedenti:** Questo flag non è supportato.<br/>  |
| **/r** *RootSubjectName* | Specifica il nome del soggetto del certificato radice cui deve essere concatenato il certificato di firma. Questo valore può essere una sottostringa dell'intero nome del soggetto del certificato radice. |
| **/tw** | Specifica che viene generato un avviso se la firma non è contrassegnata con il timestamp.|


Il comando SignTool **verify** determina se il certificato di firma è stato emesso da un'autorità attendibile, se il certificato di firma è stato revocato e, facoltativamente, se il certificato di firma è valido per un criterio specifico.  

Il comando SignTool **verify** restituisce lo stato della firma incorporata, a meno che non venga specificata un'opzione per la ricerca in un catalogo (/a, /ad, /as, /ag, /c). 


## <a name="return-value"></a>Valore restituito  

 Lo strumento Firma restituisce uno dei seguenti codici di uscita quando termina.  
  
|Codice di uscita|Descrizione|  
|----|----| 
|0|Esecuzione completata correttamente.|  
|1|Esecuzione non riuscita.|  
|2|Esecuzione completata con avvisi.|


## <a name="examples"></a>Esempio  

 Il seguente comando aggiunge il file di catalogo MyCatalogFileName.cat al database dei driver e dei componenti di sistema. L'opzione `/u` genera un nome univoco, se necessario, per impedire la sostituzione di un file di catalogo esistente denominato `MyCatalogFileName.cat`.  
  
```console  
signtool catdb /v /u MyCatalogFileName.cat  
```  
  
 Il comando seguente firma automaticamente un file usando il certificato migliore.  
  
```console  
signtool sign /a /fd SHA256 MyFile.exe 
```  
  
 Il comando seguente appone una firma digitale a un file usando un certificato archiviato in un file PFX protetto da password.  
  
```console  
signtool sign /f MyCert.pfx /p MyPassword /fd SHA256 MyFile.exe 
```  
  
 Il comando seguente appone una firma digitale e un timestamp a un file. Il certificato usato per firmare il file è memorizzato in un file PFX.  
  
```console  
signtool sign /f MyCert.pfx /t http://timestamp.digicert.com /fd SHA256 MyFile.exe 
```  
  
 Il comando seguente firma un file usando un certificato contenuto nell'archivio `My` con nome soggetto `My Company Certificate`.  
  
```console  
signtool sign /n "My Company Certificate" /fd SHA256 MyFile.exe 
```  
  
 Il comando seguente firma un controllo ActiveX e fornisce le informazioni visualizzate da Internet Explorer quando viene richiesto all'utente di installare il controllo.  
  
```console  
Signtool sign /f MyCert.pfx /d: "MyControl" /du http://www.example.com/MyControl/info.html /fd SHA256 MyControl.exe 
```  
  
 Il comando seguente appone un timestamp a un file a cui è già stata apposta una firma digitale.  
  
```console  
signtool timestamp /t http://timestamp.digicert.com MyFile.exe
```  

Il comando seguente imposta il timestamp di un file usando un server timestamp RFC 3161.  
  
```console  
signtool timestamp /tr http://timestamp.digicert.com /td SHA256 MyFile.exe
```  
  
 Il comando seguente verifica che un file sia stato firmato.  
  
```console  
signtool verify MyFile.exe  
```  
  
 Il comando seguente verifica un file di sistema che può essere firmato in un catalogo.  
  
```console  
signtool verify /a SystemFile.dll  
```  
  
 Il comando seguente verifica un file di sistema firmato in un catalogo denominato `MyCatalog.cat`.  
  
```console  
signtool verify /c MyCatalog.cat SystemFile.dll  
```  
