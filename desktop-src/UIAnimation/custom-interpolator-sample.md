---
title: Esempio di interpolazione personalizzata
description: Viene illustrato come utilizzare l'animazione Windows con un interpolatore personalizzato, con Direct2D utilizzato per il rendering.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a1a2ef09d603eaefac90b2ae25b3f533ba307
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/10/2020
ms.locfileid: "104117503"
---
# <a name="custom-interpolator-sample"></a>Esempio di interpolazione personalizzata

Viene illustrato come utilizzare l'animazione Windows con un interpolatore personalizzato, con Direct2D utilizzato per il rendering. Le immagini di esempio vengono caricate dalla raccolta immagini.

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Location                               | Percorso/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Microsoft Windows Software Development Kit 7,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Code Gallery                           | [Codice di esempio di Windows Animation Manager](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

Dopo aver scaricato e installato il Windows SDK, gli esempi sono disponibili nella directory di installazione. Se ad esempio si usa il percorso di installazione predefinito per il Windows SDK per Windows 7, gli esempi vengono installati in C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi.

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio, utilizzare uno dei metodi seguenti.

**Per compilare l'esempio al prompt dei comandi**

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto CustomInterpolator. Ad esempio, il percorso di installazione predefinito per questo esempio è C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WindowsAnimation \\ CustomInterpolator

2.  Eseguire il comando seguente: **MSBuild CustomInterpolator. sln**

**Per compilare l'esempio utilizzando Microsoft Visual Studio (scelta consigliata)**

1.  Aprire Esplora risorse e passare alla directory del progetto CustomInterpolator.

    > [!Note]  
    > L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite. In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".

     

2.  Fare doppio clic sull'icona per il file CustomInterpolator. sln per aprire il progetto in Visual Studio.

3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio:

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.

2.  Eseguire **CustomInterpolator.exe** al prompt dei comandi oppure fare doppio clic sull'icona CustomInterpolator.exe in Esplora risorse.
3.  Ridimensionare la finestra o premere la barra spaziatrice e le immagini si sistemeranno in modo casuale al centro dell'area client.

4.  Premere la freccia verso l'alto o verso il basso e le immagini si accelereranno verso la parte superiore o inferiore dell'area client.

 

 




