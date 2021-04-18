---
title: Sintassi Object (DN-String)
description: Stringa di ottetto che contiene un valore stringa e un DN.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- Sintassi dell'oggetto (DN-String) AD schema
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302848"
---
# <a name="objectdn-string-syntax"></a>Sintassi Object (DN-String)

Stringa di ottetto che contiene un valore stringa e un DN.



| Voce | Valore |
|--------------|------------------------------------------------------------------------------------|
| Nome         | Object(DN-String)                                                                  |
| ID sintassi    | 2.5.5.14                                                                           |
| ID OM        | 127                                                                                |
| Tipo MAPI    | \-                                                                                 |
| Tipo di annunci     | \_DN ADSTYPE \_ con \_ stringa                                                          |
| Tipo Variant | \_invio VT                                                                       |
| Tipo SDS     | Oggetto COM di cui è possibile eseguire il cast a un [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring). |



## <a name="remarks"></a>Commenti

Un valore con questa sintassi ha il formato seguente:

``` syntax
S:<char count>:<string value>:<object DN>
```

dove " &lt; char count &gt; " è il numero di caratteri nella stringa " &lt; Value String &gt; " e " &lt; Object DN &gt; " è un nome distinto di un oggetto in Active Directory. Active Directory aggiorna il DN se l'oggetto a cui fa riferimento è stato spostato o rinominato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
