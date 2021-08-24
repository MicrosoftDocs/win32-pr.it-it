---
description: Illustra come usare i metodi dell'interfaccia IFileOperationProgressSink per monitorare i dettagli delle azioni dell'interfaccia IFileOperation.
title: FileOperationProgressSink
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fe0ba5c86fdb2df5fe168559aa019941897563823e75670b0813ecb7e9e44d69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820351"
---
# <a name="file-operation-progress-sink"></a>FileOperationProgressSink

Illustra come usare i metodi [**dell'interfaccia IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) per monitorare i dettagli [**delle azioni dell'interfaccia IFileOperation.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation)

In questo argomento sono contenute le sezioni seguenti.

-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 6.1                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Località      | URL del percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio di FileOperationProgressSink](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dalla finestra del prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **FileOperationProgressSink.**
2.  Immettere `msbuild FileOperationProgressSinkSample.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita):

1.  Aprire Windows Explorer e passare alla directory **del progetto FilesInUse.** Ad esempio, il percorso di installazione predefinito completo è `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .
2.  Fare doppio clic sull'icona per il file FileOperationProgressSinkSample.sln per aprire il progetto in Visual Studio.
    > [!Note]  
    > L'estensione del nome file sln non viene visualizzata nelle impostazioni predefinite della cartella. In questo caso, può essere identificato dall'icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".

     

3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo eseguibile, usando la finestra del prompt dei comandi o Windows Explorer.
2.  Al prompt dei comandi immettere o in Windows Explorer fare doppio clic `FileOperationProgressSinkSample.exe` sull'icona per FileOperationProgressSinkSample.exe.

 

 



