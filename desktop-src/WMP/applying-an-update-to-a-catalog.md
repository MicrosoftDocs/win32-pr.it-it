---
title: Applicazione di un aggiornamento a un catalogo
description: Applicazione di un aggiornamento a un catalogo
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Windows Media Player negozi online, applicazione di aggiornamenti ai cataloghi
- negozi online, applicazione di aggiornamenti ai cataloghi
- store online di tipo 1, applicazione di aggiornamenti ai cataloghi
- Windows Media Player negozi online, aggiornamento dei cataloghi
- negozi online, aggiornamento dei cataloghi
- store online di tipo 1, aggiornamento dei cataloghi
- Windows Media Player online store, aggiornamenti del catalogo
- negozi online, aggiornamenti del catalogo
- tipo 1 negozi online, aggiornamenti del catalogo
- aggiornamenti del catalogo
- aggiornamento di cataloghi
- applicazione di aggiornamenti ai cataloghi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114b5b341df1101b221a3d8227bf0526bfa32af744f1dca7b0a53ca2d7793c46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124031"
---
# <a name="applying-an-update-to-a-catalog"></a>Applicazione di un aggiornamento a un catalogo

> [!Note]  
> Questa operazione non viene in genere eseguita tranne a scopo diagnostico, ad esempio per verificare che un file delle differenze sia valido. Il catalogo generato in questo modo non è in formato compresso e non deve essere passato a Windows Media Player.

 

È possibile creare un nuovo file di catalogo usando la sintassi seguente, dove *inputcatalog* è il percorso del catalogo originale e *inputdiff* è il percorso del file delle differenze da applicare. I file del catalogo devono essere in formato non compresso.


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



Ad esempio, il codice seguente crea un nuovo catalogo da C: \\ Catalog210 \\ catalog.wmdb e C: \\ Catalog210 \\ catalog.diff.


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



Se la compilazione ha esito positivo, catcomp.exe crea i file di output seguenti.



| Nome file        | Descrizione       |
|------------------|-------------------|
| catalog.wmdb.new | Nuovo file di catalogo. |



 

 

 




