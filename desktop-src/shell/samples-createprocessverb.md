---
description: Viene illustrato come implementare un verbo della shell utilizzando il metodo CreateProcess.
title: Esempio di verbo CreateProcess
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e52f251e12f0ca06bcb729407a7c8303836f9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980330"
---
# <a name="createprocess-verb-sample"></a>Esempio di verbo CreateProcess

Viene illustrato come implementare un verbo della shell utilizzando il metodo CreateProcess.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)

## <a name="description"></a>Descrizione

I verbi basati su CreateProcess dipendono dall'esecuzione di un eseguibile e dal passaggio di un argomento della riga di comando. Questo metodo non è altrettanto efficace dei metodi DropTarget e ExecuteCommand, ma consente di ottenere il comportamento out-of-process auspicabile.

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio CreateProcessVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **CreateProcessVerb** .
2.  Immettere `msbuild CreateProcessVerb.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **CreateProcessVerb** .
2.  Fare doppio clic sull'icona per il file CreateProcessVerb. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.
2.  Nella riga di comando, immettere `CreateProcessVerb.exe` . In alternativa, in Esplora risorse fare doppio clic sull'icona per CreateProcessVerb.exe.
3.  Seguire le istruzioni riportate nella finestra di dialogo visualizzata

 

 



