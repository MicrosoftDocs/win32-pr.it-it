---
title: Attività iniziali con la Creazione guidata plug-in
description: Attività iniziali con la Creazione guidata plug-in
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Windows Media Player plug-in, installazione guidata plug-in
- plug-in, installazione guidata plug-in
- compilazione di plug-in, installazione guidata plug-in
- Windows Media Player Creazione guidata plug-in, installazione
- installazione guidata plug-in
- Creazione guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2699d0316be93f6387bdc64c6671df868eaa70fb24a4ad3619026524106432
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576580"
---
# <a name="getting-started-with-the-plug-in-wizard"></a>Attività iniziali con la Creazione guidata plug-in

Per configurare l'ambiente di sviluppo per la Windows Media Player plug-in, è necessario installare gli elementi seguenti:

-   Microsoft Visual Studio .NET 2003 o versione successiva
-   Windows Media Player serie 9 o successive
-   Windows SDK, che include Windows Media Player SDK
-   Windows Media Player Creazione guidata plug-in

## <a name="installing-the-wizard"></a>Installazione della procedura guidata

Seguire questa procedura per installare la procedura guidata Windows Media Player plug-in.

1.  Individuare la cartella in cui è stato installato Windows SDK. Espandere la cartella per visualizzarne le sottocartelle e passare a Esempi di procedure \\ \\ guidate WMP \\ multimediali \\ wmpwiz.
2.  Individuare i tre file seguenti:
    -   wmpwiz.vsz
    -   wmpwiz.vsdir
    -   wmpwiz.ico
3.  Usando un editor di testo, ad esempio Blocco note, modificare il file wmpwiz.vsz.

    Individuare la riga seguente:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Passare a uno dei valori seguenti, a seconda della versione Visual Studio `<VsWizardEngine version goes here>` installata.

    

    | Valore              | Versione di Visual Studio   |
    |--------------------|-------------------------|
    | VsWizardEngine.7.1 | Visual Studio .NET 2003 |
    | VsWizardEngine.8.0 | Visual Studio 2005      |
    | VsWizardEngine.9.0 | Visual Studio 2008      |

    

     

    Individuare la riga seguente:

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    Passare `<path to wmpwiz directory goes here>` al percorso in cui si trovano i file della procedura guidata.

    Si supponga ad esempio di avere Visual Studio 2008 e che i file della procedura guidata siano qui: C: Programmi \\ \\ Microsoft SDK Windows \\ \\ v7.0 \\ Samples Multimedia \\ \\ WMP \\ \\ wizards wmpwiz. Il file wmpwiz.vsz sarà quindi simile al seguente:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Individuare la cartella in cui è stato installato Visual Studio. Espandere la cartella per visualizzarne le sottocartelle e individuare una cartella denominata vcprojects.
5.  Copiare i tre file elencati nel passaggio 2 nella cartella vcprojects. La procedura guidata è ora installata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di un plug-in](building-a-plug-in.md)
</dt> <dt>

[Uso della Creazione guidata plug-in con Visual Studio](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




