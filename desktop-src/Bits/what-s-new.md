---
title: Novità (BITS)
description: La tabella seguente identifica le novità per ogni versione di Servizio trasferimento intelligente in background (BITS).
ms.assetid: ef05f2e1-88be-4adb-aca7-a7b1451cfd04
keywords:
- Novità
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b171a1d8cede9e3fd49ac81ab47ffb09f72b6200
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047677"
---
# <a name="whats-new-bits"></a>Novità (BITS)

Dal primo rilascio come parte di Windows XP, il Servizio trasferimento intelligente in background (BITS) è stato continuamente migliorato, con l'aggiunta di controlli più potenti per lo sviluppatore e l'amministratore per il controllo e la gestione dei download. È stato aggiunto un set completo di cmdlet di PowerShell. può connettersi a più tipi di server HTTP; è più attento alla larghezza di banda di rete dell'utente e ai costi che mai. 

La tabella seguente identifica le novità per ogni versione di Servizio trasferimento intelligente in background (BITS).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Versione</th>
<th>Descrizione delle funzionalità</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Versione 10,3</td>
<td>Nuove funzionalità:<br/>
<ul>
<li>Aggiunta di <a href="/windows/win32/api/bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3"><strong>BackgroundCopyJobHttpOptions3</strong></a> per contrassegnare le intestazioni HTTP come di sola scrittura e per impostare un callback di convalida del certificato server.</li>
<li>BITS manterrà l'identità del servizio quando viene creata da un altro servizio di sistema.</li>
<li>BITS continuerà a trasferire i file in modalità standby connessa, purché il dispositivo sia collegato.</li>
</ul>
BITS versione 10,3 è incluso nell'aggiornamento di Windows 10 May 2019 (10,0; Compilazione 18362) e versioni successive.
</td>
</tr>
<tr class="even">
<td>Versione 10,2</td>
<td>Nuove funzionalità:<br/>
<ul>
<li>Aggiunta di <a href="/windows/win32/api/bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2"><strong>BackgroundCopyJobHttpOptions2</strong></a> per modificare il metodo HTTP per i download http.</li>
<li>BITS USA ora l'ordinamento proxy predefinito per essere più coerente con il resto del sistema.</li>
<li>È più semplice per i programmatori impostare la configurazione del proxy BITS per gli scenari aziendali.</li>
<li>BITS è ora più attenta alla potenza e supporta la [modalità standby moderna](/windows-hardware/design/device-experiences/modern-standby).</li>
<li>BITS supporta ora i [criteri](/windows/client-management/mdm/policy-configuration-service-provider) di gestione di dispositivi mobili (MDM) oltre ai [criteri di gruppo](./group-policies).</li>
</ul>
BITS versione 10,2 è incluso nell'aggiornamento di Windows 10 ottobre 2018 (10.0; Compilazione 17763) e versioni successive.
</td>
</tr>
<tr class="odd">
<td>Versione 10,1</td>
<td>Nuove funzionalità:<br/>
<ul>
<li>Sono stati aggiunti <a href="/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6"><strong>BackgroundCopyFile6</strong></a> e <a href="/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3"><strong>IBackgroundCopyCallback3</strong></a> per abilitare gli scenari di accesso casuale per i download http.</li>
<li>Aggiunta <strong>BITS_JOB_PROPERTY_ON_DEMAND_MODE</strong> e <strong>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS</strong> all'enumerazione <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a> per ottimizzare i comportamenti di download e notifica, rispettivamente.</li>
</ul>
BITS versione 10,1 è incluso in Windows 10 Creators Update e versioni successive.
</td>
</tr>
<tr class="even">
<td>Versione 5.0</td>
<td>Nuove funzionalità:<br/>
<ul>
<li>Aggiunta dell'interfaccia <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> che aggiunge metodi generici per ottenere e impostare le proprietà del processo BITS sui metodi ereditati dall'interfaccia <a href="/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4"><strong>IBackgroundCopyJob4</strong></a> .<br/> Per informazioni sull'uso della nuova interfaccia <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> , vedere <a href="how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md">come controllare se un processo BITS può essere scaricato tramite una connessione costosa</a> e <a href="how-to-get-the-last-set-of-http-headers-received-for-each-file-in-a-bits-download-job.md">come ottenere l'ultimo set di intestazioni HTTP ricevute per ogni file in un processo di download BITS</a>.<br/></li>
<li>Aggiunta dell'Unione <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_job_property_value"><strong>BITS_JOB_PROPERTY_VALUE</strong></a> e delle enumerazioni <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_transfer_policy"><strong>BITS_JOB_TRANSFER_POLICY</strong></a> e <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a>. Per esempi di utilizzo, vedere le procedure illustrate sopra.</li>
<li>È stata aggiunta l'interfaccia <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> , che consente di aggiungere metodi per ottenere e impostare le proprietà generiche negli oggetti BackgroundCopyFile nei metodi ereditati dall'interfaccia <a href="/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4"><strong>IBackgroundCopyFile4</strong></a> . L'aggiunta di proprietà generiche renderà possibile il miglioramento delle funzionalità di BackgroundCopyFile in futuro senza richiedere la creazione di una nuova interfaccia.</li>
<li>La prima proprietà generica esposta da <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> è la proprietà <strong>HttpResponseHeaders</strong> .</li>
<li>Aggiunta dell'Unione <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value"><strong>BITS_FILE_PROPERTY_VALUE</strong></a> e dell'enumerazione <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_file_property_id"><strong>BITS_FILE_PROPERTY_ID</strong></a> .</li>
</ul>
BITS versione 5,0 è incluso nei sistemi operativi Windows Server 2012 e Windows 8, dove la versione di% windir% \System32\QMgr.dll è &quot; 7.7. xxxx. xxxx &quot; .<br/> Le funzionalità seguenti sono state aggiunte a BITS in Windows 10<br/>
<ul>
<li>In Windows 10, versione 1607, è possibile usare le API COM BITS e i cmdlet di PowerShell BITS (dove disponibili) in una sessione remota di PowerShell. Ciò è particolarmente utile quando si amministrano versioni di Windows Server 2016 che non dispongono di funzionalità di accesso locale. I processi BITS avviati tramite sessioni remote di PowerShell vengono eseguiti nel contesto dell'account utente della sessione e registrano progressi solo in presenza di almeno una sessione di accesso locale attiva o una sessione remota di PowerShell associata a tale account utente. Prendere in considerazione l'uso di sessioni remote di PowerShell persistenti (vedere <a href="/powershell/module/microsoft.powershell.core/new-pssession">New-PSSession</a>) per i trasferimenti con esecuzione prolungata.</li>
<li>In Windows 10, versione 1607, è ora possibile per un proprietario di un processo BITS impostare i token Helper senza essere un amministratore, purché il token Helper non disponga delle funzionalità di amministratore. Si riduce così la vulnerabilità correlata agli strumenti di download o aggiornamento in background, che possono essere eseguiti con l'account NetworkService con minori privilegi anziché con un account con privilegi di amministratore.</li>
</ul>
In Windows 10 è incluso anche BITS versione 5,0, in cui la versione di% windir% \System32\QMgr.dll è &quot; 7,8. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Versione 4.0</td>
<td>Nuove funzionalità:<br/>
<ul>
<li>La memorizzazione nella cache peer USA ora Windows BranchCache. Questo nuovo modello di Caching peer sostituisce il modello usato per BITS versione 3,0. Per ulteriori informazioni, vedere <a href="peer-caching.md">peer caching</a>.</li>
<li>È stato aggiunto un modello di accesso alle risorse più flessibile che consente alle applicazioni di associare una coppia di token di sicurezza a un processo di trasferimento BITS. Per ulteriori informazioni, vedere <a href="helper-tokens-for-bits-transfer-jobs.md">token helper per i processi di trasferimento BITS</a>.</li>
<li>È stato aggiunto il <a href="bits-compact-server.md">server BITS Compact</a>, ovvero un file server HTTP/HTTPS autonomo che consente di trasferire in modo asincrono un numero limitato di file di grandi dimensioni tra computer.</li>
<li>Aggiunta limitazione della larghezza di banda più granulare. Per ulteriori informazioni, vedere <a href="group-policies.md">criteri di gruppo</a>.</li>
</ul>
BITS versione 4,0 è incluso nei sistemi operativi Windows Server 2008 R2 e Windows 7.<br/> È inoltre possibile scaricare BITS 4,0 per Windows Server 2008 con Service Pack 2 (SP2), Windows Vista con Service Pack 1 (SP1) e Windows Vista con Service Pack 2 (SP2). Per informazioni sul download di BITS 4,0, vedere <a href="https://support.microsoft.com/kb/968929">KB968929</a>.<br/> La versione di% windir% \System32\QMgr.dll è &quot; 7.5. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Versione 3.0</td>
<td>Nuove funzionalità:<br/>
<ul>
<li>Aggiunta della <a href="peer-caching.md">memorizzazione nella cache peer</a> che consente di scaricare il contenuto dai peer e di fornire contenuti ai peer in una rete di dominio.</li>
<li>Aggiunta della <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">notifica</a> per il download di un file.</li>
<li>È stato aggiunto l'accesso al <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname">file temporaneo</a> mentre è in corso il download.</li>
<li>È stata aggiunta la possibilità di controllare i <a href="/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags">reindirizzamenti</a>http.</li>
<li>Aggiunta di altri <a href="group-policies.md">criteri di gruppo</a> per controllare la memorizzazione nella cache del peer e limitare i tempi di download.</li>
<li>Aggiunta di eventi di diagnostica e risoluzione dei problemi al registro eventi di sistema.</li>
<li>Aggiunta del supporto per il <a href="user-account-control-and-bits.md">controllo dell'account utente</a> (UAC).</li>
<li>In Windows Vista e versioni successive, il tipo di avvio BITS predefinito è l'avvio automatico ritardato.</li>
</ul>
<blockquote>
[!Note]<br />
BITS USA ora i criteri di gruppo per limitare il numero di processi e file che è possibile creare. Questo potrebbe influire sulle applicazioni che attualmente creano un numero elevato di processi o aggiungono un numero elevato di file a un processo.
</blockquote>
<br/> <br/> BITS versione 3,0 è incluso nei sistemi operativi Windows Server 2008 e Windows Vista. <br/> La versione di% windir% \System32\QMgr.dll è &quot; 7.0. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Versione 2,5</td>
<td>Aggiunta del supporto per intestazioni HTTP personalizzate, autenticazione client basata su certificato per trasporti HTTP protetti e IPv6. Aggiunta anche dell'uso dei contatori del dispositivo gateway Internet (IGD) per calcolare con maggiore precisione la <a href="network-bandwidth.md">larghezza di banda</a>disponibile.<br/> Le funzionalità BITS 2,5 sono disponibili nei sistemi operativi Windows Server 2008, Windows Vista e Windows XP con Service Pack 3 (SP3). <br/> È anche possibile scaricare BITS 2,5 per Windows Server 2003 con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1) e Windows XP con Service Pack 2 (SP2). Per scaricare BITS 2,5, visitare l' <a href="https://www.microsoft.com/download/details.aspx?id=4933">area download Microsoft</a> e installare KB923845.<br/> La versione di% windir% \System32\QMgr.dll è &quot; 6.7. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Versione 2,0</td>
<td>Aggiunta del supporto per l'esecuzione di download simultanei in primo piano, usando i percorsi Server Message Block (SMB) per i nomi remoti, il download degli intervalli di un file, la modifica del prefisso o il nome completo di un nome remoto e la limitazione dell'utilizzo della larghezza di banda client. Il criterio JobInactivityTimeout è ora disponibile in configurazione computer, Modelli amministrativi, rete, Servizio trasferimento intelligente in background (BITS).<br/> BITS versione 2,0 è incluso in Windows XP con SP2 e Windows Server 2003 con SP1. È anche possibile scaricare BITS 2,0 per Windows Server 2003 e Windows XP. Per scaricare BITS 2,0, visitare l' <a href="https://www.microsoft.com/download/details.aspx?id=19031">area download Microsoft</a> e installare KB842773.<br/> La versione di% windir% \System32\QMgr.dll è &quot; 6.6. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Versione 1.5</td>
<td>Aggiunta della funzionalità di caricamento e caricamento-risposta, esecuzione della riga di comando per gli eventi e credenziali esplicite e credenziali proxy.<br/> A partire da BITS 1,5, gli utenti con un <a href="/windows/win32/secauthz/restricted-tokens">token con restrizioni</a> non possono creare o modificare i processi.<br/> BITS versione 1,5 è incluso in Windows Server 2003. Un ridistribuibile è disponibile per Windows XP dall' <a href="https://www.microsoft.com/download/details.aspx?id=22250">area download Microsoft</a>.<br/> La versione di% windir% \System32\QMgr.dll è &quot; 6.5. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Versione 1,2</td>
<td>Stessa funzionalità della versione 1,0. Contiene aggiornamenti e miglioramenti interni.<br/> BITS versione 1,2 è incluso in Windows XP con Service Pack 1 (SP1).<br/> La versione di% windir% \System32\QMgr.dll è &quot; 6.2. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Versione 1,0</td>
<td>Versione iniziale. Fornisce i download in ordine di priorità, limitati e asincroni in background o in primo piano. I download vengono ripresi automaticamente dopo il riavvio del computer e la disconnessione della rete.<br/> BITS versione 1,0 è incluso in Windows XP.<br/> La versione di% windir% \System32\QMgr.dll è &quot; 6.0. xxxx. xxxx &quot; .<br/></td>
</tr>
</tbody>
</table>

