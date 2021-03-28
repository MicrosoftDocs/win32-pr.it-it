---
description: Viene illustrato come implementare un verbo della shell utilizzando il metodo DropTarget.
title: Esempio di verbo DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f737c951c5bd588760dbb716859c04c0dc062fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979935"
---
# <a name="droptarget-verb-sample"></a>Esempio di verbo DropTarget

Viene illustrato come implementare un verbo della shell utilizzando il metodo DropTarget.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)

## <a name="description"></a>Descrizione

In questo esempio viene illustrato come implementare un verbo della shell utilizzando il metodo DropTarget. Questo metodo è preferibile per le implementazioni di verbi che devono funzionare in Windows XP. Questo esempio implementa un oggetto server locale Component Object Model (COM) autonomo, ma si prevede che l'implementazione del verbo verrà integrata nelle applicazioni esistenti. A tale scopo, l'oggetto applicazione principale registra un class factory per se stesso. Tale oggetto implementa [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) per i verbi dell'applicazione. Si noti che COM avvia l'applicazione se non è già in esecuzione, ma si connette a un'istanza in esecuzione dell'applicazione, se disponibile.

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio DropTargetVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **DropTargetVerb** .
2.  Immettere `msbuild DropTargetVerb.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **DropTargetVerb** .
2.  Fare doppio clic sull'icona per il file DropTargetVerb. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.
2.  Nella riga di comando, immettere `DropTargetVerb.exe` . In alternativa, in Esplora risorse fare doppio clic sull'icona per DropTargetVerb.exe.
3.  Seguire le istruzioni riportate nella finestra di dialogo visualizzata

 

 
