---
description: Viene illustrato come estendere il menu di scelta rapida del trascinamento della selezione (talvolta definito menu di scelta rapida).
title: Esempio NonDefaultDropMenuVerb
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9d326e012fb78b04fd542f88d49c370e8aeab613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347931"
---
# <a name="nondefaultdropmenuverb-sample"></a>Esempio NonDefaultDropMenuVerb

Viene illustrato come estendere il menu di scelta rapida del trascinamento della selezione (talvolta definito menu di scelta rapida).

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

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio NonDefaultDropMenuVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **NonDefaultDropMenuVerb** .
2.  Immettere `msbuild NonDefaultDropMenuVerb.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **NonDefaultDropMenuVerb** .
2.  Fare doppio clic sull'icona per il file NonDefaultDropMenuVerb. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo file DLL, usando il prompt dei comandi o Esplora risorse.
2.  Copiare NonDefaultDropMenuVerb.dll nella directory di sistema, ad esempio C: \\ Windows \\ system32.
3.  Al prompt dei comandi immettere `regedit NonDefaultDropMenuVerb.reg` .
4.  Usare il pulsante destro del mouse per trascinare un file da una cartella a un'altra. Vengono visualizzate altre voci di menu per l'operazione DROP.

 

 



