---
description: Illustra come implementare un verbo shell usando il metodo CreateProcess.
title: Esempio di verbo CreateProcess
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c0af34d5ec9f687ec6c58bb73f337b38d512527c0ace4bd20eae12d49c87a62d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858341"
---
# <a name="createprocess-verb-sample"></a>Esempio di verbo CreateProcess

Illustra come implementare un verbo shell usando il metodo CreateProcess.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)

## <a name="description"></a>Descrizione

I verbi basati su CreateProcess dipendono dall'esecuzione di un eseguibile e dal passaggio di un argomento della riga di comando. Questo metodo non è potente quanto i metodi DropTarget ed ExecuteCommand, ma consente di ottenere il comportamento out-of-process desiderato.

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Località      | URL del percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio di CreateProcessVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory **del progetto CreateProcessVerb.**
2.  Immettere `msbuild CreateProcessVerb.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita):

1.  Aprire Windows Explorer e passare alla directory **del progetto CreateProcessVerb.**
2.  Fare doppio clic sull'icona del file CreateProcessVerb.sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo eseguibile, usando il prompt dei comandi o Windows Explorer.
2.  Nella riga di comando immettere `CreateProcessVerb.exe` . In alternativa, in Windows Explorer fare doppio clic sull'icona per CreateProcessVerb.exe.
3.  Seguire le istruzioni nella finestra di dialogo visualizzata

 

 



