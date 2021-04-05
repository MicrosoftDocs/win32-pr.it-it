---
description: A partire da Windows Vista, il servizio WMI non utilizza i file di log WMI. USA invece Event Tracing for Windows (ETW) ed eventi sono disponibili tramite Visualizzatore eventi o lo strumento da riga di comando wevtutil.
ms.assetid: bb6401e8-caf7-4f39-ab64-b7532723ce9a
ms.tgt_platform: multiple
title: Traccia dell'attività WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14371a4f18b81019073cd2b428500b12385719e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758006"
---
# <a name="tracing-wmi-activity"></a>Traccia dell'attività WMI

A partire da Windows Vista, il servizio WMI non utilizza i [file di log WMI](wmi-log-files.md). USA invece [Event Tracing for Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) ed eventi sono disponibili tramite **Visualizzatore eventi** o lo strumento da riga di comando wevtutil.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Recupero di eventi WMI tramite Visualizzatore eventi](#obtaining-wmi-events-through-event-viewer)
-   [Abilitazione della traccia WMI al prompt dei comandi](#enabling-wmi-tracing-at-command-prompt)
-   [Uso della traccia WMI basata su WPP](#using-wpp-based-wmi-tracing)
-   [Argomenti correlati](#related-topics)

## <a name="obtaining-wmi-events-through-event-viewer"></a>Recupero di eventi WMI tramite Visualizzatore eventi

Il file WMITracing. log contiene gli eventi tracciati da WMI. Tuttavia, si tratta di un file binario. Per visualizzare questi eventi in un formato leggibile dagli utenti, utilizzare il **Visualizzatore eventi**.

Per impostazione predefinita, gli eventi WMI non vengono tracciati. In questa procedura viene descritto come utilizzare **Visualizzatore eventi** per abilitare la traccia eventi WMI e individuare gli eventi WMI. È possibile eseguire le stesse operazioni tramite lo strumento da riga di comando wevtutil.

**Per visualizzare gli eventi WMI in Visualizzatore eventi**

1.  Aprire **Visualizzatore eventi**. Dal menu **Visualizza** scegliere **Visualizza registri analitici e di debug**. Individuare il registro del canale di **traccia** per WMI in registri applicazioni e servizi \| \| attività Microsoft Windows \| WMI.
2.  Fare clic con il pulsante destro del mouse sul registro **traccia** e selezionare **proprietà log**. Fare clic sulla casella di controllo **Abilita registrazione** per avviare la traccia eventi WMI. Per ulteriori informazioni sui canali, vedere [log eventi e canali nel registro eventi di Windows](/previous-versions//aa385225(v=vs.85)).
3.  Gli eventi WMI vengono visualizzati nella finestra evento per **WMI-Activity**. Fare doppio clic su un evento nell'elenco per visualizzare le informazioni dettagliate. È possibile visualizzare un evento in una **visualizzazione XML** o in un formato di **visualizzazione descrittivo** .

Nel campo **ID evento** viene visualizzato un valore che contiene le informazioni seguenti.

<dl> <dt>

<span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Evento 1
</dt> <dd>

Inizio della sequenza di eventi per un'operazione specifica. Una occorrenza per ogni sequenza.

I campi evento per un evento 1 sono:

-   **GroupOperationID** è un identificatore univoco usato per tutti gli eventi segnalati per un client specifico.
-   **OperationId** indica la sequenza di operazioni.
-   L' **operazione** specifica la connessione o la richiesta a WMI.
-   L' **utente** indica l'account che effettua una richiesta a WMI eseguendo uno script o CIM Studio.
-   **Spazio dei nomi** Mostra lo spazio dei nomi WMI a cui viene eseguita la connessione.

Uno script può ad esempio richiedere tutte le istanze di una classe WMI, ad esempio il [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service). La prima operazione può essere una connessione a WMI.

</dd> <dt>

<span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Evento 2
</dt> <dd>

Eventi che costituiscono l'operazione. Una o più occorrenze nella sequenza.

I campi evento per un evento 2 sono:

-   **GroupOperationID** indica la sequenza in cui si verifica l'evento.
-   **GroupOperationID** indica la sequenza in cui si verifica l'evento.
-   **ProviderName** indica il nome del provider che fornisce i dati.
-   **Path** è il percorso WMI dell'oggetto.

Ad esempio, l'operazione può essere un'enumerazione del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

<span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Evento 3
</dt> <dd>

Fine della sequenza di eventi per un'operazione specifica. Una occorrenza per ogni sequenza.

Viene visualizzato solo **GroupOperationID** .

</dd> </dl>

## <a name="enabling-wmi-tracing-at-command-prompt"></a>Abilitazione della traccia WMI al prompt dei comandi

È inoltre possibile abilitare la traccia eventi WMI tramite lo strumento da riga di comando wevtutil. Usare il comando seguente: **Wevtutil.exe SL Microsoft-Windows-WMI-Activity/Trace/e: true**. L'origine evento WMI è Microsoft-Windows-WMI. Per ulteriori informazioni su Wevtutil.exe, vedere [informazioni sul registro eventi di Windows](/previous-versions//aa382610(v=vs.85)).

## <a name="using-wpp-based-wmi-tracing"></a>Uso della traccia WMI basata su WPP

Nei sistemi operativi Windows a partire da Windows Vista, WMI crea un canale di traccia attivo durante il processo di avvio. Il nome del canale è la \_ sessione di traccia WMI \_ . Solo gli errori vengono registrati nel canale.

Il preprocessore di traccia software Windows (WPP) registra le informazioni in un file binario. Per leggere il file, è innanzitutto necessario convertirlo in un formato di testo leggibile. Per eseguire la traduzione, utilizzare uno strumento denominato tracefmt.exe dal [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) . Lo strumento richiede informazioni archiviate in alcuni file associati. I file si trovano nella directory% SystemRoot% \\ system32 \\ WBEM \\ MDF e hanno l'estensione del nome di file MDF. Lo strumento richiede effettivamente un solo file con estensione MDF. Il file viene creato concatenando tutti i file con estensione MDF in un altro file con estensione MDF. Per ulteriori informazioni sui file con estensione MDF, vedere [file di formato del messaggio di traccia](/windows-hardware/drivers/devtest/trace-message-format-file).

Dopo l'installazione di [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) per ottenere la tracelog.exe e tracefmt.exe gli strumenti da riga di comando, eseguire la procedura seguente per raccogliere una traccia WMI basata su WPP.

**Per visualizzare una traccia WMI basata su WPP**

1.  Per creare il singolo file con estensione MDF, aprire una finestra del prompt dei comandi con privilegi elevati e passare alla directory% SystemRoot% \\ system32 \\ WBEM \\ MDF.

2.  Digitare **copy/y% SystemRoot% \\ system32 \\ WBEM \\ MDF \\ \* . MDF% SystemRoot% \\ system32 \\ WBEM \\ MDF \\ WMI. MDF**. Verrà creato un file denominato WMI. mdf che include il contenuto di tutti gli altri file con estensione MDF.

3.  Digitare **tracelog-Flush WMI \_ trace \_ Session**. I buffer WPP sul disco vengono scaricati.
4.  Digitare il **prefisso del formato di traccia \_ \_ = \[ %9! d! \] %8! 04X!. %3! 04X!. %3! 04X!:: %4! s! \[ %1! s! \] (%! COMPname!:%! FUNC!: %2! s!)**. Lo strumento tracefmt aggiunge alcune informazioni predefinite a ogni messaggio di traccia. È possibile configurare le informazioni incluse impostando la variabile di \_ \_ ambiente prefisso formato traccia. Per ulteriori informazioni sulla sintassi utilizzata, vedere il [prefisso del messaggio di traccia](https://msdn.microsoft.com/library/aa139695.aspx).
5.  Digitare **tracefmt-MDF% SystemRoot% \\ system32 \\ WBEM \\ MDF \\ wmi. MDF-o OUTPUT.TXT% SystemRoot% \\ system32 \\ \\ log \\ WMITracing. log**. In questo modo viene eseguita la conversione dal formato binario al formato testo leggibile.
6.  Digitare **notepad% systemroot% \\ system32 \\ WBEM \\ MDF \\OUTPUT.TXT**. Il file di traccia verrà aperto nel blocco note.

Di seguito sono riportate alcune altre attività correlate a WPP che può essere necessario eseguire.

**Per arrestare la traccia WMI basata su WPP**

-   Digitare **tracelog-stop WMI \_ trace \_ Session**.

**Per avviare la traccia WMI basata su WPP**

-   Digitare **tracelog-Start WMI \_ trace \_ Session-GUID \# 1FF6B227-2CA7-40F9-9A66-980EADAA602E-RT-Level 5-flag 0x7-f Trace. CONTENITORE** di

**Windows Vista:** Per impostazione predefinita, la traccia WMI basata su WPP è impostata sul livello 2, che include solo i messaggi di errore. Per includere anche i messaggi informativi, impostare il livello su 4. Per impostazione predefinita, tutte le aree di WMI sono tracciate. Sono disponibili tre aree distinte che è possibile tracciare: Core (flag = 0x1), ESS (flag = 0x2) e prov (flag = 0x4). Nel comando di avvio sopra riportato, il **flag 0x7** causa la traccia di tutte e tre le aree.

**Windows 7:** Per impostazione predefinita, la traccia WMI basata su WPP è disabilitata e impostata sul livello 0. Per utilizzare la traccia WMI basata su WPP, questa funzionalità deve essere abilitata e impostata su livello 2 per i messaggi di errore o livello 4 per i messaggi di errore e informativi.

**Per elencare tutte le sessioni di traccia WPP**

-   Digitare **tracelog-l**.

**Per elencare le informazioni sulla sessione di traccia WMI WPP**

-   Digitare **tracelog-l \| findstr/i "WMI \_ Trace"**.

**Per visualizzare i parametri della sessione di traccia WMI WPP**

-   Digitare **tracelog-q WMI \_ trace \_ Session**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi WMI](wmi-troubleshooting.md)
</dt> <dt>

[File di log WMI](wmi-log-files.md)
</dt> </dl>

 

 
