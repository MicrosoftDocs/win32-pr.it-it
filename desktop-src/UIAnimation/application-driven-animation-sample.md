---
title: Application-Driven di animazione
description: Mostra Windows'animazione nella configurazione guidata dall'applicazione usando Direct2D per animare il colore di sfondo di una finestra e la sincronizzazione con la frequenza di aggiornamento.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfbb5ce71ddeff6a37c2d872e0e1e93fdc58cde9fcc8359560d9d386ba7a0834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137374"
---
# <a name="application-driven-animation-sample"></a>Application-Driven di animazione

Mostra Windows'animazione nella configurazione guidata dall'applicazione usando Direct2D per animare il colore di sfondo di una finestra e la sincronizzazione con la frequenza di aggiornamento.

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

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto AppDriven. Ad esempio, il percorso di installazione predefinito per questo esempio è C: Programmi \\ \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia \\ \\ WindowsAnimation \\ AppDriven.

2.  Eseguire il comando seguente: **msbuild AppDriven.sln**

**Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita)**

1.  Aprire Windows Explorer e passare alla directory del progetto AppDriven.

2.  Fare doppio clic sull'icona per il file AppDriven.sln per aprire il progetto in Visual Studio.

    > [!Note]  
    > L'estensione del nome file sln non viene visualizzata nelle impostazioni predefinite della cartella. In questo caso, può essere identificato dall'icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".

     

3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio:

1.  Passare alla directory che contiene il nuovo eseguibile, usando il prompt dei comandi o Windows Explorer.

2.  Eseguire **AppDriven.exe** al prompt dei comandi oppure fare doppio clic sull'icona per AppDriven.exe in Windows Explorer.

3.  Fare clic in un punto qualsiasi dell'area client. Il colore di sfondo della finestra verrà modificato in un colore casuale.

 

 




