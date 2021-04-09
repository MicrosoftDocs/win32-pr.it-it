---
description: Per eseguire il test e il debug delle implementazioni del gestore di protocollo è fondamentale comprendere come vengono avviati i gestori di protocollo.
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: Debug di gestori di protocollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d59c0c7915f9bbf84a80091408ba88a9a75ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128515"
---
# <a name="debugging-protocol-handlers"></a>Debug di gestori di protocollo

Per eseguire il test e il debug delle implementazioni del gestore di protocollo è fondamentale comprendere come vengono avviati i gestori di protocollo.

Questo argomento è organizzato nel modo seguente:

-   [Informazioni sui gestori di protocollo di debug](#about-debugging-protocol-handlers)
-   [Impostazione del debug](#setting-up-debugging)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="about-debugging-protocol-handlers"></a>Informazioni sui gestori di protocollo di debug

Il processo SearchIndexer (searchindexer.exe) avvia una copia del processo SearchProtocolHost (SearchProtocolHost.exe) nel contesto di sistema e in un'altra copia nel contesto utente. Quindi, i gestori del protocollo vengono caricati nel processo SearchProtocolHost in base alle esigenze. Non vengono scaricati finché il servizio di ricerca non viene arrestato. La stessa istanza di un gestore di protocollo viene riutilizzata un numero qualsiasi di volte mentre il servizio è in esecuzione.

I processi SearchIndexer e SearchProtocolHost comunicano spesso durante l'indicizzazione. Se si sospende o si arresta il processo SearchProtocolHost per eseguire il debug, il SearchIndexer avvierà un nuovo processo SearchProtocolHost, invalidando la sessione di debug. Inoltre, se si connette il debugger direttamente al processo SearchProtocolHost, è possibile interrompere l'ereditarietà del handle da searchindexer.exe a searchprotocolhost.exe e i due processi non saranno in grado di comunicare.

Per evitare questi problemi, è necessario inviare una notifica al servizio di ricerca di cui si sta eseguendo il debug ed è necessario associare il debugger al processo SearchIndexer con le istruzioni per eseguire il debug dei processi figlio, come descritto di seguito.

## <a name="setting-up-debugging"></a>Impostazione del debug

Per configurare il debug per il gestore di protocollo, attenersi alla procedura riportata di seguito.

1.  Inviare una notifica al servizio di ricerca di cui si sta eseguendo il debug impostando il valore DebugFilters su 1 nel registro di sistema:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  Connetti un debugger usando la chiave del registro di sistema opzioni di esecuzione file di immagine:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    Nella tabella seguente sono descritte le opzioni per un debugger di esempio.

    

    **Esempio di uso del debugger NTSD** debugger *= C: \\ Debuggers \\ntsd.exe-odGx-c: "sxe ld mydll.dll; g"*   <br/>

3.  Riavviare searchindexer.exe nel debugger usando compmgmt. msc, Services. msc o una finestra di comando con comandi simili ai seguenti:
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

Per distinguere tra un processo SearchProtocolHost in esecuzione nel contesto di sistema e uno in esecuzione nel contesto utente, è possibile esaminare le stringhe di ambiente. Con ntsd.exe, ad esempio, è possibile usare il comando Extension **! PEB** per visualizzare una visualizzazione formattata delle informazioni nel blocco dell'ambiente di elaborazione (PEB).

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per informazioni sulla creazione di gestori, vedere la pagina relativa alla [registrazione delle estensioni della shell](../shell/reg-shell-exts.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>**Concetti concettuali**</dt> <dt><a href="-search-3x-wds-phaddins.md">sullo sviluppo</a></dt> di gestori di protocollo <dt><a href="-search-3x-wds-extidx-prot-implementing.md">informazioni sui gestori di protocollo</a></dt> che <dt><a href="-search-3x-wds-notifyingofchanges.md">inviano notifiche all'indice delle modifiche aggiunta di</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">icone e menu di scelta rapida</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">esempio di codice: estensioni shell per gestori di protocollo</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">creazione di un connettore di ricerca per un gestore di protocollo</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">installazione e registrazione dei gestori di protocollo</a></dt> </dl>

 

 
