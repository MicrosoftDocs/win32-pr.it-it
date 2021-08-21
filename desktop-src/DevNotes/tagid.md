---
description: Contiene l'indice di una voce e le relative informazioni TAG in un database shim.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4c65183170c7304bf05a670b1eadb3a5953d6f33b1f6415210f12db8898760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075784"
---
# <a name="tagid"></a>TAGID

Contiene l'indice di una voce e le relative informazioni TAG in un database shim.


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a>Commenti

Un **TAGID** è specifico di un database. Può essere un valore intero che rappresenta l'indice o uno dei valori seguenti:

<dl> <dt>

<span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ NULL (0)
</dt> <dd>

**TAGID** inesistente. Questo valore viene restituito da una funzione quando non può restituire un **TAGID valido.**

</dd> <dt>

<span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TAGID \_ ROOT (0)
</dt> <dd>

Indica un TAG dell'elenco radice che può essere utilizzato come elemento padre per ottenere un **TAGID figlio.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TAG**](tag.md)
</dt> <dt>

[Tipi DI TAG](tag-types.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




