---
title: Opzione /oldtlb
description: L'opzione /oldtlb indica al compilatore MIDL di generare una libreria dei tipi in formato precedente.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- Opzione /oldtlb MIDL
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b30a7bc905645523a81287eea2dfcdc408b8a4d172cc84282e0f1538e12cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895991"
---
# <a name="oldtlb-switch"></a>Opzione /oldtlb

**L'opzione /oldtlb** indica al compilatore MIDL di generare una libreria dei tipi in formato precedente.

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

L'opzione **/oldtlb** esegue l'override del valore predefinito e indica al compilatore MIDL di generare librerie dei tipi in formato precedente anche nelle versioni correnti di Windows usando [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) anziché [CreateTypeLib2.](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2)

## <a name="examples"></a>Esempio

**midl /oldtlb filename.idl**

**midl /oldtlb myoldodl.odl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/newtlb**](-newtlb.md)
</dt> </dl>

 

 