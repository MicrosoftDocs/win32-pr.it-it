---
description: "TAGREF: contiene l'indice di una voce e le relative informazioni TAG in un database shim."
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf5a9de8da025e8278ab0bca7ccbe16d70d16b782591181f6ce6ce74a010a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075776"
---
# <a name="tagref"></a>TAGREF

Contiene l'indice di una voce e le relative informazioni TAG in un database shim.


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a>Commenti

Un **TAGREF** è specifico di un database shim e valido in più database. Può essere un valore intero che rappresenta l'indice o uno dei valori seguenti:

<dl> <dt>

<span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ NULL (0)
</dt> <dd>

**TAGREF** inesistente. Questo valore viene restituito da una funzione quando non può restituire un **TAGREF valido.**

</dd> <dt>

<span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>RADICE TAGREF \_ (0)
</dt> <dd>

Indica un TAG dell'elenco radice che può essere utilizzato come elemento padre per ottenere un **TAGREF figlio.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> <dt>

[**TAG**](tag.md)
</dt> <dt>

[Tipi TAG](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