Per attivare le funzionalità del programma in base alle funzionalità BITS, usare QueryInterface on (ad esempio) l'oggetto Job per verificare se l'oggetto processo consente di creare la versione necessaria. In alternativa, vedere [determinazione della versione dei bit in un computer](./determining-the-version-of-bits-on-a-computer.md) per convertire il numero di versione di QMgr.dll nella versione BITS.

## <a name="version-103"></a>Versione 10,3

Sono state aggiunte le interfacce seguenti per questa versione
-   [**IBackgroundCopyJobHttpOptions3**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3) 
     [ **IBackgroundCopyServerCertificateValidationCallback**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback)


## <a name="version-102"></a>Versione 10,2

Sono state aggiunte le interfacce seguenti per questa versione
-   [**IBackgroundCopyJobHttpOptions2**](/windows/win32/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2)


## <a name="version-101"></a>Versione 10,1

Sono state aggiunte le interfacce seguenti per questa versione
-   [**BackgroundCopyFile6**](/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6)
-   [**IBackgroundCopyCallback3**](/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3)

Sono state aggiunte le costanti seguenti da usare con l' [enumerazione BITS_JOB_PROPERTY_ID](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id).

-   **\_Proprietà processo \_ bits \_ in \_ \_ modalità richiesta**
-   **\_intervallo di \_ notifica minimo della proprietà processo BITS \_ \_ \_ \_ ms**


