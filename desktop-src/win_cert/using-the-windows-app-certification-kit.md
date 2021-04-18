---
title: 'Uso del Kit di certificazione app Windows '
description: Per fornire all'app desktop la possibilità di ottenere la certificazione, convalidarla e testarla nel computer prima di inviarla per la certificazione e l'inserimento in Windows Store.
ms.assetid: 8B460B84-0997-4987-9B66-90F9C6D88D83
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89b3c6e4de3286dd6418c4c8e186bcadaddf00b7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399838"
---
# <a name="using-the-windows-app-certification-kit"></a>Uso del Kit di certificazione app Windows 

Per fornire all'app desktop la possibilità di ottenere la certificazione, convalidarla e testarla nel computer prima di inviarla per la certificazione e l'inserimento in Windows Store. Per certificare l'app, è necessario installare ed eseguire il [Kit di certificazione app Windows](/previous-versions//mt637081(v=vs.85)). Per informazioni dettagliate su test specifici all'interno del kit, vedere [test del kit di certificazione applicazioni Windows](windows-app-certification-kit-tests.md).

Per informazioni generali sul processo di certificazione e sull'uso di questo strumento, vedere [Certificate your desktop app](windows-certification-portal.md).

La versione corrente di ACK di Windows è disponibile in 14 lingue (ceco, inglese, francese, tedesco, italiano, giapponese, coreano, polacco, portoghese (Brasile), russo, cinese semplificato, spagnolo, cinese tradizionale e turco).

## <a name="prerequisites"></a>Prerequisiti

Prima di installare il ACK di Windows, è necessario installare ed eseguire il sistema operativo.

1. Installare ed eseguire il sistema operativo per cui si stanno sviluppando le app.

-   Se stai sviluppando app per Windows 7, puoi installare ed eseguire Windows 7, Windows 8 o Windows 8.1.
-   Se si sta sviluppando un'app desktop di Windows 8 o un'app per dispositivi desktop Windows 8, è possibile installare ed eseguire Windows 8 o Windows 8.1.
-   Se si sta sviluppando un'app desktop Windows 8.1 o un'app per dispositivi desktop Windows 8, installare Windows 8.1.

2. Installare il [Kit di certificazione applicazioni windows 3,3](/previous-versions//mt637081(v=vs.85)), incluso in Windows Software Development Kit (SDK) per Windows 8.1.

**Nota:** Quando si installa il kit di certificazione app Windows 3,3 o versione successiva nel PC, sostituire qualsiasi versione installata in precedenza del kit.

## <a name="instructions-to-run-windows-app-certification-kit-33"></a>Istruzioni per l'esecuzione del kit di certificazione app Windows 3,3

**Convalidare l'app desktop usando il kit di certificazione applicazioni Windows 3,3 in modo interattivo**

1.  Dal menu Start, cercare Windows app CERT Kit.
2.  Dal kit di certificazione applicazioni Windows, fare clic sulla categoria convalida test che si desidera eseguire. Se si sta convalidando un'app desktop, selezionare **convalida app desktop**.
3.  Nella schermata successiva passare al file di installazione dell'app desktop che si vuole convalidare.
    -   **Nota:** Se necessario, è possibile usare i [passaggi della riga di comando](#commandlinesteps) per includere opzioni o un'opzione di installazione.
4.  Indicare il tipo di utilizzo dell'app, quindi fare clic su **Avanti**. Il kit di certificazione app Windows avvia l'installazione dell'app desktop usando i file di installazione in modo che possa convalidare l'installazione.
5.  Se viene richiesto di riavviare il sistema per completare l'installazione, scegliere **No**. Se l'app deve installare diversi componenti o dipendenze esterne, selezionare con attenzione il nome dell'app. Il nome scelto è il nome assegnato all'app se viene elencato in Windows Store. Al termine della convalida, salvare il report con il nome assegnato all'app nel passaggio 6. Il kit di certificazione applicazioni Windows crea un file di report XML e lo salva.
6.  Passare alla cartella in cui è stato salvato il report e aprirlo per visualizzare i risultati del test. Se il test non è riuscito e si è idonei per una deroga, le informazioni necessarie per l'invio sono elencate qui. È necessario inviare una descrizione dettagliata per ogni possibile richiesta di deroga.

**Convalidare l'app desktop di Windows usando il kit di certificazione app Windows 3,3 da una riga di comando**

1.  Passare alla cartella in cui è stato salvato il report e aprirlo per visualizzare i risultati del test. I test non superati con una possibile richiesta di deroga sono elencati qui. È necessario inviare una descrizione dettagliata per ogni possibile richiesta di deroga.
2.  Dalla cartella che contiene il kit di certificazione applicazioni Windows, immettere questi comandi nell'ordine seguente:

    -   <span id="commandLineSteps"></span><span id="commandlinesteps"></span><span id="COMMANDLINESTEPS"></span>`appcert.exe reset`
    -   `appcert test -apptype desktop -setuppath d:\cdrom\setup.exe  -appusage peruser -reportoutputpath [report file name]`

    Dove: `[report file name]` è il nome file completo del file XML che verrà creato dal kit per contenere il report di test.

3.  Al termine del test, aprire il file di report denominato \[ report nome file \] e visualizzare i risultati del test.

    **Nota:** Per ulteriori informazioni sulla riga di comando del kit di certificazione applicazioni Windows, immettere il comando appcert.exe/?

    Il kit di certificazione applicazioni Windows deve essere eseguito nel contesto di una sessione utente attiva ma non è possibile avviare app in una sessione non interattiva. Il modo in cui il kit gestisce i token per l'esecuzione di test con o senza privilegi amministrativi dipende anche da questo contesto della sessione utente. Il kit può essere eseguito da un servizio, ma il servizio deve essere in grado di generare il processo del kit in una sessione utente attiva.

**Usa il kit di certificazione app Windows per convalidare le tue app di Windows 7**

-   Il kit di certificazione applicazioni Windows ha sostituito Windows software logo Kit. Se si desidera il logo di Windows 7 per l'app, utilizzare il kit di certificazione app Windows per il test e il report di convalida. Il kit può rilevare il sistema operativo in cui è in esecuzione e viene avviato automaticamente per le app di Windows 7. Seguire lo stesso processo per la convalida delle app di Windows 7.

**Inviare per la certificazione**

-   Una volta convalidata l'app, si è pronti per inviarla per [la certificazione tramite il processo di invio del portale](https://www.microsoft.com/?ref=go).

## <a name="reference-documents"></a>Documenti di riferimento

-   [Requisiti di certificazione per le app desktop di Windows](/windows/desktop/win_cert/certification-requirements-for-windows-desktop-apps)
-   [white paper di certificazione app](https://www.microsoft.com/download/details.aspx?id=27414)
-   [Onboarding di Windows Store per le app desktop](/previous-versions//dn322034(v=vs.85))
-   [Requisiti di certificazione delle app desktop di Windows 7](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)

## <a name="windows-app-certification-kit-tests"></a>Test del Kit di certificazione app Windows

Il kit è stato modificato per semplificare l'uso dei [test ACK di Windows](windows-app-certification-kit-tests.md) . Il kit include ora:

-   Nuova interfaccia utente semplificata
-   Test multiutente migliorato, che non richiede più la configurazione di un secondo account utente

 

 