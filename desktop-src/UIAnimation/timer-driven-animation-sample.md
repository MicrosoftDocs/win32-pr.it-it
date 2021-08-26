---
title: Timer-Driven di animazione
description: Illustra come usare l'Windows con il timer di animazione, mentre GDI+ per animare il colore di sfondo di una finestra.
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8071d51906ba2d0d7b59acb7b1b5531fcb5c577fbbf0d47ab5039d3f43e2eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008161"
---
# <a name="timer-driven-animation-sample"></a>Timer-Driven di animazione

Illustra come usare l'Windows con il timer di animazione, mentre GDI+ per animare il colore di sfondo di una finestra.

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Località                               | Percorso/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Microsoft Windows Software Development Kit 7.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Code Gallery                           | [Windows Codice di esempio di Animation Manager](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

Dopo aver scaricato e installato Windows SDK, gli esempi sono disponibili nella directory di installazione. Ad esempio, se si usa il percorso di installazione predefinito per Windows SDK per Windows 7, gli esempi vengono installati in C: \\ Programmi \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples.

## <a name="building-the-sample"></a>Compilazione dell'esempio

Usare uno dei metodi seguenti per compilare l'esempio.

**Per compilare l'esempio al prompt dei comandi**

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto TimerDriven. Ad esempio, il percorso di installazione predefinito per questo esempio è C: Programmi \\ \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia \\ \\ WindowsAnimation \\ TimerDriven.

2.  Eseguire il comando seguente: **msbuild TimerDriven.sln**

**Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita)**

1.  Aprire Windows Explorer e passare alla directory del progetto TimerDriven.

2.  Fare doppio clic sull'icona del file TimerDriven.sln per aprire il progetto in Visual Studio.

    > [!Note]  
    > L'estensione del nome file sln non viene visualizzata nelle impostazioni predefinite della cartella. In questo caso, può essere identificato dall'icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".

     

3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio:

1.  Passare alla directory che contiene il nuovo eseguibile, usando il prompt dei comandi o Windows Explorer.

2.  Eseguire **TimerDriven.exe** al prompt dei comandi oppure fare doppio clic sull'icona per TimerDriven.exe in Windows Explorer.

3.  Fare clic in un punto qualsiasi dell'area client. Il colore di sfondo della finestra verrà modificato in un colore casuale.

 

 




