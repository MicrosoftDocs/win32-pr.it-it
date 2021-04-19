---
title: Struttura CD3DX12_DEFAULT (D3dx12. h)
description: Passa \_ il valore predefinito di D3D12 in un costruttore per ogni struttura helper. Questa struttura viene semplicemente utilizzata come meccanismo per impostare i parametri predefiniti sulle altre strutture di supporto.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- Struttura CD3DX12_DEFAULT
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
ms.openlocfilehash: b010e8f0fdce67f16750d0f66d1cf272c8ddb849
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322279"
---
# <a name="cd3dx12_default-structure"></a>\_Struttura predefinita CD3DX12

Passa \_ il valore predefinito di D3D12 in un costruttore per ogni struttura helper. Questa struttura viene semplicemente utilizzata come meccanismo per impostare i parametri predefiniti sulle altre strutture di supporto.

## <a name="remarks"></a>Commenti

Questa struct viene dichiarata come segue:

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

Passa \_ il valore predefinito di D3D12 in un costruttore per ogni struct helper. Ad esempio, il costruttore seguente viene dichiarato in d3dx12. h:

\_ \_ Handle descrittore CPU CD3DX12 \_ ( \_ valore predefinito CD3DX12) {ptr = 0;}

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





