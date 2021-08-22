---
title: 'Uso del Kit di certificazione app Windows '
description: Per offrire all'app desktop la migliore possibilità di ottenere la certificazione, convalidarla e testarla nel computer prima di inviarla per la certificazione e l'inserzione in Windows Store.
ms.assetid: 8B460B84-0997-4987-9B66-90F9C6D88D83
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8692e87f8bd152b730129c0d8684bc7ec2ca91964ecd6c25e98eb3db3e0fce44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118708749"
---
# <a name="using-the-windows-app-certification-kit"></a>Uso del Kit di certificazione app Windows 

Per offrire all'app desktop la migliore possibilità di ottenere la certificazione, convalidarla e testarla nel computer prima di inviarla per la certificazione e l'inserzione in Windows Store. Per certificare l'app, è necessario installare ed eseguire Windows Kit di [certificazione app.](/previous-versions//mt637081(v=vs.85)) Per informazioni dettagliate su test specifici all'interno del kit, fare riferimento Windows test del kit di [certificazione delle app.](windows-app-certification-kit-tests.md)

Per un'analisi di alto livello del processo di certificazione e della posizione in cui si inserisce l'uso di questo strumento, vedere [Certificare l'app desktop.](windows-certification-portal.md)

La versione corrente di Windows ACK è disponibile in 14 lingue (ceco, inglese, francese, tedesco, italiano, giapponese, coreano, polacco, portoghese (Brasile), russo, cinese semplificato, spagnolo, cinese tradizionale e turco.

## <a name="prerequisites"></a>Prerequisiti

Prima di installare il Windows ACK, è necessario installare ed eseguire il sistema operativo.

1. Installare ed eseguire il sistema operativo per cui si sviluppano le app.

-   Se si sviluppano app per Windows 7, è possibile installare ed eseguire Windows 7, Windows 8 o Windows 8.1.
-   Se si sviluppa un'app desktop Windows 8 o un Windows 8 app per dispositivi desktop, è possibile installare ed eseguire Windows 8 o Windows 8.1.
-   Se si sta sviluppando un'app desktop Windows 8.1 o un'app Windows 8 dispositivo desktop, installare Windows 8.1.

2. Installare Windows [App Certification Kit 3.3,](/previous-versions//mt637081(v=vs.85))incluso in Windows Software Development Kit (SDK) per Windows 8.1.

**Nota:** Quando si installa Windows App Certification Kit 3.3 o versione successiva nel PC, si sostituisce qualsiasi versione del kit installata in precedenza.

## <a name="instructions-to-run-windows-app-certification-kit-33"></a>Istruzioni per eseguire Windows App Certification Kit 3.3

**Convalidare l'app desktop usando Windows App Certification Kit 3.3 in modo interattivo**

1.  Nel menu Start cercare Windows App Cert Kit.
2.  Nel kit di Windows app fare clic sulla categoria di convalida dei test che si vuole eseguire. Se si sta convalidando un'app desktop, selezionare **Convalida app desktop**.
3.  Nella schermata successiva passare al file di installazione dell'app desktop da convalidare.
    -   **Nota:** Se necessario, è [possibile usare](#commandlinesteps) i passaggi della riga di comando per includere opzioni o un'opzione di installazione.
4.  Indicare il tipo di utilizzo dell'app e quindi fare clic su **Avanti.** Il Windows kit di certificazione delle app avvia l'installazione dell'app desktop usando i file di installazione in modo che possa convalidare l'installazione.
5.  Se viene chiesto di riavviare il sistema per completare l'installazione, scegliere **No**. Se l'app deve installare diversi componenti o dipendenze esterne, selezionare con attenzione il nome dell'app. Il nome scelto qui è il nome assegnato all'app se viene elencata nell'Windows Store. Al termine della convalida, salvare il report con il nome fornito all'app nel passaggio 6. Il Windows App Certification Kit crea un file di report XML e lo salva.
6.  Passare alla cartella in cui è stato salvato il report e aprirlo per visualizzare i risultati del test. Se il test non è riuscito e si è idonei per una deroga, le informazioni da inviare sono elencate qui. È necessario inviare una descrizione dettagliata per ogni possibile richiesta di rinuncia.

**Convalidare l Windows app desktop usando Windows App Certification Kit 3.3 dalla riga di comando**

1.  Passare alla cartella in cui è stato salvato il report e aprirlo per visualizzare i risultati del test. I test non superati con una possibile richiesta di rinuncia sono elencati qui. È necessario inviare una descrizione dettagliata per ogni possibile richiesta di rinuncia.
2.  Nella cartella che contiene il kit di Windows app immettere questi comandi nell'ordine seguente:

    -   <span id="commandLineSteps"></span><span id="commandlinesteps"></span><span id="COMMANDLINESTEPS"></span>`appcert.exe reset`
    -   `appcert test -apptype desktop -setuppath d:\cdrom\setup.exe  -appusage peruser -reportoutputpath [report file name]`

    dove: è il nome file completo del file XML che verrà creato dal `[report file name]` kit per contenere il report di test.

3.  Al termine del test, aprire il file di report denominato \[ nome file del report e visualizzare i risultati del \] test.

    **Nota:** Per altre informazioni sulla riga di comando Windows App Certification Kit, immettere il comando appcert.exe /?

    Il Windows di certificazione app deve essere eseguito nel contesto di una sessione utente attiva, ma non è possibile avviare le app in una sessione non interattiva. Il modo in cui il kit gestisce i token per l'esecuzione di test con o senza privilegi amministrativi dipende anche da questo contesto di sessione utente. Il kit può essere eseguito da un servizio, ma il servizio deve essere in grado di generare il processo del kit in una sessione utente attiva.

**Usare il kit di Windows app per convalidare le Windows 7 app**

-   Il Windows di certificazione delle app ha sostituito Windows Software Logo Kit. Se si vuole usare il logo Windows 7 per l'app, usare il kit di Windows app per il test di convalida e il report. Il kit può rilevare il sistema operativo su cui è in esecuzione e avvia automaticamente per Windows 7 app. Seguire lo stesso processo per convalidare Windows 7 app.

**Inviare per la certificazione**

-   Dopo aver convalidato l'app, è possibile inviarla per la certificazione [tramite il processo di invio del portale.](https://www.microsoft.com/?ref=go)

## <a name="reference-documents"></a>Documenti di riferimento

-   [Requisiti di certificazione per le app desktop di Windows](/windows/desktop/win_cert/certification-requirements-for-windows-desktop-apps)
-   [Certificazione delle app white paper](https://www.microsoft.com/download/details.aspx?id=27414)
-   [Windows Onboarding dello Store per le app desktop](/previous-versions//dn322034(v=vs.85))
-   [Windows 7 requisiti di certificazione delle app desktop](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)

## <a name="windows-app-certification-kit-tests"></a>Test del Kit di certificazione app Windows

Il kit è stato modificato per semplificare [l'uso Windows test ACK.](windows-app-certification-kit-tests.md) Il kit include ora:

-   Una nuova interfaccia utente semplificata
-   Miglioramento del test multi-utente, che non richiede più la configurazione di un secondo account utente

 

 