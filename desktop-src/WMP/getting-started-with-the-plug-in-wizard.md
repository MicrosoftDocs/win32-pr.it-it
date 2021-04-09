---
title: Introduzione con la procedura guidata plug-in
description: Introduzione con la procedura guidata plug-in
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Plug-in di Windows Media Player, installazione guidata plug-in
- plug-in, installazione guidata plug-in
- creazione di plug-in, installazione guidata plug-in
- Creazione guidata plug-in di Windows Media Player, installazione
- installazione guidata plug-in
- procedura guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955678"
---
# <a name="getting-started-with-the-plug-in-wizard"></a>Introduzione con la procedura guidata plug-in

Per configurare l'ambiente di sviluppo per la creazione di plug-in di Windows Media Player, è necessario installare gli elementi seguenti:

-   Microsoft Visual Studio .NET 2003 o versione successiva
-   Windows Media Player 9 serie o versione successiva
-   Windows SDK, che include Windows Media Player SDK
-   Procedura guidata plug-in di Windows Media Player

## <a name="installing-the-wizard"></a>Installazione della procedura guidata

Per installare la creazione guidata plug-in di Windows Media Player, attenersi alla procedura riportata di seguito.

1.  Individuare la cartella in cui è stato installato il Windows SDK. Espandere la cartella per visualizzare le relative sottocartelle e passare a esempi di \\ strumenti multimediali per \\ WMP \\ \\ wmpwiz.
2.  Individuare i tre file seguenti:
    -   wmpwiz. vsz
    -   wmpwiz. vsdir
    -   wmpwiz. ico
3.  Utilizzando un editor di testo, ad esempio Blocco note, modificare il file wmpwiz. vsz.

    Individuare la riga seguente:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Passare `<VsWizardEngine version goes here>` a uno dei valori seguenti, a seconda della versione di Visual Studio installata.

    

    | Valore              | Versione di Visual Studio   |
    |--------------------|-------------------------|
    | VsWizardEngine. 7.1 | Visual Studio .NET 2003 |
    | VsWizardEngine. 8.0 | Visual Studio 2005      |
    | VsWizardEngine. 9.0 | Visual Studio 2008      |

    

     

    Individuare la riga seguente:

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    Passare `<path to wmpwiz directory goes here>` al percorso in cui si trovano i file della procedura guidata.

    Si supponga, ad esempio, di avere Visual Studio 2008 e che i file della procedura guidata siano disponibili qui: C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi di \\ strumenti multimediali per \\ WMP \\ \\ wmpwiz. Il file wmpwiz. vsz avrà un aspetto simile al seguente:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Individuare la cartella in cui è installato Visual Studio. Espandere la cartella per visualizzare le relative sottocartelle e individuare una cartella denominata vcprojects.
5.  Copiare i tre file elencati nel passaggio 2 nella cartella VCProjects. Ora è installata la procedura guidata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un plug-in](building-a-plug-in.md)
</dt> <dt>

[Uso della procedura guidata plug-in con Visual Studio](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




