---
title: Applicazione di un aggiornamento a un catalogo
description: Applicazione di un aggiornamento a un catalogo
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Windows Media Player Online Stores, applicazione degli aggiornamenti ai cataloghi
- negozi online, applicazione di aggiornamenti ai cataloghi
- digitare 1 negozi online, applicazione di aggiornamenti ai cataloghi
- Windows Media Player Online Stores, aggiornamento di cataloghi
- archivi online, aggiornamento di cataloghi
- digitare 1 negozi online, aggiornamento di cataloghi
- Windows Media Player Online Stores, aggiornamenti del catalogo
- archivi online, aggiornamenti del catalogo
- digitare 1 negozi online, aggiornamenti del catalogo
- aggiornamenti del catalogo
- aggiornamento di cataloghi
- applicazione degli aggiornamenti ai cataloghi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d468edb7d09b8804fa924f7c31fc1be45d27c8fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298931"
---
# <a name="applying-an-update-to-a-catalog"></a>Applicazione di un aggiornamento a un catalogo

> [!Note]  
> Questa operazione non viene in genere eseguita ad eccezione degli scopi di diagnostica, ad esempio per verificare che un file di differenza sia valido. Il catalogo generato in questo modo non è in formato compresso e non deve essere passato a Windows Media Player.

 

È possibile creare un nuovo file di catalogo usando la sintassi seguente, dove *inputcatalog* è il percorso del catalogo originale e *inputdiff* è il percorso del file di differenza da applicare. I file di catalogo devono essere in formato non compresso.


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



Ad esempio, di seguito viene creato un nuovo catalogo da C: \\ Catalog210 \\ Catalog. WMDB e c: \\ Catalog210 \\ Catalog. diff.


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



Se la compilazione ha esito positivo, catcomp.exe crea i file di output seguenti.



| Nome file        | Descrizione       |
|------------------|-------------------|
| Catalog. WMDB. New | Nuovo file di catalogo. |



 

 

 




