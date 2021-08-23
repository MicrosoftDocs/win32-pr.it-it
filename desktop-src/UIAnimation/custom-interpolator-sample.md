---
title: Esempio di interpolatore personalizzato
description: Illustra come usare l'Windows con un interpolatore personalizzato, con Direct2D usato per il rendering.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c801822bd50eebe9f405cad00bc8ffcd7ac2d611924a3ff0bae91d30bc9f249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999701"
---
# <a name="custom-interpolator-sample"></a>Esempio di interpolatore personalizzato

Illustra come usare l'Windows con un interpolatore personalizzato, con Direct2D usato per il rendering. Le immagini di esempio vengono caricate dalla Raccolta immagini.

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Località                               | Percorso/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Microsoft Windows Software Development Kit 7.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Code Gallery                           | [Windows Codice di esempio di Animation Manager](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

Dopo aver scaricato e installato Windows SDK, gli esempi sono disponibili nella directory di installazione. Ad esempio, se si usa il percorso di installazione predefinito per Windows SDK per Windows 7, gli esempi vengono installati in C: \\ Programmi \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples.

## <a name="building-the-sample"></a>Compilazione dell'esempio

Usare uno dei metodi seguenti per compilare l'esempio.

**Per compilare l'esempio al prompt dei comandi**

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto CustomInterpolator. Ad esempio, il percorso di installazione predefinito per questo esempio è C: Programmi \\ \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia \\ \\ WindowsAnimation \\ CustomInterpolator

2.  Eseguire il comando seguente: **msbuild CustomInterpolator.sln**

**Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita)**

1.  Aprire Windows Explorer e passare alla directory del progetto CustomInterpolator.

    > [!Note]  
    > L'estensione del nome file sln non viene visualizzata nelle impostazioni predefinite della cartella. In questo caso, può essere identificato dall'icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".

     

2.  Fare doppio clic sull'icona del file CustomInterpolator.sln per aprire il progetto in Visual Studio.

3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio:

1.  Passare alla directory che contiene il nuovo eseguibile, usando il prompt dei comandi o Windows Explorer.

2.  Eseguire **CustomInterpolator.exe** al prompt dei comandi oppure fare doppio clic sull'icona per CustomInterpolator.exe in Windows Explorer.
3.  Ridimensionare la finestra o premere la barra spaziatrice per disporre le immagini in modo casuale al centro dell'area client.

4.  Premere la freccia su o giù per accelerare le immagini verso la parte superiore o inferiore dell'area client.

 

 




