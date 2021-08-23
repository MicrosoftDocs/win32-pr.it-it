---
title: Tipi di handle di associazione
description: Gli handle di associazione possono essere automatici, impliciti o espliciti.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a3db77f01bf0228623efe9d3dca5fbeb023d97fbe00e5da4d4ba070f323ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011075"
---
# <a name="types-of-binding-handles"></a>Tipi di handle di associazione

Gli handle di associazione possono essere automatici, impliciti o espliciti. Si differenziano per la quantità di controllo dell'applicazione rispetto al processo di associazione. Come suggerisce il nome, l'associazione automatica gestisce l'associazione automatica. Le applicazioni client e server non necessitano di codice per gestire il processo di associazione. Gli handle di associazione impliciti consentono ai programmi client di configurare l'handle di associazione prima dell'esecuzione dell'associazione. Dopo che il client ha stabilito un'associazione, la libreria di runtime RPC gestisce il resto. L'associazione esplicita gestisce lo spostamento del controllo completo sul processo di associazione nel codice sorgente dei programmi client e server. Con questo controllo aumenta la complessità. L'applicazione deve chiamare le funzioni RPC per gestire l'associazione. Non viene eseguita automaticamente. È consigliabile utilizzare handle di associazione espliciti.

Nel diagramma seguente vengono illustrate le differenze tra handle di associazione automatici, impliciti ed espliciti.

![differenze tra handle di associazione automatici, impliciti ed espliciti](images/bhand.png)

Inoltre, ogni handle di associazione è primitivo o personalizzato. Ogni tipo di handle di associazione viene illustrato negli argomenti seguenti:

-   [Handle di associazione automatici](automatic-binding-handles.md)
-   [Handle di associazione impliciti](implicit-binding-handles.md)
-   [Handle di associazione espliciti](explicit-binding-handles.md)
-   [Handle di associazione primitivi e personalizzati](primitive-and-custom-binding-handles.md)

 

 




