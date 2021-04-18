---
title: Esempio di animazione Application-Driven
description: Mostra l'animazione Windows nella configurazione guidata dall'applicazione tramite Direct2D per animare il colore di sfondo di una finestra e la sincronizzazione alla frequenza di aggiornamento.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b24905d09ac6559527146ebf572666a6a84f5
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/10/2020
ms.locfileid: "106299558"
---
# <a name="application-driven-animation-sample"></a>Esempio di animazione Application-Driven

Mostra l'animazione Windows nella configurazione guidata dall'applicazione tramite Direct2D per animare il colore di sfondo di una finestra e la sincronizzazione alla frequenza di aggiornamento.

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

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto AppDriven. Ad esempio, il percorso di installazione predefinito per questo esempio è C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WindowsAnimation \\ AppDriven.

2.  Eseguire il comando seguente: **MSBuild AppDriven. sln**

**Per compilare l'esempio utilizzando Microsoft Visual Studio (scelta consigliata)**

1.  Aprire Esplora risorse e passare alla directory del progetto AppDriven.

2.  Fare doppio clic sull'icona per il file AppDriven. sln per aprire il progetto in Visual Studio.

    > [!Note]  
    > L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite. In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".

     

3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio:

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.

2.  Eseguire **AppDriven.exe** al prompt dei comandi oppure fare doppio clic sull'icona AppDriven.exe in Esplora risorse.

3.  Fare clic in un punto qualsiasi dell'area client e il colore di sfondo della finestra cambierà in un colore casuale.

 

 