## <a name="version-50"></a>Versione 5.0

Per questa versione sono state aggiunte le interfacce seguenti:

-   [**IBackgroundCopyJob5**](/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5)

## <a name="version-40"></a>Versione 4.0

Per questa versione sono state aggiunte le interfacce seguenti:

-   [**IBitsToken**](/windows/win32/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
-   [**IBackgroundCopyFile4**](/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4)

## <a name="version-30"></a>Versione 3.0

Per questa versione sono state aggiunte le interfacce seguenti:

-   [**IBackgroundCopyCallback2**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2)
-   [**IBackgroundCopyFile3**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3)
-   [**IBackgroundCopyJob4**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4)
-   [**IBitsPeer**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeer)
-   [**IBitsPeerCacheAdministration**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration)
-   [**IBitsPeerCacheRecord**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacherecord)
-   [**IEnumBitsPeerCacheRecords**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords)
-   [**IEnumBitsPeers**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeers)

Sono state aggiunte le costanti seguenti da usare con il metodo [**IBackgroundCopyJobHttpOptions:: SetSecurityFlags**](/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) :

-   **\_criteri di reindirizzamento HTTP di BG \_ \_ \_ Consenti invisibile all' \_ utente**
-   **\_criteri di reindirizzamento HTTP di BG \_ \_ \_ Consenti \_ report**
-   **\_criteri di reindirizzamento http BG non \_ \_ \_ consentiti**
-   **\_maschera dei \_ criteri di reindirizzamento HTTP \_ di BG \_**
-   **i \_ \_ \_ criteri di reindirizzamento HTTP di BG \_ consentono \_ https \_ a \_ http**

## <a name="version-25"></a>Versione 2,5

Per la versione 2,5 sono state aggiunte le seguenti interfacce ed enumerazioni:

-   [**IBackgroundCopyJobHttpOptions**](/windows/win32/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions)
-   [**\_ \_ percorso archivio certificati \_ BG**](/windows/win32/api/Bits2_5/ne-bits2_5-bg_cert_store_location)

## <a name="version-20"></a>Versione 2,0

Per la versione 2,0 sono state aggiunte le interfacce, la struttura e gli argomenti seguenti:

-   [**IBackgroundCopyJob3**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)
-   [**IBackgroundCopyFile2**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2)
-   [**\_intervallo di file BG \_**](/windows/win32/api/Bits2_0/ns-bits2_0-bg_file_range)
-   [Criteri di gruppo](group-policies.md)

Per informazioni sui download simultanei in primo piano, vedere la sezione Osservazioni relativa alla [**\_ \_ priorità del processo BG**](/windows/win32/api/Bits/ne-bits-bg_job_priority).

Per informazioni sull'uso del protocollo SMB, vedere [**\_ \_ informazioni sul file BG**](/windows/win32/api/Bits/ns-bits-bg_file_info).

## <a name="version-15"></a>Versione 1.5

Per la versione 1,5 sono state aggiunte le interfacce e gli argomenti seguenti:

-   [**IBackgroundCopyJob2**](/windows/win32/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
-   [Recupero della risposta da un processo di Upload-Reply](retrieving-the-reply-from-an-upload-reply-job.md)
-   [Registrazione per l'esecuzione di un programma](registering-to-execute-a-program.md)
-   [Impostazioni del server BITS per i processi di caricamento](bits-server-settings-for-upload-jobs.md)
-   [Configurazione del server per i caricamenti](setting-up-the-server-for-uploads.md)
-   [Uso delle intestazioni di richiesta/risposta per le notifiche BITS](using-bits-notification-request-response-headers.md)

 
## <a name="updating-bits-versions"></a>Aggiornamento di versioni BITS
 
È possibile scaricare BITS 4,0 per Windows Server 2008 con Service Pack 2 (SP2), Windows Vista con Service Pack 1 (SP1) e Windows Vista con Service Pack 2 (SP2). Per informazioni sul download di BITS 4,0, vedere [KB968929](https://support.microsoft.com/kb/968929).
