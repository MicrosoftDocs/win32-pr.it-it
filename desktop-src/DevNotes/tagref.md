---
description: "TAGREF: contiene l'indice di una voce e le relative informazioni TAG in un database shim."
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e27a60847630e7bbd8e07ccf005dfd7b474d7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096629"
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

**TAGREF** inesistente. Questo valore viene restituito da una funzione quando non può restituire un **tag TAGREF valido.**

</dd> <dt>

<span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF \_ ROOT (0)
</dt> <dd>

Indica un TAG dell'elenco radice che può essere usato come elemento padre per ottenere un **TAGREF figlio.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> <dt>

[**TAG**](tag.md)
</dt> <dt>

[Tipi DI TAG](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




