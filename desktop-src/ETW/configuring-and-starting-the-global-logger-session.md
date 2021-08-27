---
description: La sessione di traccia degli eventi del logger globale registra gli eventi che si verificano nelle prime fasi del processo di avvio del sistema operativo.
ms.assetid: 1462bbef-ef32-4053-9930-5b4a0ab46b47
title: Configurazione e avvio della sessione del logger globale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a928cba5eb782ca4a57f7dba4776de79f42d7af
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477047"
---
# <a name="configuring-and-starting-the-global-logger-session"></a>Configurazione e avvio della sessione del logger globale

La sessione di traccia degli eventi del logger globale registra gli eventi che si verificano nelle prime fasi del processo di avvio del sistema operativo. Le applicazioni e i driver di dispositivo possono usare la sessione global Logger per acquisire tracce prima che l'utente eseere connesso. Si noti che alcuni driver di dispositivo, ad esempio i driver di dispositivo del disco, non vengono caricati al momento dell'avvio della sessione del logger globale.

> [!Note]  
> Se si crea una sessione del logger globale in Windows Vista, è consigliabile creare una [sessione di AutoLogger.](configuring-and-starting-an-autologger-session.md)

 

Usare il Registro di sistema per configurare la sessione del logger globale. Aggiungere la **chiave GlobalLogger** alla chiave del Registro di sistema seguente, se non è già presente:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
```

Nella tabella seguente vengono descritti i valori che è possibile definire per la **chiave GlobalLogger.** Per specificare questi valori del Registro di sistema, è necessario disporre dei privilegi di amministratore. I valori del Registro di sistema influiscono su tutti i provider che registrano gli eventi nella sessione del logger globale. Il **valore Start** è l'unico valore necessario per avviare la sessione del logger globale. Tutti gli altri valori hanno impostazioni predefinite che vengono usate se il valore non è presente nel Registro di sistema. In genere, è consigliabile usare i valori predefiniti. Se si specifica un valore che ETW non può supportare, ETW eseguirà l'override del valore.




| valore | Tipo | Descrizione | 
|-------|------|-------------|
| <strong>Inizia</strong> | <strong>REG_DWORD</strong> | Impostare questo valore su 1 (on) per avviare la sessione del logger globale al successivo avvio del sistema. Per arrestare l'avvio della sessione, impostare questo valore su 0 (disattivato). <br /> | 
| <strong>BufferSize</strong> | <strong>REG_DWORD</strong> | Dimensioni di ogni buffer, in kilobyte. Questo valore deve essere minore di un megabyte. ETW usa le dimensioni della memoria fisica per calcolare questo valore. <br /> | 
| <strong>ClockType</strong> | <strong>REG_DWORD</strong> | Timer da utilizzare per la registrazione del timestamp per ogni evento.<ul><li>1 = Valore del contatore delle prestazioni (risoluzione elevata)</li><li>2 = Timer di sistema</li><li>3 = contatore del ciclo cpu</li></ul>Per una descrizione di ogni tipo di orologio, vedere il <strong>membro ClientContext</strong> <a href="wnode-header.md"><strong>di WNODE_HEADER</strong></a>.<br /> Il valore predefinito è 1 (valore del contatore delle prestazioni) Windows Vista e versioni successive. Prima di Windows Vista, il valore predefinito è 2 (timer di sistema).<br /> | 
| <strong>EnableKernelFlags</strong> | <strong>REG_BINARY</strong> | Usare questo valore per abilitare uno o più provider del kernel. Se si abilitano i provider del kernel, la sessione global logger verrà rinominata in NT Kernel Logger all'avvio. Per i valori possibili, vedere il <strong>membro EnableFlags</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>di EVENT_TRACE_PROPERTIES</strong></a>.<br /> | 
| <strong>FileCounter</strong> | <strong>REG_DWORD</strong> | Numero di file di log di traccia eventi generati dalle sessioni del logger globale. Il sistema incrementa questo valore fino a raggiungere il valore <strong>di FileMax</strong>. Quindi, reimposta il valore su 0. Questo contatore impedisce al sistema di sovrascrivere un file di log di traccia del logger globale. <br /> | 
| <strong>FileMax</strong> | <strong>REG_DWORD</strong> | Numero massimo di file di log di traccia eventi consentiti nel sistema. Quando il numero di log di traccia raggiunge il valore massimo specificato, il sistema inizia a sovrascrivere i log, a partire dal meno recente. <br /> Se il file di log specificato in <strong>FileName</strong> esiste, ETW aggiunge il <strong>valore FileCounter</strong> al nome file. Ad esempio, se viene usato il nome del file di log predefinito, il formato è %SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.NNNN. <br /> Il valore predefinito è 0, ovvero non è presente alcun valore massimo. <br /> | 
| <strong>FileName</strong> | <strong>REG_SZ</strong> | Percorso completo del file di log. Il percorso di questo file deve esistere. Il file di log è un file di log sequenziale. Si noti che tutti i provider che scrivono eventi nella sessione global Logger scrivono eventi in questo file di log. Il percorso è limitato a 1024 caratteri. Se <strong>FileName</strong> non viene specificato, gli eventi vengono scritti in %SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl. <strong>Prima di Windows Vista:</strong> Il file predefinito è %SystemRoot%\System32\LogFiles\WMI\Trace.log.<br /><br /> | 
| <strong>FlushTimer</strong> | <strong>REG_DWORD</strong> | Frequenza, in secondi, dello scaricamento forzato dei buffer di traccia. Il tempo minimo di scaricamento è di 1 secondo. Questo scaricamento forzato si aggiunge allo scaricamento automatico che si verifica quando un buffer è pieno e quando la sessione di traccia si arresta. <br /> Nel caso di un logger in tempo reale, il valore zero (valore predefinito) indica che il tempo di scaricamento verrà impostato su 1 secondo. Un logger in tempo reale è quando <strong>LogFileMode è</strong> impostato su <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br /> Il valore predefinito è 0. Per impostazione predefinita, i buffer vengono scaricati solo quando sono completi. <br /> | 
| <strong>LogFileMode</strong> | <strong>REG_DWORD</strong> | Specifica le opzioni della sessione di log. Per i valori, vedere <a href="logging-mode-constants.md">Costanti della modalità di registrazione</a>. Questi valori sono supportati in Windows Vista e versioni successive. <br /> | 
| <strong>MaximumBuffers</strong> | <strong>REG_DWORD</strong> | Numero massimo di buffer da allocare. In genere, questo valore è il numero minimo di buffer più 20. ETW usa le dimensioni del buffer e la dimensione della memoria fisica per calcolare questo valore. Questo valore deve essere maggiore o uguale al valore per <strong>MinimumBuffers</strong>.<br /> | 
| <strong>Maxfilesize</strong> | <strong>REG_DWORD</strong> | Dimensioni massime, in megabyte, del file di log della traccia eventi. Per impostazione predefinita, non esistono dimensioni massime del file.<br /> | 
| <strong>MinimumBuffers</strong> | <strong>REG_DWORD</strong> | Numero minimo di buffer da allocare all'avvio della sessione del logger globale. Il numero minimo di buffer che è possibile specificare è di due buffer per processore. In un computer a processore singolo, ad esempio, il numero minimo di buffer è due. <br /> Il valore predefinito in un sistema a processore singolo è 0x3.<br /> | 
| <strong>Status</strong> | <strong>REG_DWORD</strong> | Stato di avvio del logger globale. Se l'avvio del logger globale non è riuscito, il valore di questa chiave è il codice di errore Win32 appropriato. Se il logger globale è stato avviato correttamente, il valore di questa chiave è ERROR_SUCCESS (0).<br /> | 




 

Dopo che il Registro di sistema è stato modificato e il computer è stato riavviato, la sessione del logger globale viene avviata automaticamente e viene usata come qualsiasi altra sessione con un'eccezione: usare l'handle della costante WMI \_ GLOBAL \_ LOGGER ID (definito in Wmistr.h) per fare riferimento alla sessione \_ del logger globale. Questa costante può essere usata come argomento per qualsiasi funzione di traccia eventi che accetta un handle di sessione. Nelle funzioni che accettano un nome di sessione usare GLOBAL \_ LOGGER \_ NAME.

Il controller global logger non chiama la [**funzione EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) per abilitare i provider. Il provider è responsabile di determinare se la sessione del logger globale viene avviata e quindi attivata.

Per determinare se la sessione del logger globale viene avviata, è possibile chiamare la funzione [**ControlTrace,**](/windows/win32/api/evntrace/nf-evntrace-controltracea) impostando *SessionHandle* su WMI GLOBAL LOGGER ID e \_ \_ \_ *ControlCode* su **EVENT TRACE CONTROL \_ \_ \_ QUERY**. Se la chiamata **a ControlTrace** ha esito positivo, la sessione del logger globale esiste e il provider può abilitare se stesso e registrare gli eventi nella sessione del logger globale (la funzione **ControlTrace** restituisce ERROR WMI INSTANCE NOT FOUND se il logger globale non è \_ \_ \_ \_ attivo).

In genere, il controller è responsabile del passaggio dei flag di abilitazione e del livello al provider quando abilita il provider, ma poiché il controller del logger globale non abilita il provider, è responsabilità del provider passare queste informazioni a se stesso, se necessario.

La sessione del logger globale è una risorsa limitata e deve essere usata con moderità. I servizi che vogliono acquisire informazioni durante il processo di avvio devono prendere in considerazione l'aggiunta della logica del controller a se stessa anziché usare la sessione del logger globale.

Per informazioni dettagliate sull'avvio di una sessione di traccia eventi, vedere [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).

Per informazioni dettagliate sull'avvio di una sessione di logger privata, vedere [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).

Per informazioni dettagliate sull'avvio di una sessione di logger del kernel NT, vedere [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).

