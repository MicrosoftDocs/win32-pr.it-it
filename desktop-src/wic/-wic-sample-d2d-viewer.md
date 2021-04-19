---
description: In questo esempio viene illustrato l'utilizzo di Windows Imaging Component (WIC) per decodificare un file di immagine e Direct2D per eseguire il rendering dell'immagine sullo schermo.
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: Visualizzatore immagini WIC con esempio Direct2D
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323889"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a>Visualizzatore immagini WIC con esempio Direct2D

In questo esempio viene illustrato l'utilizzo di Windows Imaging Component (WIC) per decodificare un file di immagine e Direct2D per eseguire il rendering dell'immagine sullo schermo.

## <a name="requirements"></a>Requisiti

Questo esempio presenta i requisiti seguenti.

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows Vista |
| Windows SDK minimo | [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) per Windows 7 |

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [Visualizzatore WIC D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).

## <a name="building-the-sample"></a>Compilare l'esempio

### <a name="using-visual-studio-preferred-method"></a>Uso di Visual Studio (metodo preferito)

1. Aprire Esplora risorse, quindi spostarsi nella directory.
2. Fare doppio clic sull'icona del file con estensione sln (soluzione) per aprire il file in Visual Studio.
3. Scegliere **Compila soluzione** dal menu **Compila**. L'applicazione verrà compilata nella \\ directory di debug o di \\ versione predefinita.

### <a name="using-the-command-prompt"></a>Tramite il prompt dei comandi

Per compilare l'esempio utilizzando un prompt dei comandi:

1. Aprire una finestra del prompt dei comandi e passare alla directory di esempio.
2. Digitare `msbuild WICViewerD2D.sln`

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Dopo aver avviato l'applicazione, caricare un file di immagine usando il comando **Apri** del menu **file** .

## <a name="see-also"></a>Vedi anche

[Codec Microsoft Windows Imaging](-wic-lh.md)

[Guida per programmatori](-wic-programming-guide.md)

[Riferimento](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Esempi ed esempi di codice](-wic-samples.md)
