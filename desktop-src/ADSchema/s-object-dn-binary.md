---
title: Sintassi Object (DN-Binary)
description: Stringa di ottetto che contiene un valore binario e un nome distinto (DN).
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Schema di AD Object (DN-Binary) per la sintassi
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104121786"
---
# <a name="objectdn-binary-syntax"></a>Sintassi Object (DN-Binary)

Stringa di ottetto che contiene un valore binario e un nome distinto (DN).



| Voce | Valore |
|--------------|------------------------------------------------------------------------------------|
| Nome         | Object(DN-Binary)                                                                  |
| ID sintassi    | 2.5.5.7                                                                            |
| ID OM        | 127                                                                                |
| Tipo MAPI    | TSTRING                                                                            |
| Tipo di annunci     | \_DN ADSTYPE \_ con \_ binario                                                          |
| Tipo Variant | \_invio VT                                                                       |
| Tipo SDS     | Oggetto COM di cui è possibile eseguire il cast a un [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary). |



## <a name="remarks"></a>Commenti

Un valore con questa sintassi ha il formato seguente:

``` syntax
B:<char count>:<binary value>:<object DN>
```

dove " &lt; char count &gt; " è il numero di cifre esadecimali in " &lt; Binary value &gt; ", " &lt; Binary value &gt; " è la rappresentazione esadecimale del valore binario e " &lt; Object DN &gt; " è un nome distinto. Active Directory aggiorna automaticamente il DN se l'oggetto a cui fa riferimento è stato spostato o rinominato. Per ulteriori informazioni e un esempio di codice in cui viene utilizzata questa sintassi, vedere [Abilitazione dell'associazione Rinomina-safe con la proprietà otherWellKnownObjects archiviato nel](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
