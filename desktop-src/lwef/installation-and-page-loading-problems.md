---
title: Problemi di installazione e caricamento delle pagine
description: Problemi di installazione e caricamento delle pagine
ms.assetid: 1611c3f1-0411-4631-a64c-e7637fc7edd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3139a9224f88f49a31b1f71a981d1b49b3e42127
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481946"
---
# <a name="installation-and-page-loading-problems"></a>Problemi di installazione e caricamento delle pagine

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

### <a name="when-i-attempt-to-install-microsoft-agent-on-microsoft-windows-nt-i-get-a-message-indicating-that-i-need-to-be-an-administrator"></a>Quando si tenta di installare Microsoft Agent in Microsoft Windows NT, viene visualizzato un messaggio che indica che è necessario essere un amministratore.

Poiché Microsoft Agent scrive i file nella directory di sistema durante l'installazione, è necessario disporre dei privilegi di amministratore (non utente) per l'installazione.

### <a name="when-i-attempt-to-install-microsoft-agent-i-get-one-of-the-following-errors-process-regsvr32-s-windowsmsagentagentctldll-error-while-creating-this-file-cannot-find-this-file-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows-a-required-dll-msvcrtdll-was-not-found-error-creating-process-cwindowsmsagentagentsvrexe-regserver-reason-one-of-the-library-files-needed-to-run-this-application-cannot-be-found-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows"></a>Quando si prova a installare Microsoft Agent, viene visualizzato uno degli errori seguenti: Processo (Regsvr32 /s windows \\ msagent \\AgentCtl.dll). Errore durante la creazione del file. Impossibile trovare questo file. Nota: il percorso della directory citato nel messaggio di errore varia a seconda della modalità di Windows. Non è stata trovata MSVCRT.DLL dll necessaria. Errore durante la creazione del <c: \\ windows \\ msagent \\agentsvr.exe /regserver>. Motivo: impossibile trovare uno dei file di libreria necessari per eseguire l'applicazione. Nota: il percorso della directory citato nel messaggio di errore varia a seconda della modalità di Windows.

L'installazione di Microsoft Agent richiede l'installazione corretta di Regsvr32.exe, Msvcrt.dll (libreria di runtime di Microsoft C) e dll OLE aggiornate. Vedere Aggiornamento DCOM: ( <https://docs.microsoft.com/openspecs/windows_protocols/ms-dcom/4a893f3d-bd29-48cd-9f43-d9777a4415b0> ). Il modo migliore per assicurarsi che siano presenti tutti i file di sistema corretti è [installare Microsoft Internet Explorer 4.0](https://www.microsoft.com/ie/download) o versione successiva.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-a-scripting-error-vbscript-runtime-error-object-required"></a>Quando si tenta di caricare una pagina con script per Microsoft Agent, viene visualizzato un errore di scripting: "Errore di runtime VBScript, oggetto obbligatorio".

Una delle condizioni seguenti può causare la visualizzazione del messaggio:

-   Le opzioni di sicurezza per Microsoft Internet Explorer devono essere impostate per abilitare ActiveX e plug-in. Controllare la pagina di sicurezza del browser. In Microsoft Internet Explorer aprire il menu Visualizza, scegliere Opzioni, fare clic sul scheda Sicurezza e verificare che la casella di controllo Abilita controlli ActiveX e Plug-Ins sia selezionata.
-   Si esegue in un sistema Windows 9x o Windows NT ad avvio doppio ed è stato installato Microsoft Agent in un sistema operativo, ma si sta tentando di accedere alla pagina dall'altro sistema operativo. Anche se i sistemi operativi possono condividere directory e file, le informazioni del Registro di sistema usate da Microsoft Agent non sono condivise, pertanto è necessario installare Microsoft Agent nel sistema operativo usato per accedere alle pagine Web con script con il carattere .

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-nothing-happens"></a>Quando si tenta di caricare una pagina con script per Microsoft Agent, non accade nulla.

Ciò può verificarsi se esiste una delle condizioni seguenti:

-   Controllare le opzioni di sicurezza del browser. Il browser deve essere impostato per abilitare il caricamento ActiveX script e la riproduzione ActiveX controlli.
-   Se si accede a pagine con script con Microsoft Agent e si usa Microsoft Internet Explorer, è necessario avere la versione 3.02 o successiva (scaricare la versione più recente di Internet Explorer all'indirizzo [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) <https://www.microsoft.com/windows/ie/> ). In Microsoft Internet Explorer aprire il menu Visualizza, scegliere Opzioni, fare clic sul scheda Sicurezza e selezionare tutte le caselle di controllo Contenuto attivo.
-   Questo errore può essere causato anche da un'applet Java nella pagina. Per eseguire Microsoft Agent nella stessa pagina di un'applet Java è necessaria la versione 2.0 di Microsoft Virtual Machine (VM). Per altre informazioni, vedere Domande frequenti sulla [programmazione/scripting.](programming-scripting-faq.yml)

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-unable-to-initialize-microsoft-agent"></a>Quando si tenta di caricare una pagina con script per Microsoft Agent, viene visualizzato il messaggio "Impossibile inizializzare Microsoft Agent".

Ciò si verifica in genere quando non è installato Microsoft Agent o un altro controllo utilizzato dalla pagina e scegliere No quando viene richiesto di installare il controllo. Provare ad aggiornare la pagina, anche se la pagina può funzionare solo se si installano tutti i componenti necessari.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-the-component-has-been-digitally-signed-by-its-publisher-but-the-signature-does-not-match-the-component-it-is-possible-that-this-component-has-been-damaged-or-tampered-with-do-you-want-to-continue"></a>Quando si tenta di caricare una pagina con script per Microsoft Agent, viene visualizzato il messaggio "Il componente è stato "firmato" digitalmente dal relativo editore, ma la firma non corrisponde al componente. È possibile che questo componente sia stato danneggiato o manomesso? Continuare?"

Ciò può essere visualizzato se si tenta di installare Microsoft Agent in Microsoft Internet Explorer 3.02. È possibile continuare con l'installazione o aggiornare il browser per Internet Explorer 4.0 o versione successiva.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-using-netscape-navigator-or-other-internet-browsers-i-get-errors"></a>Quando si tenta di caricare una pagina con script per Microsoft Agent usando Netscape Navigator (o altri browser Internet), si verificano errori.

Microsoft Agent viene implementato usando ActiveX interfacce. È possibile usarlo solo con un browser (ad esempio Microsoft Internet Explorer) che supporta l'incorporamento di oggetti ActiveX tramite script in una pagina e solo nei sistemi che eseguono Microsoft Windows 95, Windows 98 e Windows NT 4.0 (o versioni successive). Se non si usa Microsoft Internet Explorer ( ), rivolgersi al fornitore del browser per altre informazioni sul ActiveX [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) supporto.

 

 




