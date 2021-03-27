---
description: Illustra le sovrapposizioni e le barre di stato dell'icona della barra delle applicazioni.
title: Esempio di stato della periferica della barra delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E4B693FB-EE7D-47d0-A5D8-91205AD4A3DC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 793c09853e3174f426b7b41685f2593daaae9b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995045"
---
# <a name="taskbar-peripheral-status-sample"></a>Esempio di stato della periferica della barra delle applicazioni

Illustra le sovrapposizioni e le barre di stato dell'icona della barra delle applicazioni.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

Questo esempio crea un pulsante della barra delle applicazioni di esempio in cui viene illustrato l'uso di [**all'ITaskbarList3:: SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) consentendo di applicare varie sovrimpressioni scelte da un menu.

L'esempio fornisce anche la possibilità di simulare un indicatore di stato sul pulsante, dimostrando l'uso di [**all'ITaskbarList3:: SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) e [**all'ITaskbarList3:: SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) mostrando inizialmente un indicatore di stato indeterminato (TBPF \_ indeterminato), quindi un indicatore proporzionale normale (TBPF \_ normale).

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio TaskBarPeripheralStatus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarPeripheralStatus) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **TaskbarPeripheralStatus** .
2.  Immettere `msbuild PeripheralStatus.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **TaskbarPeripheralStatus** .
2.  Fare doppio clic sull'icona per il file PeripheralStatus. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo file eseguibile (ad esempio, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug` ), usando il prompt dei comandi o Esplora risorse.

    -   Se si usa la riga di comando, immettere `PeripheralStatus.exe` .
    -   Se si usa Esplora risorse, fare doppio clic sull'icona per PeripheralStatus.exe.

    Viene aperta una nuova finestra con un pulsante della barra delle applicazioni associato.

2.  Per dimostrare le sovrapposizioni, scegliere **sovrimpressione 1** o **sovrapposizione 2** dal menu **stato periferica** della finestra. La sovrimpressione scelta verrà visualizzata sul pulsante della barra delle applicazioni. Per rimuovere la sovrimpressione, scegliere **Cancella sovrimpressione**.
3.  Per illustrare l'indicatore di stato, scegliere **simula stato** dal menu **stato periferica** della finestra. Il pulsante della barra delle applicazioni Visualizza un indicatore di stato indeterminato, quindi passa a un indicatore normale.
4.  Scegliere **Esci** dal menu **file** della finestra per terminare il programma.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Estensioni della barra delle applicazioni](taskbar-extensions.md)
</dt> </dl>

 

 



