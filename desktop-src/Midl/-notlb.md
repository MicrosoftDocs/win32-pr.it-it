---
title: Opzione /notlb
description: L'opzione /notlb impedisce al compilatore MIDL di generare un file di libreria dei tipi (TLB).
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- Opzione /notlb MIDL
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e309ed753d1549c31c9e3dea0a5c7aa87b32217aa12e5ee04934a183927adf87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067521"
---
# <a name="notlb-switch"></a>Opzione /notlb

**L'opzione /notlb** impedisce al compilatore MIDL di generare un file di libreria dei tipi (TLB).

``` syntax
midl /notlb
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il compilatore MIDL genererà un file TLB ogni volta che rileva [**un'istruzione LIBRARY.**](library.md) Questa opzione esegue l'override del comportamento predefinito.

Quando si **specifica l'opzione /notlb,** tutti gli altri stub, intestazioni e così via vengono generati come di consueto.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/tlb**](-tlb.md)
</dt> </dl>

 

 




