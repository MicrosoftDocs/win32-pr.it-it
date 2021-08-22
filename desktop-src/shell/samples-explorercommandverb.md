---
description: Illustra come implementare un verbo Shell usando i metodi ExplorerCommand e ExplorerCommandState.
title: Esempio di verbo del comando Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ec8f4c88ea01aad410e982fc24fd248f3c1826d8c8657e904844b535e621fd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719183"
---
# <a name="explorer-command-verb-sample"></a>Esempio di verbo del comando Explorer

Illustra come implementare un verbo Shell usando i metodi ExplorerCommand e ExplorerCommandState.

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
| GitHub  | [Esempio di ExplorerCommandVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **ExplorerCommandVerb.**
2.  Immettere `msbuild ExplorerCommandVerb.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita):

1.  Aprire Windows Explorer e passare alla directory **del progetto ExplorerCommandVerb.**
2.  Fare doppio clic sull'icona per il file ExplorerCommandVerb.sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il ExplorerCommandVerb.dll, usando il prompt dei comandi o Windows Explorer. Assicurarsi di usare il file DLL a 64 bit in un Windows a 64 bit.
2.  Nella riga di comando immettere `regsvr32.exe ExplorerCommandVerb.dll` .
3.  Due nuovi verbi verranno visualizzati nel menu di scelta rapida quando si fa clic con il pulsante destro del mouse su .txt file.

 

 



