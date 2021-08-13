---
description: Illustra come implementare un verbo shell usando il metodo DropTarget.
title: Esempio di verbo DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ae9ae3edb2d993f2e42a2556899d45cb3b10722fc7d7a9dc5e9786560fc3078f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719533"
---
# <a name="droptarget-verb-sample"></a>Esempio di verbo DropTarget

Illustra come implementare un verbo shell usando il metodo DropTarget.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)

## <a name="description"></a>Descrizione

Questo esempio illustra come implementare un verbo shell usando il metodo DropTarget. Questo metodo è preferibile per le implementazioni di verbi che devono funzionare Windows XP. In questo esempio viene implementato un oggetto com (Server Component Object Model) locale autonomo, ma è previsto che l'implementazione del verbo sia integrata nelle applicazioni esistenti. A tale scopo, l'oggetto applicazione principale registra un class factory per se stesso. Tale oggetto implementa [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) per i verbi dell'applicazione. Si noti che COM avvia l'applicazione se non è già in esecuzione, ma si connette a un'istanza in esecuzione dell'applicazione, se presente.

## <a name="requirements"></a>Requisiti



| Product                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Località      | URL del percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio di DropTargetVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory **del progetto DropTargetVerb.**
2.  Immettere `msbuild DropTargetVerb.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita):

1.  Aprire Windows Explorer e passare alla directory **del progetto DropTargetVerb.**
2.  Fare doppio clic sull'icona per il file DropTargetVerb.sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo eseguibile, usando il prompt dei comandi o Windows Explorer.
2.  Nella riga di comando immettere `DropTargetVerb.exe` . In alternativa, in Windows Explorer fare doppio clic sull'icona per DropTargetVerb.exe.
3.  Seguire le istruzioni nella finestra di dialogo visualizzata

 

 
