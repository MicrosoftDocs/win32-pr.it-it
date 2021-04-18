---
title: Problemi di installazione e caricamento pagina
description: Problemi di installazione e caricamento pagina
ms.assetid: 1611c3f1-0411-4631-a64c-e7637fc7edd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9775e6a9afa957867d5279b9faaf506e32757f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "106299533"
---
# <a name="installation-and-page-loading-problems"></a>Problemi di installazione e caricamento pagina

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

### <a name="when-i-attempt-to-install-microsoft-agent-on-microsoft-windows-nt-i-get-a-message-indicating-that-i-need-to-be-an-administrator"></a>Quando si tenta di installare Microsoft Agent in Microsoft Windows NT, viene ricevuto un messaggio che indica che è necessario essere un amministratore.

Poiché Microsoft Agent scrive i file nella directory di sistema durante l'installazione di, è necessario disporre dei privilegi di amministratore (non utente) per l'installazione.

### <a name="when-i-attempt-to-install-microsoft-agent-i-get-one-of-the-following-errors-process-regsvr32-s-windowsmsagentagentctldll-error-while-creating-this-file-cannot-find-this-file-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows-a-required-dll-msvcrtdll-was-not-found-error-creating-process-cwindowsmsagentagentsvrexe-regserver-reason-one-of-the-library-files-needed-to-run-this-application-cannot-be-found-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows"></a>Quando si tenta di installare Microsoft Agent, si verifica uno degli errori seguenti: processo (regsvr32/s Windows \\ msagent \\AgentCtl.dll). Errore durante la creazione del file. Il file non è stato trovato. Nota: il percorso della directory citato nel messaggio di errore varia a seconda della modalità di installazione di Windows. Impossibile trovare una DLL obbligatoria MSVCRT.DLL. Errore durante la creazione del processo <c: \\ Windows \\ msagent \\agentsvr.exe/regserver>. Motivo: Impossibile trovare uno dei file di libreria necessari per eseguire l'applicazione. Nota: il percorso della directory citato nel messaggio di errore varia a seconda della modalità di installazione di Windows.

L'installazione di Microsoft Agent richiede l'installazione corretta di Regsvr32.exe, Msvcrt.dll (la libreria di runtime Microsoft C) e le DLL OLE aggiornate. Vedere aggiornamento DCOM: ( <https://docs.microsoft.com/openspecs/windows_protocols/ms-dcom/4a893f3d-bd29-48cd-9f43-d9777a4415b0> ). Il modo migliore per assicurarsi che tutti i file di sistema corretti siano presenti è installare [Microsoft Internet Explorer 4,0](https://www.microsoft.com/ie/download) o versione successiva.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-a-scripting-error-vbscript-runtime-error-object-required"></a>Quando si tenta di caricare una pagina di cui è stato eseguito lo script per Microsoft Agent, viene ricevuto un errore di script: "errore di runtime VBScript, oggetto obbligatorio".

Una delle condizioni seguenti può causare la visualizzazione del messaggio:

-   Le opzioni di sicurezza per Microsoft Internet Explorer devono essere impostate per abilitare i controlli ActiveX e i plug-in. Controllare la pagina sicurezza del browser. In Microsoft Internet Explorer aprire il menu Visualizza, scegliere Opzioni, fare clic sulla scheda sicurezza e verificare che la casella di controllo Abilita controlli ActiveX e Plug-Ins sia selezionata.
-   Si esegue un sistema Windows 9x o Windows NT a doppio avvio ed è stato installato Microsoft Agent in un sistema operativo, ma si sta tentando di accedere alla pagina dall'altro sistema operativo. Sebbene i sistemi operativi possano condividere directory e file, le informazioni del registro di sistema utilizzate da Microsoft Agent non sono condivise, quindi è necessario installare Microsoft Agent nel sistema operativo utilizzato per accedere alle pagine Web con il carattere.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-nothing-happens"></a>Quando si tenta di caricare una pagina con script per Microsoft Agent, non viene eseguita alcuna operazione.

Questo problema può verificarsi in presenza di una delle condizioni seguenti:

-   Controllare le opzioni di sicurezza del browser. Il browser deve essere impostato in modo da consentire il caricamento di script ActiveX e la riproduzione di controlli ActiveX.
-   Se si accede a pagine con script Microsoft Agent e si utilizza Microsoft Internet Explorer, è necessario disporre della versione 3,02 o successiva (scaricare la versione più recente di Internet Explorer all'indirizzo [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) <https://www.microsoft.com/windows/ie/> ). In Microsoft Internet Explorer aprire il menu Visualizza, scegliere Opzioni, fare clic sulla scheda sicurezza e selezionare tutte le caselle di controllo contenuto attivo.
-   Questo errore può essere causato anche da un'applet Java nella pagina. Per eseguire Microsoft Agent nella stessa pagina di un'applet Java è richiesta la versione 2,0 della macchina virtuale (VM) Microsoft. Per ulteriori informazioni, vedere le [domande frequenti su programmazione/scripting](programming-scripting-faq.md).

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-unable-to-initialize-microsoft-agent"></a>Quando si tenta di caricare una pagina di cui è stato eseguito lo script per Microsoft Agent, viene ricevuto il messaggio "Impossibile inizializzare Microsoft Agent".

Questo problema si verifica in genere quando non si dispone di un agente Microsoft o di un altro controllo usato dalla pagina installato e scegliere No quando viene richiesto di installare il controllo. Provare ad aggiornare la pagina, anche se la pagina può funzionare solo se si installano tutti i componenti richiesti.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-the-component-has-been-digitally-signed-by-its-publisher-but-the-signature-does-not-match-the-component-it-is-possible-that-this-component-has-been-damaged-or-tampered-with-do-you-want-to-continue"></a>Quando si tenta di caricare una pagina con script per Microsoft Agent, viene ricevuto il messaggio "il componente è stato" firmato digitalmente "dal relativo server di pubblicazione, ma la firma non corrisponde al componente. È possibile che il componente sia stato danneggiato o manomesso? Continuare?"

Questo può essere visualizzato se si tenta di installare Microsoft Agent in Microsoft Internet Explorer 3,02. È possibile continuare con l'installazione o aggiornare il browser a Internet Explorer 4,0 o versione successiva.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-using-netscape-navigator-or-other-internet-browsers-i-get-errors"></a>Quando si tenta di caricare una pagina con script per Microsoft Agent usando Netscape Navigator (o altri browser Internet), si verificano errori.

Microsoft Agent viene implementato utilizzando le interfacce ActiveX. È possibile utilizzarlo solo con un browser (ad esempio Microsoft Internet Explorer) che supporta l'incorporamento di oggetti ActiveX tramite script in una pagina e solo nei sistemi che eseguono Microsoft Windows 95, Windows 98 e Windows NT 4,0 (o versione successiva). Se non si utilizza Microsoft Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ), rivolgersi al fornitore del browser per ulteriori informazioni sul supporto ActiveX.

 

 




