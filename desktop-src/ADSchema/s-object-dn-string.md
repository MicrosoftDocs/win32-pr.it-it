---
title: Sintassi Object(DN-String)
description: Stringa ottetto che contiene un valore stringa e un DN.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- Schema AD della sintassi di Object(DN-String)
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18222343a5c10b7231d174021c8d4238ba075b66b648d99a704f4e1d1d651e2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580251"
---
# <a name="objectdn-string-syntax"></a>Sintassi Object(DN-String)

Stringa ottetto che contiene un valore stringa e un DN.



| Voce | Valore |
|--------------|------------------------------------------------------------------------------------|
| Nome         | Object(DN-String)                                                                  |
| ID sintassi    | 2.5.5.14                                                                           |
| OM ID        | 127                                                                                |
| Tipo MAPI    | \-                                                                                 |
| Tipo ADS     | ADSTYPE \_ DN \_ WITH \_ STRING                                                          |
| Tipo variant | VT \_ DISPATCH                                                                       |
| Tipo SDS     | Oggetto COM di cui è possibile eseguire il cast a [**un oggetto IADsDNWithString.**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring) |



## <a name="remarks"></a>Commenti

Un valore con questa sintassi ha il formato seguente:

``` syntax
S:<char count>:<string value>:<object DN>
```

dove " char count " è il numero di caratteri nella stringa " string value " e " object DN " è il nome distinto di un oggetto &lt; &gt; in Active &lt; &gt; &lt; &gt; Directory. Active Directory aggiorna il DN se l'oggetto a cui fa riferimento viene spostato o rinominato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
