---
description: In questo esempio viene illustrato l'utilizzo di Windows Imaging Component (WIC) per decodificare un'immagine codificata con livelli progressivi.
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: Esempio di decodifica progressiva WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 2e4b1fc560af0ee8c817208fec628ddb068676bb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323890"
---
# <a name="wic-progressive-decoding-sample"></a>Esempio di decodifica progressiva WIC

In questo esempio viene illustrato l'utilizzo di Windows Imaging Component (WIC) per decodificare un'immagine codificata con livelli progressivi. In questo esempio viene utilizzato Direct2D per eseguire il rendering dei diversi livelli progressivi sullo schermo.

## <a name="requirements"></a>Requisiti

Questo esempio presenta i requisiti seguenti.

| Requisito | Valore |
|-|
| Client minimo supportato | Windows 7 |
| Windows SDK minimo | [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) per Windows 7 |

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nella [codifica progressiva WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).

## <a name="building-the-sample"></a>Compilare l'esempio

### <a name="using-visual-studio-preferred-method"></a>Uso di Visual Studio (metodo preferito)

1. Aprire Esplora risorse, quindi spostarsi nella directory.
2. Fare doppio clic sull'icona del file con estensione sln (soluzione) per aprire il file in Visual Studio.
3. Scegliere Genera soluzione dal menu Genera. L'applicazione verrà compilata nella \\ directory di debug o di \\ versione predefinita.

### <a name="using-the-command-prompt"></a>Tramite il prompt dei comandi

Per compilare l'esempio utilizzando il prompt dei comandi.

1. Aprire il prompt dei comandi e passare alla directory di esempio.
2. Digitare `msbuild WICProgressiveDecoding.sln`

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Dopo l'avvio dell'applicazione, caricare un file di immagine tramite il menu file Apri. Al caricamento, il livello progressivo predefinito è impostato su 0. È possibile passare a livelli progressivi diversi tramite il menu o il tasto freccia su o giù. Il testo del livello progressivo corrente viene visualizzato sulla barra di stato della finestra principale. Il ridimensionamento delle finestre è supportato.

> [!NOTE]
> La decodifica progressiva è disponibile solo per le immagini che sono state codificate progressivamente. L'immagine fornita con questo esempio è stata codificata in maniera progressiva.

## <a name="see-also"></a>Vedi anche

[Codec Microsoft Windows Imaging](-wic-lh.md)

[Guida per programmatori](-wic-programming-guide.md)

[Riferimento](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Esempi ed esempi di codice](-wic-samples.md)

[Panoramica della decodifica progressiva](-wic-progressive-decoding.md)
