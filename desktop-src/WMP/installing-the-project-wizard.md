---
title: Installazione della Project guidata
description: Installazione della Project guidata
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Windows Media Player store online, plug-in
- online store, plug-in
- store online di tipo 2, plug-in
- Windows Media Player store online, procedura guidata plug-in
- online stores, procedura guidata plug-in
- tipo 2 negozi online, procedura guidata plug-in
- Windows Media Player online, creazione guidata progetto
- online stores, creazione guidata progetto
- tipo 2 negozi online, creazione guidata progetto
- Windows Media Player online, installazione guidata plug-in
- online store, installazione guidata plug-in
- tipo 2 negozi online, installazione guidata plug-in
- Windows Media Player online, installazione guidata progetto
- online stores,installazione guidata progetto
- tipo 2 negozi online, installazione guidata progetto
- plug-in, Windows Media Player online store
- plug-in, negozi online
- plug-in, tipo 2 negozi online
- plug-in, installazione guidata plug-in
- plug-in, procedura guidata plug-in
- plug-in, installazione guidata progetto
- plug-in, creazione guidata progetto
- Windows Media Player plug-in, digitare 2 store online
- Windows Media Player plug-in, store online
- Windows Media Player plug-in, Windows Media Player store online
- Windows Media Player plug-in, installazione guidata plug-in
- Windows Media Player plug-in, procedura guidata plug-in
- Windows Media Player plug-in, installazione guidata progetto
- Windows Media Player plug-in, Creazione guidata progetto
- installazione guidata plug-in
- Procedura guidata plug-in
- installazione guidata del progetto
- Creazione guidata progetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f00e0430791fb36285ba365eed752083889f2b55bd126c4a588d2a506f58acd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123521"
---
# <a name="installing-the-project-wizard"></a>Installazione della Project guidata

Per configurare l'ambiente di sviluppo per la creazione di plug-in dello store online di tipo 2, è necessario installare gli elementi seguenti:

-   Microsoft Visual Studio .NET 2003 o versione successiva
-   Windows Media Player serie 9 o successive
-   Windows SDK, che include l'SDK Windows Media Player
-   Creazione guidata plug-in dello store online

## <a name="installing-the-wizard"></a>Installazione della procedura guidata

Usare la procedura seguente per installare la procedura guidata del plug-in dello store online in Visual Studio.

1.  Individuare la cartella in cui è stato installato Windows SDK. Espandere la cartella per visualizzarne le sottocartelle e passare a Samples Multimedia WMP wizards services (Esempi di servizi \\ \\ delle procedure guidate WMP \\ \\ multimediali).
2.  Individuare i tre file seguenti:
    -   wmpservices.vsz
    -   wmpservices.vsdir
    -   wmpservices.ico
3.  Usando un editor di testo come Blocco note, modificare il file wmpservices.vsz.

    Individuare la riga seguente:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Modificare `<VsWizardEngine version goes here>` con uno dei valori seguenti, a seconda della versione di Visual Studio installata.

    

    | Valore              | Versione di Visual Studio   |
    |--------------------|-------------------------|
    | VsWizardEngine.7.1 | Visual Studio .NET 2003 |
    | VsWizardEngine.8.0 | Visual Studio 2005      |
    | VsWizardEngine.9.0 | Visual Studio 2008      |

    

     

    Individuare la riga seguente:

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Passare `<path to wmpservices directory goes here>` al percorso in cui si trovano i file della procedura guidata.

    Si supponga, ad esempio, di avere Visual Studio 2008 e che i file della procedura guidata siano disponibili qui: C: Programmi \\ \\ Microsoft SDKs \\ Windows \\ v7.0 Samples Multimedia \\ \\ \\ WMP \\ wizards services(C: Programmi Microsoft SDK Windows v7.0 Samples Multimedia WMP \\ wizards services). Il file wmpservices.vsz sarà quindi simile al seguente:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Individuare la cartella in cui è stato Visual Studio. Espandere la cartella per visualizzarne le sottocartelle e individuare una cartella denominata vcprojects.
5.  Copiare i tre file elencati nel passaggio 2 nella cartella vcprojects. La procedura guidata è ora installata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del plug-in per uno store online di tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




