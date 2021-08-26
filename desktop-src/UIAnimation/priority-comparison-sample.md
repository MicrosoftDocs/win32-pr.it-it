---
title: Esempio di confronto delle priorità
description: Illustra come usare l'Windows animation con un confronto di priorità personalizzato, usando Direct2D per il rendering.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafeb2332de02115cbb8af2f2afd69a2fc783be9908a91dbb4e9bb0615876bd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008191"
---
# <a name="priority-comparison-sample"></a>Esempio di confronto delle priorità

Illustra come usare l'Windows animation con un confronto di priorità personalizzato, usando Direct2D per il rendering.

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Località                               | Percorso/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Microsoft Windows Software Development Kit 7.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Code Gallery                           | [Windows Codice di esempio di Gestione animazioni](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

Dopo aver scaricato e installato Windows SDK, gli esempi sono disponibili nella directory di installazione. Ad esempio, se si usa il percorso di installazione predefinito per Windows SDK per Windows 7, gli esempi vengono installati in C: \\ Programmi Microsoft SDK Windows \\ \\ \\ v7.0 \\ Samples.

## <a name="building-the-sample"></a>Compilazione dell'esempio

Usare uno dei metodi seguenti per compilare l'esempio.

**Per compilare l'esempio al prompt dei comandi**

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto PriorityComparison. Ad esempio, il percorso di installazione predefinito per questo esempio è C: Programmi \\ \\ Microsoft SDK Windows \\ \\ v7.0 \\ Samples Multimedia \\ \\ WindowsAnimation \\ PriorityComparison.

2.  Eseguire il comando seguente: **msbuild PriorityComparison.sln**

**Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita)**

1.  Aprire Windows Explorer e passare alla directory del progetto PriorityComparison.

2.  Fare doppio clic sull'icona per il file PriorityComparison.sln per aprire il progetto in Visual Studio.

    > [!Note]  
    > L'estensione di file sln non viene visualizzata nelle impostazioni predefinite della cartella. In questo caso, può essere identificato dalla relativa icona univoca o dalla relativa descrizione del tipo, "Microsoft Visual Studio Soluzione".

     

3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio:

1.  Passare alla directory che contiene il nuovo eseguibile, usando il prompt dei comandi o Windows Explorer.

2.  Eseguire **PriorityComparison.exe** al prompt dei comandi o fare doppio clic sull'icona per PriorityComparison.exe in Windows Explorer.

3.  Le immagini di esempio vengono caricate dalla raccolta immagini. Ridimensionare la finestra o premere la barra spaziatrice per spostare le immagini al centro.

4.  Usare i tasti freccia SINISTRA e DESTRA per selezionare immagini diverse(più velocemente viene premuto il tasto, più velocemente la selezione cambierà).

5.  Usare i tasti freccia SU e GIÙ per creare un'onda attraverso le immagini (più velocemente viene premuto il tasto, più veloce è l'onda).

 

 




