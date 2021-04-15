---
title: Proprietà dell'estensione di IIS per BITS
description: Servizio trasferimento intelligente in background (BITS) utilizza un ISAPI per estendere IIS per supportare i processi di caricamento.
ms.assetid: 08a40cc1-ec6d-4b65-971a-15c7b06df148
keywords:
- BITS proprietà estensione IIS BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09412f6aa0be1ab76e6e45ea0920e1caf1054d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516971"
---
# <a name="bits-iis-extension-properties"></a>Proprietà dell'estensione di IIS per BITS

Servizio trasferimento intelligente in background (BITS) utilizza un ISAPI per estendere IIS per supportare i [**processi di caricamento**](/windows/win32/api/bits/ne-bits-bg_job_type). Nella tabella seguente sono elencate le proprietà aggiunte da BITS alla metabase IIS per il componente directory virtuale. BITS usa queste proprietà per determinare come caricare i file. Le proprietà dell'estensione IIS BITS sono ereditabili, ad eccezione di **BITSUploadEnabled**.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BITSUploadEnabled</strong> Tipo di dati: <strong>Boolean</strong><br/></td>
<td>Indica se i caricamenti BITS sono abilitati nella directory virtuale. Se l'impostazione non è presente o è 0, i caricamenti BITS sono disabilitati.<br/> Questa proprietà è di sola lettura. Per impostare questa proprietà, chiamare il metodo <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads"><strong>EnableBITSUploads</strong></a> o <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-disablebitsuploads"><strong>DisableBITSUploads</strong></a> dell'interfaccia <a href="/windows/win32/api/bitscfg/nn-bitscfg-ibitsextensionsetup"><strong>IBITSExtensionSetup</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><strong>BITSSessionTimeout</strong> Tipo di dati: <strong>DWORD</strong><br/></td>
<td>Numero di secondi durante i quali la connessione viene mantenuta se non è stato eseguito il caricamento del file. il timer viene reimpostato quando viene eseguito lo stato di avanzamento. BITS chiude la connessione se viene raggiunto il timeout e pulisce i dati associati alla sessione.<br/> L'impostazione di un timeout di sessione breve può costituire un problema per i processi di caricamento-risposta, perché la risposta viene scaricata solo quando l'utente è connesso e connesso alla rete. È possibile che la sessione si timeout prima che la risposta venga scaricata, nel qual caso la sessione viene annullata e il file di risposta viene eliminato.<br/> Si noti che BITS Annulla il processo se viene raggiunto il valore <a href="/windows/win32/bits/group-policies">JobInactivityTimeout</a> criteri di gruppo (il valore predefinito è 90 giorni), indipendentemente da questa impostazione.<br/> Il valore predefinito è 1.209.600 (14 giorni).<br/></td>
</tr>
<tr class="odd">
<td><strong>BITSMaximumUploadSize</strong> Tipo di dati: <strong>String</strong><br/></td>
<td>Numero massimo di byte che è possibile caricare per processo. Specificare il numero massimo di byte come stringa decimale. il valore della stringa deve essere minore o uguale a &quot; 1844674407370955 &quot; . Una stringa vuota equivale a specificare &quot; 1844674407370955 &quot; .<br/> Il valore predefinito è una stringa vuota.<br/>
<blockquote>
[!Note]<br />
In IIS 7, il limite di caricamento predefinito è pari a 30 milioni byte. Il valore della proprietà <strong>BITSMaximumUploadSize</strong> non può superare il limite di IIS. Per informazioni dettagliate e informazioni sulla modifica del valore predefinito di IIS, vedere <a href="https://support.microsoft.com//kb/942074">KB942074</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>BITSServerNotificationType</strong> Tipo di dati: <strong>DWORD</strong><br/></td>
<td>Specifica come inviare il file di caricamento all'applicazione server. I valori possibili sono: 0, 1 e 2.<br/> Il valore 0 indica che il file non viene inviato all'applicazione server. BITS inserisce il file di caricamento nella directory specificata nel nome remoto (il nome remoto specificato quando è stato <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-addfile">aggiunto il file</a> al processo) senza notificare l'applicazione server. Se il file attualmente esiste nella directory di destinazione, viene sostituito con il file di caricamento.<br/> Il valore 1 indica che BITS passa il percorso del file di caricamento all'applicazione server specificata nella proprietà <strong>BITSServerNotificationURL</strong> . Se necessario, l'applicazione server elabora il file e genera un file di risposta. Per impostazione predefinita, BITS rimuove i file di caricamento e di risposta dal server dopo aver ricevuto la risposta dall'applicazione server. Per fare in modo che BITS copi il file di caricamento nel percorso specificato dal nome del file remoto nel processo, includere l'intestazione <a href="/windows/win32/bits/notification-protocol-for-server-applications">bits-copy-file-to-Destination</a> nella risposta. Se non si include l'intestazione e si desidera salvare i file di caricamento e di risposta, è necessario copiare i file di caricamento e di risposta in un nuovo percorso prima di rispondere.<br/> Il valore 2 indica che BITS passa il file di caricamento nel corpo della richiesta all'applicazione server specificata nella proprietà <strong>BITSServerNotificationURL</strong> . L'applicazione server elabora il file e restituisce la risposta nel corpo della risposta, se necessario.<br/> Per informazioni dettagliate sulle intestazioni di richiesta e risposta, vedere <a href="/windows/win32/bits/notification-protocol-for-server-applications">protocollo di notifica per le applicazioni server</a>.<br/> L'applicazione server deve fornire una risposta entro cinque minuti. Se l'applicazione server non risponde entro cinque minuti, il processo entra nello stato di errore temporaneo. Quando il <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay"><strong>ritardo tra tentativi</strong></a> scade, il server BITS invierà un'altra notifica all'applicazione server (l'applicazione server deve essere scritta per gestire le notifiche duplicate). <strong>BITS 1,5:</strong> Il timeout della notifica è di 30 secondi.<br/> <br/> Il valore predefinito è 0.<br/></td>
</tr>
<tr class="odd">
<td><strong>BITSServerNotificationURL</strong> Tipo di dati: <strong>String</strong><br/></td>
<td>facoltativo. Contiene l'URL dell'applicazione server a cui BITS inserisce il file di caricamento. È necessario specificare un URL se il valore della proprietà <strong>BITSServerNotificationType</strong> è 1 o 2. L'URL è limitato a 2.200 caratteri, escluso il carattere di terminazione null. L'URL deve essere un URL HTTP; BITS non supporta gli URL di notifica HTTPS.<br/> Se l'URL non è disponibile al momento del caricamento, BITS tenterà di eseguire il caricamento fino a quando l'URL di notifica non esiste o fino alla scadenza del periodo di ripetizione dei tentativi.<br/> Si noti che se il nome remoto specificato nel processo contiene una stringa di query, la stringa di query viene aggiunta all'URL specificato. Se, ad esempio, il nome remoto contiene https://myserver/myvdir/subdir/file.asp?ACCOUNT=86433 e si specifica l'impostazione di <strong>BITSServerNotificationURL</strong> come https://otherserver/myvdir2/bag.asp , l'URL a cui i post BITS è https://otherserver/myvdir2/bag.asp?ACCOUNT=86433 .<br/> Se l'URL originale è https://myserver/myvdir/file.txt e l'URL di notifica è myasp. asp, BITS USA http//MyServer/MyVDir/myasp. asp come URL di notifica.<br/> Se la parte relativa al percorso e al nome file dell'URL contiene caratteri Unicode non comuni alla tabella codici nel client e nel server, la conversione dell'URL avrà esito negativo nel server e il processo BITS verrà inserito nello stato di errore. Se la parte relativa al server dell'URL contiene caratteri Unicode, è necessario codificare la parte del server usando <a href="/windows/win32/intl/handling-internationalized-domain-names--idns">i nomi di dominio internazionali</a> (IDN).<br/></td>
</tr>
<tr class="even">
<td><strong>BITSHostId</strong> Tipo di dati: <strong>String</strong><br/></td>
<td>Impostare questa proprietà se l'installazione del server è un Web farm che non utilizza l'archiviazione condivisa.<br/> Specificare il nome del server o l'indirizzo IP del server a cui riconnettersi dopo che il processo di caricamento è stato interrotto. In genere, si specifica il nome del server che si sta configurando. L'URL è limitato a 300 caratteri, escluso il carattere di terminazione null.<br/> Se non si specifica questa proprietà e il processo di caricamento viene interrotto, è possibile che BITS riprenda il processo in un altro server della farm. Tuttavia, il server precedente contiene ancora il file di caricamento parziale da prima dell'interruzione. BITS rimuove il file parziale dopo la scadenza del <strong>BITSSessionTimeout</strong> .<br/>
<blockquote>
[!Note]<br />
Non utilizzare la proprietà <strong>BITSHostId</strong> se SSL viene utilizzato in un Web farm che utilizza bilanciamento carico di rete (NLB) o nomi DNS con più indirizzi IP, a meno che non si includa il nome del cluster e i nomi dei singoli server nel certificato. Se il nome del server specificato in <strong>BITSHostId</strong> non corrisponde al nome comune nel certificato, il processo avrà esito negativo. Al contrario, per NLB, impostare il parametro <a href="/previous-versions/tn-archive/bb687542(v=technet.10)">affinity</a> su <strong>Single</strong> per garantire che il client comunichi con lo stesso server in futuro.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSHostIdFallbackTimeout</strong> Tipo di dati: <strong>DWORD</strong><br/></td>
<td>Numero di secondi durante i quali il client BITS tenta di riconnettersi al nome del server <strong>BITSHostId</strong> prima di ripristinare il nome host specificato nel nome file remoto del processo. Il timer inizia quando BITS non è in grado di connettersi al server <strong>BITSHostId</strong> . Il timer viene reimpostato quando il client si connette correttamente al server.<br/> Si noti che il valore di timeout nessun stato del processo (vedere <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout"><strong>Metodo ibackgroundcopyjob:: SetNoProgressTimeout</strong></a>) deve essere più lungo del valore di timeout. In caso contrario, il processo avrà esito negativo prima della scadenza del valore di timeout di fallback.<br/> Impostare questa proprietà solo se si imposta la proprietà <strong>BITSHostId</strong> .<br/> Il valore predefinito è 86.400 (1 giorno).<br/></td>
</tr>
<tr class="even">
<td><strong>BITSAllowOverwrites</strong> Tipo di dati: <strong>Integer</strong><br/></td>
<td>Indica se un file di caricamento può sovrascrivere un file esistente con lo stesso nome. Il file di caricamento sovrascrive il file esistente se <strong>BITSAllowOverwrites</strong> è 1.<br/> Il valore predefinito è 0.<br/> <strong>IIS 6,0:</strong> È possibile impostare questa proprietà solo da uno script, non è possibile impostarla utilizzando la pagina delle proprietà dell'estensione BITS nell'interfaccia utente di IIS.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSCleanupUseDefault</strong> Tipo di dati: <strong>Boolean</strong><br/></td>
<td>Indica se l'attività di pulizia utilizza le pianificazioni predefinite. Per impostazione predefinita, l'attività di pulizia viene eseguita ogni 12 ore.<br/> Impostare su 1 per utilizzare la pianificazione predefinita. in caso contrario, 0 per specificare una pianificazione.<br/> Per specificare una pianificazione, usare le proprietà <strong>BITSCleanupCount</strong> e <strong>BITSCleanupUnits</strong> .<br/> L'attività di pulizia pulisce la directory virtuale eliminando i processi che non sono stati modificati entro il periodo di timeout della sessione (vedere <strong>BITSSessionTimeout</strong>).<br/> Il valore predefinito è 1. utilizzare la pianificazione predefinita.<br/> <strong>IIS 6,0:</strong> Non supportato.<br/></td>
</tr>
<tr class="even">
<td><strong>BITSCleanupCount</strong> Tipo di dati: <strong>Integer</strong><br/></td>
<td>Specifica l'intervallo di attesa tra l'esecuzione dell'attività di pulizia. L'intervallo che è possibile specificare dipende dalle unità. Per i valori di intervallo possibili, vedere la proprietà <strong>BITSCleanupUnits</strong> .<br/> Questa proprietà viene ignorata se <strong>BITSCleanupUseDefault</strong> è 0.<br/> <strong>IIS 6,0:</strong> Non supportato.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSCleanupUnits</strong> Tipo di dati: <strong>Integer</strong><br/></td>
<td>Specifica le unità per l'intervallo di pulizia specificato nella proprietà <strong>BITSCleanupCount</strong> . Questa proprietà viene ignorata se <strong>BITSCleanupUseDefault</strong> è 0.<br/> I valori possibili sono:<dl> 0: le unità sono in minuti. I valori possibili sono compresi tra 1 e 60.<br />
1: le unità sono ore. Questo è il valore predefinito. I valori possibili sono compresi tra 1 e 24.<br />
2: le unità sono giorni. I valori possibili sono compresi tra 1 e 360.<br />
</dl> <br/> <strong>IIS 6,0:</strong> Non supportato.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>BITSNumberOfSessionsLimit</strong> Tipo di dati: <strong>Integer</strong><br/></td>
<td>Limita il numero di sessioni di caricamento che possono esistere simultaneamente per un utente. Se il numero di sessioni per un utente è superiore a questo limite, quando viene eseguita l'attività di pulizia eliminerà le sessioni più recenti finché il numero di sessioni per l'utente non è inferiore al limite.<br/> Il valore predefinito è 50 sessioni.<br/> <strong>IIS 6,0:</strong> Non supportato.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSSessionLimitEnable</strong> Tipo di dati: <strong>Boolean</strong><br/></td>
<td>Indica se BITS limita il numero di sessioni di caricamento per utente. Se l'impostazione non è presente o è 0, il limite è disabilitato.<br/> Per specificare il limite, impostare la proprietà <strong>BITSNumberOfSessionsLimit</strong> .<br/> Il valore predefinito è 1.<br/> <strong>IIS 6,0:</strong> Non supportato.<br/> <br/></td>
</tr>
</tbody>
</table>



 

Nell'esempio seguente viene illustrato come impostare le proprietà dell'estensione IIS BITS utilizzando Windows script host. Se la directory virtuale punta a una condivisione remota, impostare anche le proprietà IIS **UNCUserName** e **UNCPassword** .


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

// Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



 

