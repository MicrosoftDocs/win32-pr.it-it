---
description: Questo esempio illustra la decodifica di diversi frame in un file GIF, la lettura dei metadati appropriati per ogni frame, la composizione di frame e il rendering dell'animazione con Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: Esempio GIF animato WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: afb0c1368e2c66d40d1be4095ec56d5daeb5ab53
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323894"
---
# <a name="wic-animated-gif-sample"></a>Esempio GIF animato WIC

Questo esempio illustra la decodifica di diversi frame in un file GIF, la lettura dei metadati appropriati per ogni frame, la composizione di frame e il rendering dell'animazione con Direct2D.

## <a name="requirements"></a>Requisiti

Questo esempio presenta i requisiti seguenti.

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 7 |
| Windows SDK minimo | [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) per Windows 7 |

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel formato [gif animato di WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).

## <a name="building-the-sample"></a>Compilare l'esempio

### <a name="using-visual-studio-preferred-method"></a>Uso di Visual Studio (metodo preferito)

1. Aprire Esplora risorse, quindi spostarsi nella directory.
2. Fare doppio clic sull'icona del file con estensione sln (soluzione) per aprire il file in Visual Studio.
3. Scegliere **Compila soluzione** dal menu **Compila**. L'applicazione verrà compilata nella \\ directory di debug o di \\ versione predefinita.

### <a name="using-the-command-prompt"></a>Tramite il prompt dei comandi

Per compilare l'esempio utilizzando un prompt dei comandi.

1. Aprire il prompt dei comandi e passare alla directory di esempio.
2. Digitare `msbuild WICAnimatedGif.sln`

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Dopo l'avvio dell'applicazione, caricare un file di immagine usando il comando **Apri** del menu **file** . Il ridimensionamento delle finestre è supportato.

## <a name="see-also"></a>Vedi anche

[Codec Microsoft Windows Imaging](-wic-lh.md)

[Guida per programmatori](-wic-programming-guide.md)

[Riferimento](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Esempi ed esempi di codice](-wic-samples.md)
