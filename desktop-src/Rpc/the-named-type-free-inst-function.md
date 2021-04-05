---
title: Funzione named_type_free_inst
description: Gli stub chiamano la \_ \_ funzione Inst gratuita del tipo denominato \_ per liberare la memoria associata al tipo trasmesso.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d3b5103572eb58e4311c65b0e1cff02e91f66f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709091"
---
# <a name="the-named_type_free_inst-function"></a>\_ \_ Funzione Inst disponibile del tipo denominato \_

Gli stub chiamano la **funzione \_ \_ \_ inst gratuita del tipo denominato** per liberare la memoria associata al tipo trasmesso. La funzione è definita come segue:

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

Il parametro punta all'istanza del tipo trasmesso. Questo oggetto non deve essere liberato. Per una discussione su quando chiamare la funzione, vedere [l'argomento rappresentare \_ come attributo](the-represent-as-attribute.md).

 

 




