---
description: Viene illustrata una barra degli strumenti dell'anteprima, un controllo attivo della barra degli strumenti incorporato nell'anteprima dell'anteprima di una finestra, usato per fornire l'accesso ai comandi chiave di una finestra senza fare in modo che l'utente ripristini o attivi la finestra dell'applicazione.
title: Esempio di barra degli strumenti di anteprima della barra delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e61208f15772a43138e6cd7a38fd6327445bdfa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980322"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a>Esempio di barra degli strumenti di anteprima della barra delle applicazioni

Viene illustrata una barra degli strumenti dell'anteprima, un controllo attivo della barra degli strumenti incorporato nell'anteprima dell'anteprima di una finestra, usato per fornire l'accesso ai comandi chiave di una finestra senza fare in modo che l'utente ripristini o attivi la finestra dell'applicazione.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

In questo esempio viene illustrato come fornire una semplice barra degli strumenti per un'anteprima dell'anteprima della barra delle applicazioni. La barra degli strumenti è costituita da tre pulsanti. Quando si fa clic su un pulsante, viene visualizzata una finestra per confermare che il pulsante è stato attivato. Vengono illustrate le API seguenti:

-   [**All'ITaskbarList3:: ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**All'ITaskbarList3:: ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   Struttura [**ThumbButton**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio TaskbarThumbnailToolbar](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **TaskbarThumbnailToolbar** .
2.  Immettere `msbuild ThumbnailToolbar.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **TaskbarThumbnailToolbar** .
2.  Fare doppio clic sull'icona per il file ThumbnailToolbar. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo file eseguibile (ad esempio, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` ), usando il prompt dei comandi o Esplora risorse.

    -   Se si usa la riga di comando, immettere `ThumbnailToolbar.exe` .
    -   Se si usa Esplora risorse, fare doppio clic sull'icona per ThumbnailToolbar.exe.

    Viene aperta una nuova finestra con un pulsante della barra delle applicazioni associato.

2.  Posizionare il puntatore del mouse sul pulsante della barra delle applicazioni di **ThumbnailToolbar** in modo che l'anteprima venga visualizzata. Fare clic su uno dei tre pulsanti (verde, giallo, rosso) visualizzato sulla barra degli strumenti dell'anteprima.
3.  Scegliere **Esci** dal menu **file** della finestra per terminare il programma.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Estensioni della barra delle applicazioni](taskbar-extensions.md)
</dt> </dl>

 

 



