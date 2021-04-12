---
description: Contiene l'indice di una voce e le relative informazioni sui TAG in un database di shim.
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8631811f101850b68bdbad1097c19b9a41737bd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523153"
---
# <a name="tagref"></a>TAGREF

Contiene l'indice di una voce e le relative informazioni sui TAG in un database di shim.


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a>Commenti

Un **TAGREF** è specifico di un database di shim e valido tra più database. Può essere un valore intero che rappresenta l'indice o uno dei valori seguenti:

<dl> <dt>

<span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ null (0)
</dt> <dd>

Il **TAGREF** non esiste. Questo valore viene restituito da una funzione quando non può restituire un **TAGREF** valido.

</dd> <dt>

<span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>\_Radice TAGREF (0)
</dt> <dd>

Indica un TAG dell'elenco radice che può essere utilizzato come elemento padre per ottenere un **TAGREF** figlio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> <dt>

[**TAG**](tag.md)
</dt> <dt>

[Tipi di TAG](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




