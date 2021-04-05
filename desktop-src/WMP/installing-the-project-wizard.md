---
title: Installazione guidata progetto
description: Installazione guidata progetto
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Windows Media Player Online Stores, plug-in
- archivi online, plug-in
- digitare 2 archivi online, plug-in
- Windows Media Player Online Stores, creazione guidata plug-in
- negozi online, creazione guidata plug-in
- digitare 2 archivi online, creazione guidata plug-in
- Windows Media Player Online Stores, creazione guidata progetto
- negozi online, creazione guidata progetto
- digitare 2 archivi online, creazione guidata progetto
- Windows Media Player Online Stores, installazione guidata plug-in
- negozi online, installazione guidata plug-in
- digitare 2 archivi online, installazione guidata plug-in
- Windows Media Player Online Stores, installazione guidata progetto
- negozi online, installazione guidata progetto
- digitare 2 archivi online, installazione guidata progetto
- plug-in, archivi Windows Media Player online
- plug-in, archivi online
- plug-in, digitare 2 archivi online
- plug-in, installazione guidata plug-in
- plug-in, creazione guidata plug-in
- plug-in, installazione guidata progetto
- plug-in, creazione guidata progetto
- Plug-in di Windows Media Player, digitare 2 archivi online
- Plug-in di Windows Media Player, archivi online
- Plug-in di Windows Media Player, archivi Windows Media Player online
- Plug-in di Windows Media Player, installazione guidata plug-in
- Plug-in di Windows Media Player, creazione guidata plug-in
- Plug-in di Windows Media Player, installazione guidata progetto
- Plug-in di Windows Media Player, creazione guidata progetto
- installazione guidata plug-in
- procedura guidata plug-in
- installazione guidata progetto
- Creazione guidata progetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc37754a028d73114b1b425dcbc80e268559355d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711989"
---
# <a name="installing-the-project-wizard"></a>Installazione guidata progetto

Per configurare l'ambiente di sviluppo per la creazione di plug-in di archivio online di tipo 2, è necessario installare gli elementi seguenti:

-   Microsoft Visual Studio .NET 2003 o versione successiva
-   Windows Media Player 9 serie o versione successiva
-   Windows SDK, che include Windows Media Player SDK
-   Procedura guidata plug-in di archivio online

## <a name="installing-the-wizard"></a>Installazione della procedura guidata

Usare la procedura seguente per installare la procedura guidata plug-in di negozio online in Visual Studio.

1.  Individuare la cartella in cui è stato installato il Windows SDK. Espandere la cartella per visualizzare le relative sottocartelle e passare a esempi \\ Multimedia \\ WMP \\ Wizards \\ Services.
2.  Individuare i tre file seguenti:
    -   wmpservices. vsz
    -   wmpservices. vsdir
    -   wmpservices. ico
3.  Utilizzando un editor di testo, ad esempio Blocco note, modificare il file wmpservices. vsz.

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
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Passare `<path to wmpservices directory goes here>` al percorso in cui si trovano i file della procedura guidata.

    Si supponga, ad esempio, di avere Visual Studio 2008 e che i file della procedura guidata siano qui: C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi di \\ Multimedia \\ WMP \\ Wizards \\ Services. Il file wmpservices. vsz avrà un aspetto simile al seguente:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Individuare la cartella in cui è installato Visual Studio. Espandere la cartella per visualizzare le relative sottocartelle e individuare una cartella denominata vcprojects.
5.  Copiare i tre file elencati nel passaggio 2 nella cartella VCProjects. Ora è installata la procedura guidata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del plug-in per un negozio online di tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




