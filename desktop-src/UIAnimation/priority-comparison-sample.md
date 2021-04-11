---
title: Esempio di confronto prioritario
description: Viene illustrato come utilizzare l'animazione Windows con un confronto prioritario tramite Direct2D per il rendering.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfcb20785d6a4c3c3384b85327a0e27d93c58d7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/10/2020
ms.locfileid: "104117502"
---
# <a name="priority-comparison-sample"></a>Esempio di confronto prioritario

Viene illustrato come utilizzare l'animazione Windows con un confronto prioritario tramite Direct2D per il rendering.

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

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto PriorityComparison. Ad esempio, il percorso di installazione predefinito per questo esempio è C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WindowsAnimation \\ PriorityComparison.

2.  Eseguire il comando seguente: **MSBuild PriorityComparison. sln**

**Per compilare l'esempio utilizzando Microsoft Visual Studio (scelta consigliata)**

1.  Aprire Esplora risorse e passare alla directory del progetto PriorityComparison.

2.  Fare doppio clic sull'icona per il file PriorityComparison. sln per aprire il progetto in Visual Studio.

    > [!Note]  
    > L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite. In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".

     

3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio:

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.

2.  Eseguire **PriorityComparison.exe** al prompt dei comandi oppure fare doppio clic sull'icona PriorityComparison.exe in Esplora risorse.

3.  Le immagini di esempio vengono caricate dalla raccolta immagini. Ridimensionare la finestra o premere la barra spaziatrice e le immagini vengono spostate al centro.

4.  Usare i tasti freccia sinistra e destra per selezionare immagini diverse (più velocemente verrà premuto il tasto, più velocemente verrà modificata la selezione).

5.  Usare i tasti freccia su e giù per creare un'onda attraverso le immagini (maggiore è la pressione della chiave, più velocemente l'onda).

 

 




