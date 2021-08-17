---
description: Viene illustrato come estendere il menu di scelta rapida di trascinamento della selezione( talvolta definito menu di scelta rapida).
title: Esempio NonDefaultDropMenuVerb
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1c4623b9143e0a23762cfc44dd8dfc4f46b827a0f6433098d45d8a784ead81f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968790"
---
# <a name="nondefaultdropmenuverb-sample"></a>Esempio NonDefaultDropMenuVerb

Viene illustrato come estendere il menu di scelta rapida di trascinamento della selezione( talvolta definito menu di scelta rapida).

In questo argomento sono contenute le sezioni seguenti.

-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Località      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio di NonDefaultDropMenuVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **NonDefaultDropMenuVerb.**
2.  Immettere `msbuild NonDefaultDropMenuVerb.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita):

1.  Aprire Windows Explorer e passare alla directory del progetto **NonDefaultDropMenuVerb.**
2.  Fare doppio clic sull'icona per il file NonDefaultDropMenuVerb.sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo file DLL, usando il prompt dei comandi o Windows Explorer.
2.  Copiare NonDefaultDropMenuVerb.dll nella directory System (ad esempio, C: \\ Windows \\ System32).
3.  Al prompt dei comandi immettere `regedit NonDefaultDropMenuVerb.reg` .
4.  Usare il pulsante destro del mouse per trascinare un file da una cartella a un'altra. Verranno visualizzati elementi di menu aggiuntivi per l'operazione di rilascio.

 

 



