---
description: La sessione di traccia eventi del logger globale registra gli eventi che si verificano nelle fasi iniziali del processo di avvio del sistema operativo.
ms.assetid: 1462bbef-ef32-4053-9930-5b4a0ab46b47
title: Configurazione e avvio della sessione Global Logger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8692e1f7321acc163e48cda7e3323f3d24adc1c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980122"
---
# <a name="configuring-and-starting-the-global-logger-session"></a>Configurazione e avvio della sessione Global Logger

La sessione di traccia eventi del logger globale registra gli eventi che si verificano nelle fasi iniziali del processo di avvio del sistema operativo. Le applicazioni e i driver di dispositivo possono usare la sessione Global Logger per acquisire tracce prima che l'utente effettui l'accesso. Si noti che alcuni driver di dispositivo, ad esempio i driver dei dispositivi disco, non vengono caricati nel momento in cui inizia la sessione Global Logger.

> [!Note]  
> Se si sta creando una sessione di logger globale in Windows Vista, è consigliabile creare invece una [sessione di autologger](configuring-and-starting-an-autologger-session.md) .

 

Usare il registro di sistema per configurare la sessione globale del logger. Aggiungere la chiave **GlobalLogger** alla seguente chiave del registro di sistema, se non è già presente:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
```

Nella tabella seguente vengono descritti i valori che è possibile definire per la chiave **GlobalLogger** . Per specificare questi valori del registro di sistema, è necessario disporre dei privilegi di amministratore. I valori del registro di sistema influiscono su tutti i provider che registrano gli eventi nella sessione globale del logger. Il valore **iniziale** è l'unico valore necessario per avviare la sessione globale del logger. tutti gli altri valori hanno impostazioni predefinite che vengono usate se il valore non è presente nel registro di sistema. In genere, è consigliabile usare i valori predefiniti. Se si specifica un valore che ETW non supporta, ETW eseguirà l'override del valore.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Tipo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Inizia</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Impostare questo valore su 1 (on) per avviare la sessione del logger globale al successivo avvio del sistema. Per arrestare l'avvio della sessione, impostare questo valore su 0 (disattivato). <br/></td>
</tr>
<tr class="even">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Dimensioni di ogni buffer, in kilobyte. Questo valore deve essere minore di un megabyte. ETW usa le dimensioni della memoria fisica per calcolare questo valore. <br/></td>
</tr>
<tr class="odd">
<td><strong>ClockType</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Timer da usare per registrare il timestamp per ogni evento.
<ul>
<li>1 = valore del contatore delle prestazioni (alta risoluzione)</li>
<li>2 = timer di sistema</li>
<li>3 = contatore cicli CPU</li>
</ul>
Per una descrizione di ogni tipo di orologio, vedere il membro <strong>ClientContext</strong> di <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.<br/> Il valore predefinito è 1 (valore del contatore delle prestazioni) in Windows Vista e versioni successive. Prima di Windows Vista, il valore predefinito è 2 (timer di sistema).<br/></td>
</tr>
<tr class="even">
<td><strong>EnableKernelFlags</strong></td>
<td><strong>REG_BINARY</strong></td>
<td>Utilizzare questo valore per abilitare uno o più provider kernel. Se si abilitano i provider del kernel, la sessione Global Logger si rinominerà al logger del kernel NT all'avvio. Per i valori possibili, vedere il membro <strong>EnableFlags</strong> di <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>Filecounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Numero di file di log di traccia degli eventi generati dalle sessioni di logger globali. Questo valore viene incrementato dal sistema fino a quando non viene raggiunto il valore di <strong>FileMax</strong>. Reimposta quindi il valore su 0. Questo contatore impedisce al sistema di sovrascrivere un file di log di traccia globale del logger. <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Numero massimo di file di log di traccia eventi consentiti nel sistema. Quando il numero di log di traccia raggiunge il valore massimo specificato, il sistema inizia a sovrascrivere i log, a partire dal meno recente. <br/> Se il file di log specificato in <strong>filename</strong> esiste, ETW aggiunge il valore <strong>filecounter</strong> al nome del file. Se, ad esempio, viene utilizzato il nome del file di log predefinito, il form è%SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.NNNN. <br/> Il valore predefinito è 0, ovvero non esiste alcun valore massimo. <br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Percorso completo del file di log. Il percorso di questo file deve esistere. Il file di log è un file di log sequenziale. Si noti che tutti i provider che scrivono eventi nella sessione Global Logger scrivono gli eventi in questo file di log. Il percorso è limitato a 1024 caratteri. Se <strong>filename</strong> non è specificato, gli eventi vengono scritti in%SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl. <strong>Prima di Windows Vista:</strong> Il file predefinito è%SystemRoot%\System32\LogFiles\WMI\Trace.log.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Con quale frequenza, in secondi, i buffer di traccia vengono scaricati forzatamente. Il tempo di svuotamento minimo è 1 secondo. Questo svuotamento forzato è in aggiunta allo scaricamento automatico che si verifica quando un buffer è pieno e quando la sessione di traccia viene arrestata. <br/> Per il caso di un logger in tempo reale, un valore pari a zero (valore predefinito) indica che il tempo di scaricamento verrà impostato su 1 secondo. Un logger in tempo reale è quando <strong>LogFileMode</strong> è impostato su <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> Il valore predefinito è 0. Per impostazione predefinita, i buffer vengono scaricati solo quando sono pieni. <br/></td>
</tr>
<tr class="odd">
<td><strong>LogFileMode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Specifica le opzioni della sessione di log. Per i valori, vedere <a href="logging-mode-constants.md">costanti della modalità di registrazione</a>. Questi valori sono supportati in Windows Vista e versioni successive. <br/></td>
</tr>
<tr class="even">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Numero massimo di buffer da allocare. In genere, questo valore è il numero minimo di buffer più venti. ETW usa le dimensioni del buffer e le dimensioni della memoria fisica per calcolare questo valore. Questo valore deve essere maggiore o uguale al valore di <strong>MinimumBuffers</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Dimensione massima, in megabyte, del file di log di traccia eventi. Per impostazione predefinita, non sono disponibili dimensioni massime del file.<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Numero minimo di buffer da allocare quando viene avviata la sessione globale del logger. Il numero minimo di buffer che è possibile specificare è costituito da due buffer per processore. Ad esempio, in un computer a processore singolo, il numero minimo di buffer è due. <br/> Il valore predefinito in un sistema a processore singolo è 0x3.<br/></td>
</tr>
<tr class="odd">
<td><strong>Status</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Stato di avvio del logger globale. Se non è stato possibile avviare il logger globale, il valore di questa chiave è il codice di errore Win32 appropriato. Se il logger globale è stato avviato correttamente, il valore di questa chiave è ERROR_SUCCESS (0).<br/></td>
</tr>
</tbody>
</table>



 

Dopo che il registro di sistema è stato modificato e il computer è stato riavviato, la sessione globale del logger viene avviata automaticamente e viene utilizzata come qualsiasi altra sessione con un'unica eccezione: si utilizza l' \_ \_ \_ handle costante ID logger globale WMI (definito in Wmistr. h) per fare riferimento alla sessione del logger globale. Questa costante può essere utilizzata come argomento per qualsiasi funzione di traccia eventi che accetta un handle di sessione. In funzioni che accettano un nome di sessione, usare il \_ nome del logger globale \_ .

Il controller di logger globale non chiama la funzione [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) per abilitare i provider. Il provider è responsabile di determinare se la sessione globale del logger è stata avviata e quindi abilitata autonomamente.

Per determinare se la sessione del logger globale è stata avviata, è possibile chiamare la funzione [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) , impostando *SessionHandle* sull' \_ \_ ID logger globale WMI \_ e *ControlCode* sulla query di **\_ controllo della traccia \_ \_ eventi**. Se la chiamata **ControlTrace** ha esito positivo, la sessione globale del logger esiste e il provider può abilitare se stesso e registrare gli eventi nella sessione globale del logger (la funzione **CONTROLTRACE** restituisce l'errore dell' \_ \_ istanza WMI \_ non \_ trovata se il logger globale non è attivo).

In genere, il controller è responsabile del passaggio dei flag di abilitazione e del livello al provider quando Abilita il provider, ma poiché il controller di logger globale non Abilita il provider, è responsabilità del provider passare le informazioni a se stesso, se necessario.

La sessione del logger globale è una risorsa limitata e deve essere usata in modo sporadico. I servizi che vogliono acquisire informazioni durante il processo di avvio devono considerare l'aggiunta della logica del controller a se stessa, anziché usare la sessione globale del logger.

Per informazioni dettagliate sull'avvio di una sessione di traccia eventi, vedere [configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md).

Per informazioni dettagliate sull'avvio di una sessione di logger privata, vedere [configurazione e avvio di una sessione di logger privati](configuring-and-starting-a-private-logger-session.md).

Per informazioni dettagliate sull'avvio di una sessione del logger di kernel NT, vedere [configurazione e avvio della sessione del logger di kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md).

