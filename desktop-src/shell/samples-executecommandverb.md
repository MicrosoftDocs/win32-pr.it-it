---
description: Illustra come implementare un verbo Shell usando il metodo ExecuteCommand.
title: Esempio di verbo del comando Execute
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e32b472d63b9d2d779c97b64833f354e7d4d2eaed034d3a213ae4e101f7beb3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858270"
---
# <a name="execute-command-verb-sample"></a>Esempio di verbo del comando Execute

Illustra come implementare un verbo Shell usando il metodo ExecuteCommand.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)

## <a name="description"></a>Descrizione

Questo metodo è preferibile per le implementazioni di verbi perché offre la massima flessibilità, è semplice e supporta l'attivazione out-of-process. Questo esempio implementa un oggetto server Component Object Model (COM) autonomo, ma è previsto che l'implementazione del verbo verrà integrata nelle applicazioni esistenti. A tale scopo, l'oggetto applicazione principale deve registrare un class factory per se stesso. Tale oggetto implementa [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) per i verbi dell'applicazione. Si noti che COM avvia l'applicazione se non è già in esecuzione, ma si connette a un'istanza in esecuzione dell'applicazione, se presente.

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Località      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio di ExecuteCommandVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **ExecuteCommandVerb.**
2.  Immettere `msbuild ExecuteCommand.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita):

1.  Aprire Windows Explorer e passare alla directory del progetto **ExecuteCommandVerb.**
2.  Fare doppio clic sull'icona per il file ExecuteCommand.sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo eseguibile, usando il prompt dei comandi o Windows Explorer.
2.  Nella riga di comando immettere `ExecuteCommand.exe` . In alternativa, da esplora Windows fare doppio clic sull'icona per ExecuteCommand.exe.
3.  Seguire le istruzioni nella finestra di dialogo visualizzata

 

 
