---
title: Installazione guidata plug-in di Online Store
description: Installazione guidata plug-in di Online Store
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Windows Media Player negozi online, plug-in
- negozi online, plug-in
- tipo 1 negozi online, plug-in
- Windows Media Player negozi online, procedura guidata plug-in
- negozi online, creazione guidata plug-in
- tipo 1 negozi online, procedura guidata plug-in
- Windows Media Player negozi online, installazione guidata plug-in
- negozi online, installazione guidata plug-in
- tipo 1 negozi online, installazione guidata plug-in
- plug-in, Windows Media Player online store
- plug-in, negozi online
- plug-in, tipo 1 negozi online
- plug-in, installazione guidata plug-in
- plug-in, creazione guidata plug-in
- Windows Media Player plug-in, tipo 1 negozi online
- Windows Media Player plug-in, negozi online
- Windows Media Player plug-in, Windows Media Player online store
- Windows Media Player plug-in, installazione guidata plug-in
- Windows Media Player plug-in, creazione guidata plug-in
- installazione guidata plug-in
- Creazione guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1088d915715be44de092604d626bc24792f6d263a9765a1076ce1afa3f67ef4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135544"
---
# <a name="installing-the-online-store-plug-in-wizard"></a>Installazione guidata plug-in di Online Store

Per configurare l'ambiente di sviluppo per la creazione di plug-in del negozio online di tipo 1, è necessario installare gli elementi seguenti:

-   Microsoft Visual Studio 2005 o versione successiva
-   Windows Media Player 11 o versione successiva
-   Windows SDK, che include Windows Media Player SDK
-   Creazione guidata plug-in del negozio online

## <a name="installing-the-wizard"></a>Installazione della procedura guidata

Usare la procedura seguente per installare la procedura guidata plug-in del negozio online in Visual Studio.

1.  Individuare la cartella in cui è stato installato Windows SDK. Espandere la cartella per visualizzarne le sottocartelle e passare a Esempi di servizi \\ delle \\ procedure guidate WMP \\ \\ multimediali.
2.  Individuare i tre file seguenti:
    -   wmpservices.vsz
    -   wmpservices.vsdir
    -   wmpservices.ico
3.  Usando un editor di testo come Blocco note, modificare il file wmpservices.vsz.

    Individuare la riga seguente:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Passare `<VsWizardEngine version goes here>` a uno dei valori seguenti, a seconda della versione Visual Studio installata.

    

    | Valore              | Versione di Visual Studio |
    |--------------------|-----------------------|
    | VsWizardEngine.8.0 | Visual Studio 2005    |
    | VsWizardEngine.9.0 | Visual Studio 2008    |

    

     

    Individuare la riga seguente:

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Passare `<path to wmpservices directory goes here>` al percorso in cui si trovano i file della procedura guidata.

    Si supponga, ad esempio, di avere Visual Studio 2008 e che i file della procedura guidata siano qui: C: Programmi \\ \\ Microsoft SDK Windows \\ v7.0 Samples Multimedia WMP wizards services (C: Programmi Microsoft SDK Windows \\ v7.0 \\ Samples Multimedia \\ \\ WMP \\ \\ wizards services). Il file wmpservices.vsz sarà quindi simile al seguente:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Individuare la cartella in cui è stato installato Visual Studio. Espandere la cartella per visualizzarne le sottocartelle e individuare una cartella denominata vcprojects.
5.  Copiare i tre file elencati nel passaggio 2 nella cartella vcprojects. La procedura guidata è ora installata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione del plug-in per uno Store online di tipo 1](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




