---
title: CD3DX12_DESCRIPTOR_RANGE struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura DESCRIPTOR RANGE D3D12. \_ \_
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- CD3DX12_DESCRIPTOR_RANGE struttura
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 641afe973c89d66257a8fc7b46defe2e77d8a8667094448ef58ab4beb2839b8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989941"
---
# <a name="cd3dx12_descriptor_range-structure"></a>Struttura CD3DX12 \_ DESCRIPTOR \_ RANGE

Struttura helper per consentire una facile inizializzazione di [**una struttura \_ DESCRIPTOR \_ RANGE D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un DESCRIPTOR RANGE D3DX12. \_ \_

</dd> <dt>

**EXPLICIT CD3DX12 \_ DESCRIPTOR \_ RANGE(const D3D12 \_ DESCRIPTOR \_ RANGE &o)**
</dt> <dd>

Crea una nuova istanza di un DESCRIPTOR RANGE D3DX12, inizializzata con il contenuto di un'altra struttura \_ \_ [**D3D12 \_ DESCRIPTOR \_ RANGE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)

</dd> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE(D3D12 \_ DESCRIPTOR \_ RANGE TYPE \_ TypeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR RANGE OFFSET \_ \_ \_ APPEND)**
</dt> <dd>

Crea una nuova istanza di un DESCRIPTOR RANGE D3DX12, \_ \_ inizializzando i parametri seguenti:

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UiNT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**inline Init(D3D12 \_ DESCRIPTOR \_ RANGE TYPE \_ rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR RANGE OFFSET \_ \_ \_ APPEND)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UiNT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**static inline Init(D3D12 \_ DESCRIPTOR \_ RANGE &range, D3D12 \_ DESCRIPTOR RANGE TYPE \_ \_ rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR RANGE OFFSET \_ \_ \_ APPEND)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**D3D12 \_ INTERVALLO \_ DESCRITTORE &**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) intervallo

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UiNT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INTERVALLO DESCRITTORE D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





