---
description: Il tipo di dati AnyPath è una stringa di testo contenente un percorso completo o relativo.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab5d8e7aaf4e92c2b33379b92b00263df07366ff340346aa19518478f8f2394
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045781"
---
# <a name="anypath"></a>AnyPath

Il tipo di dati AnyPath è una stringa di testo contenente un percorso completo o relativo. Quando si specifica un percorso relativo, è possibile includere un nome di file lungo con il nome file breve separando i nomi brevi e lunghi con una barra verticale ( \| ). Si noti che non è possibile specificare più livelli di una directory o percorsi completi in questo modo. Il percorso può contenere proprietà racchiuse tra parentesi quadre ( \[ \] ).

Esempi di dati AnyPath validi:

-   \\\\server \\ share \\ temp
-   c: \\ temp
-   \\Temp
-   projec~1 \| Project stato

Esempi di dati AnyPath non validi:

-   c: \\ temp \\ projec~1 \| c: temp one Project \\ \\ Status
-   \\temp \\ projec~1 \| \\ temp one Project \\ Status

 

 



