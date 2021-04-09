---
description: Contiene l'indice di una voce e le relative informazioni sui TAG in un database di shim.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7d8b8a25633d3505936d105b0eef7ed38746ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966005"
---
# <a name="tagid"></a>TAGID

Contiene l'indice di una voce e le relative informazioni sui TAG in un database di shim.


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a>Commenti

Un **TagId** è specifico di un database. Può essere un valore intero che rappresenta l'indice o uno dei valori seguenti:

<dl> <dt>

<span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ null (0)
</dt> <dd>

Il **TagId** non esiste. Questo valore viene restituito da una funzione quando non può restituire un **TagId** valido.

</dd> <dt>

<span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>\_Radice TagId (0)
</dt> <dd>

Indica un TAG dell'elenco radice che può essere utilizzato come elemento padre per ottenere un **TagId** figlio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TAG**](tag.md)
</dt> <dt>

[Tipi di TAG](tag-types.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




