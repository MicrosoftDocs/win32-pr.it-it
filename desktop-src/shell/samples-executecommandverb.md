---
description: Viene illustrato come implementare un verbo della shell utilizzando il metodo ExecuteCommand.
title: Esempio di verbo del comando Execute
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2deeb63fc6648d07b3d870888d6d2eabc6fb0490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234213"
---
# <a name="execute-command-verb-sample"></a>Esempio di verbo del comando Execute

Viene illustrato come implementare un verbo della shell utilizzando il metodo ExecuteCommand.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)

## <a name="description"></a>Descrizione

Questo metodo è preferibile per le implementazioni di verbi perché offre la massima flessibilità, è semplice e supporta l'attivazione out-of-process. In questo esempio viene implementato un oggetto server locale Component Object Model (COM) autonomo, ma si prevede che l'implementazione del verbo verrà integrata nelle applicazioni esistenti. A tale scopo, l'oggetto applicazione principale deve registrare un class factory per se stesso. Tale oggetto implementa [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) per i verbi dell'applicazione. Si noti che COM avvia l'applicazione se non è già in esecuzione, ma si connette a un'istanza in esecuzione dell'applicazione, se disponibile.

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio ExecuteCommandVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **ExecuteCommandVerb** .
2.  Immettere `msbuild ExecuteCommand.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **ExecuteCommandVerb** .
2.  Fare doppio clic sull'icona per il file ExecuteCommand. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.
2.  Nella riga di comando, immettere `ExecuteCommand.exe` . In alternativa, in Esplora risorse fare doppio clic sull'icona per ExecuteCommand.exe.
3.  Seguire le istruzioni riportate nella finestra di dialogo visualizzata

 

 
