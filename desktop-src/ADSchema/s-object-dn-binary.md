---
title: Sintassi Object(DN-Binary)
description: Stringa ottetto che contiene un valore binario e un nome distinto (DN).
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Schema AD della sintassi di Object(DN-Binary)
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15172a8577cf8ccec71053c3d374b389d71d3264fcc1934b19440a3f9efc4904
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702571"
---
# <a name="objectdn-binary-syntax"></a>Sintassi Object(DN-Binary)

Stringa ottetto che contiene un valore binario e un nome distinto (DN).



| Voce | Valore |
|--------------|------------------------------------------------------------------------------------|
| Nome         | Object(DN-Binary)                                                                  |
| ID sintassi    | 2.5.5.7                                                                            |
| OM ID        | 127                                                                                |
| Tipo MAPI    | TSTRING                                                                            |
| Tipo ADS     | ADSTYPE \_ DN \_ CON BINARY \_                                                          |
| Tipo variant | VT \_ DISPATCH                                                                       |
| Tipo SDS     | Oggetto COM di cui è possibile eseguire il cast a [**un oggetto IADsDNWithBinary.**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary) |



## <a name="remarks"></a>Commenti

Un valore con questa sintassi ha il formato seguente:

``` syntax
B:<char count>:<binary value>:<object DN>
```

dove " char count " è il numero di cifre esadecimali in " valore binario ", " valore binario " è la rappresentazione esadecimale del valore binario e " DN oggetto " è un nome &lt; &gt; &lt; &gt; &lt; &gt; &lt; &gt; distinto. Active Directory aggiorna automaticamente il DN se l'oggetto a cui fa riferimento viene spostato o rinominato. Per altre informazioni e un esempio di codice che usa questa sintassi, vedere Abilitazione dell'associazione indipendente dalla ridenominazione con la proprietà [otherWellKnownObjects](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
