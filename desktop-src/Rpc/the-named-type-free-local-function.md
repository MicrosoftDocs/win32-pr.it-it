---
title: Funzione named_type_free_local
description: Gli stub chiamano la funzione locale type free per liberare la memoria allocata da \_ una chiamata al tipo denominato alla routine \_ \_ \_ \_ locale.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 123e0eb12a187ee6a5b7665ec126ba98153638e9d766015a0c9e7b1c7aec7dee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924081"
---
# <a name="the-named_type_free_local-function"></a>Funzione \_ locale \_ senza tipo \_ denominato

Gli stub chiamano la **funzione \_ locale type free \_** per liberare la memoria allocata da una chiamata al tipo denominato [ \_ \_ alla \_](the-named-type-to-local-function.md) routine locale. Non libera la memoria allocata dallo stub. Il prototipo di funzione è definito come:

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

Il parametro è un puntatore alla memoria allocata **dal tipo \_ denominato \_ \_ all'oggetto locale.**

 

 




