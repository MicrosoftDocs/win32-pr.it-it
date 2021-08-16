---
title: Proprietà dell'estensione di IIS per BITS
description: Servizio trasferimento intelligente in background (BITS) usa un ISAPI per estendere IIS per supportare i processi di caricamento.
ms.assetid: 08a40cc1-ec6d-4b65-971a-15c7b06df148
keywords:
- BITS DELLE proprietà dell'estensione IIS BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c81d57114a23a07c5f952a9cb33399644f5cbed8bbf67cccf802a1c996b72b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835170"
---
# <a name="bits-iis-extension-properties"></a>Proprietà dell'estensione di IIS per BITS

Servizio trasferimento intelligente in background (BITS) usa un ISAPI per estendere IIS per supportare i [**processi di caricamento.**](/windows/win32/api/bits/ne-bits-bg_job_type) Nella tabella seguente sono elencate le proprietà aggiunte da BITS alla metabase IIS per il componente della directory virtuale. BITS usa queste proprietà per determinare come caricare i file. Le proprietà dell'estensione IIS BITS sono ereditabili, ad eccezione di **BITSUploadEnabled**.



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
<td>Indica se i caricamenti BITS sono abilitati nella directory virtuale. Se l'impostazione non è presente o è 0, i caricamenti BITS sono disabilitati.<br/> Questa proprietà è di sola lettura. Per impostare questa proprietà, chiamare il <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads"><strong>metodo EnableBITSUploads</strong></a> o <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-disablebitsuploads"><strong>DisableBITSUploads</strong></a> dell'interfaccia <a href="/windows/win32/api/bitscfg/nn-bitscfg-ibitsextensionsetup"><strong>IBITSExtensionSetup.</strong></a><br/></td>
</tr>
<tr class="even">
<td><strong>BITSSessionTimeout</strong> Tipo di dati: <strong>DWORD</strong><br/></td>
<td>Numero di secondi per cui la connessione viene mantenuta se non viene effettuato alcun avanzamento durante il caricamento del file. il timer viene reimpostato quando viene effettuato lo stato di avanzamento. BITS chiude la connessione se viene raggiunto il timeout ed elimina i dati associati alla sessione.<br/> L'impostazione di un breve timeout di sessione può essere un problema per i processi di caricamento-risposta perché la risposta viene scaricata solo quando l'utente è connesso alla rete. È possibile che la sessione si timeout prima del download della risposta, nel qual caso la sessione viene annullata e il file di risposta viene eliminato.<br/> Si noti che BITS annulla il processo se viene raggiunto il valore <a href="/windows/win32/bits/group-policies">Criteri di gruppo JobInactivityTimeout</a> (il valore predefinito è 90 giorni), indipendentemente da questa impostazione.<br/> Il valore predefinito è 1.209.600 (14 giorni).<br/></td>
</tr>
<tr class="odd">
<td><strong>BITSMaximumUploadSize</strong> Tipo di dati: <strong>Stringa</strong><br/></td>
<td>Numero massimo di byte che è possibile caricare per ogni processo. Specificare il numero massimo di byte come stringa decimale. Il valore della stringa deve essere minore o uguale a &quot; 1844674407370955 &quot; . Una stringa vuota è uguale a quando si specifica &quot; 1844674407370955 &quot; .<br/> Il valore predefinito è una stringa vuota.<br/>
<blockquote>
[!Note]<br />
In IIS 7 il limite di caricamento predefinito è 30 milioni di byte. Il valore della <strong>proprietà BITSMaximumUploadSize</strong> non può superare il limite iis. Per informazioni dettagliate e sulla modifica dell'impostazione predefinita di IIS, <a href="https://support.microsoft.com//kb/942074">vedere KB942074</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>BITSServerNotificationType</strong> Tipo di dati: <strong>DWORD</strong><br/></td>
<td>Specifica come inviare il file di caricamento all'applicazione server. I valori possibili sono: 0, 1 e 2.<br/> Il valore 0 indica che il file non viene inviato all'applicazione server. BITS inserisce il file di caricamento nella directory specificata nel nome remoto (il nome remoto specificato al momento dell'aggiunta del <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-addfile">file</a> al processo) senza notificare all'applicazione server. Se il file esiste attualmente nella directory di destinazione, viene sostituito con il file di caricamento.<br/> Il valore 1 indica che BITS passa il percorso del file di caricamento all'applicazione server specificata nella <strong>proprietà BITSServerNotificationURL.</strong> L'applicazione server elabora il file e genera un file di risposta, se necessario. Per impostazione predefinita, BITS rimuove i file di caricamento e risposta dal server dopo aver ricevuto la risposta dall'applicazione server. Per fare in modo che BITS copia il file di caricamento nel percorso specificato dal nome file remoto nel processo, includere l'intestazione <a href="/windows/win32/bits/notification-protocol-for-server-applications">BITS-Copy-File-To-Destination</a> nella risposta. Se non si include l'intestazione e si vogliono salvare i file di caricamento e risposta, è necessario copiare i file di caricamento e risposta in un nuovo percorso prima di rispondere.<br/> Il valore 2 indica che BITS passa il file di caricamento nel corpo della richiesta all'applicazione server specificata nella <strong>proprietà BITSServerNotificationURL.</strong> L'applicazione server elabora il file e, se necessario, passa nuovamente la risposta nel corpo della risposta.<br/> Per informazioni dettagliate sulle intestazioni di richiesta e risposta, vedere <a href="/windows/win32/bits/notification-protocol-for-server-applications">Protocollo di notifica per applicazioni server</a>.<br/> L'applicazione server deve fornire una risposta entro cinque minuti. Se l'applicazione server non risponde entro cinque minuti, il processo entra nello stato di errore temporaneo. Alla scadenza <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay"><strong>del ritardo tra</strong></a> tentativi, il server BITS invierà un'altra notifica all'applicazione server (l'applicazione server deve essere scritta per gestire le notifiche duplicate). <strong>BITS 1.5:</strong> Il timeout della notifica è di 30 secondi.<br/> <br/> Il valore predefinito è 0.<br/></td>
</tr>
<tr class="odd">
<td><strong>BITSServerNotificationURL</strong> Tipo di dati: <strong>Stringa</strong><br/></td>
<td>facoltativo. Contiene l'URL dell'applicazione server in cui BITS invia il file di caricamento. È necessario specificare un URL se il valore della <strong>proprietà BITSServerNotificationType</strong> è 1 o 2. L'URL è limitato a 2.200 caratteri, senza includere il carattere di terminazione Null. L'URL deve essere un URL HTTP. BITS non supporta gli URL di notifica HTTPS.<br/> Se l'URL non è disponibile al momento del caricamento, BITS ripeterà il caricamento fino a quando non esiste l'URL di notifica o fino alla scadenza del periodo di ripetizione dei tentativi.<br/> Si noti che se il nome remoto specificato nel processo contiene una stringa di query, la stringa di query viene aggiunta all'URL specificato. Ad esempio, se il nome remoto contiene e si specifica l'impostazione https://myserver/myvdir/subdir/file.asp?ACCOUNT=86433 <strong>BITSServerNotificationURL</strong> come https://otherserver/myvdir2/bag.asp , l'URL a cui BITS invia è https://otherserver/myvdir2/bag.asp?ACCOUNT=86433 .<br/> Se l'URL originale è e l'URL di notifica è https://myserver/myvdir/file.txt myasp.asp, BITS usa http//myserver/myvdir/myasp.asp come URL di notifica.<br/> Se la parte relativa al percorso e al nome file dell'URL contiene caratteri Unicode non comuni alla tabella codici sia nel client che nel server, la conversione dell'URL avrà esito negativo nel server e il processo BITS verrà inserito nello stato di errore. Se la parte del server dell'URL contiene caratteri Unicode, è necessario codificare la parte del server usando <a href="/windows/win32/intl/handling-internationalized-domain-names--idns">i nomi</a> di dominio internazionalizzati (IDN).<br/></td>
</tr>
<tr class="even">
<td><strong>BITSHostId</strong> Tipo di dati: <strong>Stringa</strong><br/></td>
<td>Impostare questa proprietà se l'installazione del server è una Web farm che non usa l'archiviazione condivisa.<br/> Specificare il nome del server o l'indirizzo IP del server a cui riconnettersi dopo l'interruzione del processo di caricamento. In genere, si specifica il nome del server che si sta configurando. L'URL è limitato a 300 caratteri, senza includere il carattere di terminazione Null.<br/> Se non si specifica questa proprietà e il processo di caricamento viene interrotto, è possibile che BITS riprendi il processo in un altro server della farm. Tuttavia, il server precedente contiene ancora il file di caricamento parziale da prima dell'interruzione. BITS rimuove il file parziale dopo la scadenza di <strong>BITSSessionTimeout.</strong><br/>
<blockquote>
[!Note]<br />
Non usare la proprietà <strong>BITSHostId</strong> se SSL viene usato in una Web farm che usa Bilanciamento carico di rete (NLB) o nomi DNS con più indirizzi IP, a meno che non si includano il nome del cluster e i singoli nomi di server nel certificato. Se il nome del server specificato in <strong>BITSHostId</strong> non corrisponde al nome comune nel certificato, il processo avrà esito negativo. Per Bilanciamento carico di rete impostare invece il <a href="/previous-versions/tn-archive/bb687542(v=technet.10)">parametro Affinity</a> su <strong>Single</strong> per assicurarsi che il client comunichi con lo stesso server in futuro.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSHostIdFallbackTimeout</strong> Tipo di dati: <strong>DWORD</strong><br/></td>
<td>Numero di secondi per cui il client BITS tenta di riconnettersi al nome del server <strong>BITSHostId</strong> prima di ripristinare il nome host specificato nel nome file remoto del processo. Il timer inizia quando BITS non è in grado di connettersi al server <strong>BITSHostId.</strong> Il timer viene reimpostato quando il client si connette correttamente al server.<br/> Si noti che il valore di nessun timeout di stato del processo (vedere <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout"><strong>IBackgroundCopyJob::SetNoProgressTimeout</strong></a>) deve essere più lungo di questo valore di timeout. In caso contrario, il processo avrà esito negativo prima della scadenza del valore di timeout di fallback.<br/> Impostare questa proprietà solo se si imposta la <strong>proprietà BITSHostId.</strong><br/> Il valore predefinito è 86.400 (1 giorno).<br/></td>
</tr>
<tr class="even">
<td><strong>BITSAllowOverwrites</strong> Tipo di dati: <strong>Integer</strong><br/></td>
<td>Indica se un file di caricamento può sovrascrivere un file esistente con lo stesso nome. Il file di caricamento sovrascrive il file esistente se <strong>BITSAllowOverwrites</strong> è 1.<br/> Il valore predefinito è 0.<br/> <strong>IIS 6.0:</strong> È possibile impostare questa proprietà solo da uno script. Non è possibile impostarla usando la pagina delle proprietà dell'estensione BITS nell'interfaccia utente di IIS.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSCleanupUseDefault</strong> Tipo di dati: <strong>Boolean</strong><br/></td>
<td>Indica se l'attività di pulizia usa le pianificazioni predefinite. Per impostazione predefinita, l'attività di pulizia viene eseguita ogni 12 ore.<br/> Impostare su 1 per usare la pianificazione predefinita. in caso contrario, 0 per specificare una pianificazione.<br/> Per specificare una pianificazione, usare le <strong>proprietà BITSCleanupCount</strong> e <strong>BITSCleanupUnits.</strong><br/> L'attività di pulizia pulisce la directory virtuale eliminando i processi che non sono stati modificati entro il periodo di timeout della sessione (vedere <strong>BITSSessionTimeout</strong>).<br/> Il valore predefinito è 1. Usare la pianificazione predefinita.<br/> <strong>IIS 6.0:</strong> Non supportato.<br/></td>
</tr>
<tr class="even">
<td><strong>BITSCleanupCount</strong> Tipo di dati: <strong>Integer</strong><br/></td>
<td>Specifica l'intervallo di attesa tra l'esecuzione dell'attività di pulizia. L'intervallo che è possibile specificare dipende dalle unità. Per i possibili valori di intervallo, vedere la <strong>proprietà BITSCleanupUnits.</strong><br/> Questa proprietà viene ignorata <strong>se BITSCleanupUseDefault</strong> è 0.<br/> <strong>IIS 6.0:</strong> Non supportato.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSCleanupUnits</strong> Tipo di dati: <strong>Integer</strong><br/></td>
<td>Specifica le unità per l'intervallo di pulizia specificato nella <strong>proprietà BITSCleanupCount.</strong> Questa proprietà viene ignorata <strong>se BITSCleanupUseDefault</strong> è 0.<br/> I valori possibili sono:<dl> 0: le unità sono minuti. I valori possibili sono da 1 a 60.<br />
1: le unità sono ore. Questo è il valore predefinito. I valori possibili sono da 1 a 24.<br />
2: le unità sono giorni. I valori possibili sono da 1 a 360.<br />
</dl> <br/> <strong>IIS 6.0:</strong> Non supportato.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>BITSNumberOfSessionsLimit</strong> Tipo di dati: <strong>Integer</strong><br/></td>
<td>Limita il numero di sessioni di caricamento che possono esistere contemporaneamente per un utente. Se il numero di sessioni per un utente è superiore a questo limite, quando viene eseguita l'attività di pulizia verranno eliminate le sessioni più recenti finché il numero di sessioni per l'utente non sarà inferiore al limite.<br/> Il valore predefinito è 50 sessioni.<br/> <strong>IIS 6.0:</strong> Non supportato.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSSessionLimitEnable</strong> Tipo di dati: <strong>Boolean</strong><br/></td>
<td>Indica se BITS limita il numero di sessioni di caricamento per utente. Se l'impostazione non è presente o è 0, il limite è disabilitato.<br/> Per specificare il limite, impostare la <strong>proprietà BITSNumberOfSessionsLimit.</strong><br/> Il valore predefinito è 1.<br/> <strong>IIS 6.0:</strong> Non supportato.<br/> <br/></td>
</tr>
</tbody>
</table>



 

Nell'esempio seguente viene illustrato come impostare le proprietà dell'estensione IIS BITS Windows Host script. Se la directory virtuale punta a una condivisione remota, impostare anche le proprietà **IIS UNCUserName** **e UNCPassword.**


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



 

