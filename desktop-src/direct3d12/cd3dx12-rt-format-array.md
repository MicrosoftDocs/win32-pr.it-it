---
title: CD3DX12_RT_FORMAT_ARRAY struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura D3D12 \_ RT \_ FORMAT \_ ARRAY.
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- CD3DX12_RT_FORMAT_ARRAY struttura
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9c153b98e84176d2682f028657176902fb68ebc0e8e1e52c69c196842dc2fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988362"
---
# <a name="cd3dx12_rt_format_array-structure"></a>Struttura CD3DX12 \_ RT \_ FORMAT \_ ARRAY

Struttura helper per consentire una facile inizializzazione di [**una struttura D3D12 \_ RT FORMAT \_ \_ ARRAY.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ RT \_ FORMAT \_ ARRAY()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un OGGETTO CD3DX12 \_ RT \_ FORMAT \_ ARRAY.

</dd> <dt>

**EXPLICIT CD3DX12 \_ RT \_ FORMAT \_ ARRAY(const D3D12 \_ RT FORMAT ARRAY& \_ \_ o)**
</dt> <dd>

Crea una nuova istanza di cd3DX12 RT FORMAT ARRAY, inizializzata con valori copiati da una struttura \_ \_ \_ [**D3D12 \_ RT \_ FORMAT \_ ARRAY.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)

</dd> <dt>

**EXPLICIT CD3DX12 \_ RT \_ FORMAT \_ ARRAY(const DXGI \_ FORMAT \* pFormats, UINT NumFormats)**
</dt> <dd>

Crea una nuova istanza di CD3DX12 \_ RT \_ FORMAT ARRAY, inizializzata con i valori passati \_ nell'elenco di parametri. Il contenuto della matrice specificata dal *parametro pFormats* viene copiato nella matrice di membri **RTFormats**. Si presuppone che la matrice specificata da *pFormats* abbia le stesse dimensioni di **RTFormats**.

</dd> <dt>

**operator const D3D12 \_ RT \_ FORMAT ARRAY \_&() const**
</dt> <dd>

Conversione implicita in [**una struttura D3D12 \_ RT FORMAT \_ \_ ARRAY.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) Poiché D3D12 RT FORMAT ARRAY è il tipo sottostante di \_ \_ CD3DX12 DEPTH STENCIL DESC1, l'oggetto viene semplicemente restituito come riferimento \_ \_ \_ \_ const D3D12 RT FORMAT ARRAY a \_ \_ \_ se stesso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**MATRICE DI FORMATO D3D12 \_ RT \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





