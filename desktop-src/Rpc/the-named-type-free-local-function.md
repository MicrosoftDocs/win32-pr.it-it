---
title: Funzione named_type_free_local
description: Gli stub chiamano la \_ \_ funzione locale di tipo free per liberare la memoria allocata da una chiamata al \_ tipo denominato \_ alla \_ routine locale.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f2796f33e9dc60364b6afda244d8dae47eef0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709088"
---
# <a name="the-named_type_free_local-function"></a>\_Funzione locale del tipo denominato \_ Free \_

Gli stub chiamano la **funzione \_ \_ locale di tipo Free** per liberare la memoria allocata da una chiamata [al \_ tipo denominato \_ alla routine \_ locale](the-named-type-to-local-function.md) . Non libera la memoria allocata dallo stub. Il prototipo di funzione è definito come segue:

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

Il parametro è un puntatore alla memoria allocata dal **\_ tipo denominato \_ a \_ local**.

 

 




