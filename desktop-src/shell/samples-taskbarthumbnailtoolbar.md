---
description: Illustra una barra degli strumenti di anteprima, un controllo della barra degli strumenti attivo incorporato nell'anteprima dell'anteprima di una finestra, usato per fornire l'accesso ai comandi chiave di una finestra senza fare in modo che l'utente ripristini o attivi la finestra dell'applicazione.
title: Esempio di barra degli strumenti di anteprima della barra delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: cd16ee40bfb480b3e7eacef2bc4681e61fdb24ace1ac68985e2016ce11b7c0e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219630"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a>Esempio di barra degli strumenti di anteprima della barra delle applicazioni

Illustra una barra degli strumenti di anteprima, un controllo della barra degli strumenti attivo incorporato nell'anteprima dell'anteprima di una finestra, usato per fornire l'accesso ai comandi chiave di una finestra senza fare in modo che l'utente ripristini o attivi la finestra dell'applicazione.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

Questo esempio illustra come fornire una semplice barra degli strumenti a un'anteprima dell'anteprima della barra delle applicazioni. La barra degli strumenti è costituita da tre pulsanti. Facendo clic su un pulsante viene visualizzata una finestra per confermare che il pulsante è stato attivato. Vengono illustrate le API seguenti:

-   [**ITaskbarList3::ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3::ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**Struttura THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Località      | URL del percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio di TaskbarThumbnailToolbar](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **TaskbarThumbnailToolbar.**
2.  Immettere `msbuild ThumbnailToolbar.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita):

1.  Aprire Windows Explorer e passare alla directory **del progetto TaskbarThumbnailToolbar.**
2.  Fare doppio clic sull'icona per il file ThumbnailToolbar.sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo file eseguibile , ad esempio , usando il prompt dei comandi `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` o Windows Explorer.

    -   Se si usa la riga di comando, immettere `ThumbnailToolbar.exe` .
    -   Se si usa Windows Explorer, fare doppio clic sull'icona per ThumbnailToolbar.exe.

    Verrà aperta una nuova finestra, con un pulsante della barra delle applicazioni associato.

2.  Passare il cursore sul pulsante **della barra delle applicazioni ThumbnailToolbar** in modo che l'anteprima sia visualizzata. Fare clic su uno dei tre pulsanti (verde, giallo, rosso) visualizzati nella barra degli strumenti dell'anteprima.
3.  Scegliere **Esci** dal menu **File della** finestra per terminare il programma.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Estensioni della barra delle applicazioni](taskbar-extensions.md)
</dt> </dl>

 

 



