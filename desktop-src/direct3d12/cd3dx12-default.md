---
title: CD3DX12_DEFAULT struttura (D3dx12.h)
description: Passa D3D12 \_ DEFAULT in un costruttore per ogni struttura helper. Questa struttura viene semplicemente usata come meccanismo per impostare i parametri predefiniti nelle altre strutture helper.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- CD3DX12_DEFAULT struttura
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 876fbb5e666680e85854196fb9136bfd4d765d6eecf8f16bf6101bb321a7039a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531288"
---
# <a name="cd3dx12_default-structure"></a>Struttura CD3DX12 \_ DEFAULT

Passa D3D12 \_ DEFAULT in un costruttore per ogni struttura helper. Questa struttura viene semplicemente usata come meccanismo per impostare i parametri predefiniti nelle altre strutture helper.

## <a name="remarks"></a>Commenti

Questo struct viene dichiarato come segue:

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

Passa D3D12 \_ DEFAULT in un costruttore per ogni struct helper. Ad esempio, il costruttore seguente viene dichiarato in d3dx12.h:

HANDLE DESCRITTORE \_ CPU CD3DX12(CD3DX12 \_ \_ \_ DEFAULT) { ptr = 0; }

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





