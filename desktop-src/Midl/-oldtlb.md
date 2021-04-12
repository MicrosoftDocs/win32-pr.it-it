---
title: opzione/oldtlb
description: L'opzione/oldtlb indica al compilatore MIDL di generare una libreria dei tipi in formato obsoleto.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- /oldtlb switch MIDL
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a08e468d0acff16aa1df4a45fcacafeb676b00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398910"
---
# <a name="oldtlb-switch"></a>opzione/oldtlb

L'opzione **/oldtlb** indica al compilatore MIDL di generare una libreria dei tipi in formato obsoleto.

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

L'opzione **/oldtlb** esegue l'override del valore predefinito e indica al compilatore MIDL di generare librerie dei tipi obsolete anche nelle versioni correnti di Windows usando [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) anziché [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).

## <a name="examples"></a>Esempio

**MIDL/oldtlb nomefile. idl**

**MIDL/oldtlb myoldodl. FAD**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/newtlb**](-newtlb.md)
</dt> </dl>

 

 