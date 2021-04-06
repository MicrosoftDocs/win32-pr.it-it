---
title: Tipi di handle di associazione
description: Gli handle di associazione possono essere automatici, impliciti o espliciti.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a09b858dfc677d06cf5885dc7a5f7a6ba599eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045076"
---
# <a name="types-of-binding-handles"></a>Tipi di handle di associazione

Gli handle di associazione possono essere automatici, impliciti o espliciti. Si differenziano per la quantità di controllo che l'applicazione ha sul processo di binding. Come suggerisce il nome, l'associazione automatica gestisce l'associazione automatica. Le applicazioni client e server non necessitano di codice per gestire il processo di associazione. Gli handle di associazione impliciti consentono ai programmi client di configurare l'handle di associazione prima che l'associazione venga svolta. Una volta che il client ha stabilito un'associazione, la libreria di runtime RPC gestisce il resto. Gli handle di binding espliciti spostano il controllo completo sul processo di associazione nel codice sorgente del client e dei programmi server. Con questo controllo si presenta una maggiore complessità. L'applicazione deve chiamare funzioni RPC per gestire l'associazione. Non viene eseguita automaticamente. Sono consigliati gli handle di binding espliciti.

Nel diagramma seguente vengono illustrate le differenze tra gli handle di binding automatici, impliciti ed espliciti.

![differenze tra handle di binding automatici, impliciti ed espliciti](images/bhand.png)

Inoltre, ogni handle di associazione è primitivo o personalizzato. Ogni tipo di handle di associazione viene discusso negli argomenti seguenti:

-   [Handle di binding automatici](automatic-binding-handles.md)
-   [Handle di binding impliciti](implicit-binding-handles.md)
-   [Handle di binding espliciti](explicit-binding-handles.md)
-   [Handle di binding primitivi e personalizzati](primitive-and-custom-binding-handles.md)

 

 




