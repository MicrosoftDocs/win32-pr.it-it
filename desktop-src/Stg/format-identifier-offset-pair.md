---
title: Identificatore di formato/coppia di offset
description: La seconda parte del flusso del set di proprietà contiene una coppia identificatore/offset di formato.
ms.assetid: cc3a748d-e81c-45da-b04f-ea986158a4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f80a85175278b92fedbfd7b2d50d94007b7e4a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329540"
---
# <a name="format-identifieroffset-pair"></a>Identificatore di formato/coppia di offset

La seconda parte del flusso del set di proprietà contiene una coppia identificatore/offset di formato. FMTID è il nome del set di proprietà. identifica in modo univoco il modo in cui interpretare il contenuto della sezione seguente. L'offset corrisponde alla distanza, in byte, dall'inizio dell'intero flusso a quello in cui inizia la sezione.

La struttura seguente è utile per la gestione delle coppie identificatore/offset del formato.

``` syntax
typedef struct tagFORMATIDOFFSET 
{ 
    FMTID  fmtid ;     // Name of the section. 
    DWORD  dwOffset ;  // Offset for the section. 
} FORMATIDOFFSET;
```

 

 




