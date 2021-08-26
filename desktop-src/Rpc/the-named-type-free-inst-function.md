---
title: Funzione named_type_free_inst
description: Gli stub chiamano la funzione inst del tipo denominato free per \_ \_ liberare la memoria \_ associata al tipo trasmesso.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa55e896b89fccc513795a62634e805c2ad6e21b7bdecdd99a0b9cfe2d71cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016890"
---
# <a name="the-named_type_free_inst-function"></a>Funzione \_ \_ inst del \_ tipo denominato free

Gli stub chiamano la **funzione \_ \_ \_ inst del** tipo denominato free per liberare la memoria associata al tipo trasmesso. La funzione è definita come:

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

Il parametro punta all'istanza del tipo trasmesso. Questo oggetto non deve essere liberato. Per informazioni su quando chiamare la funzione, vedere Rappresenta [ \_ come attributo](the-represent-as-attribute.md).

 

 




