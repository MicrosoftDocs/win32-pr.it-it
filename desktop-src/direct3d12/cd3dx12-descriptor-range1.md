---
title: CD3DX12_DESCRIPTOR_RANGE1 struttura (D3dx12.h)
description: Struttura helper per consentire l'inizializzazione semplificata di una struttura \_ DESCRIPTOR RANGE1 D3D12. \_
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- CD3DX12_DESCRIPTOR_RANGE1 struttura
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 404cb41a019dac404bbe351f78f1d1e65277dd9ad2aecf2cc2d94d06fe242f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989881"
---
# <a name="cd3dx12_descriptor_range1-structure"></a>Struttura CD3DX12 \_ DESCRIPTOR \_ RANGE1

Struttura helper per consentire l'inizializzazione semplificata di [**una struttura \_ DESCRIPTOR \_ RANGE1 D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE1()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un descrittore RANGE1 CD3DX12. \_ \_

</dd> <dt>

**explicit CD3DX12 \_ DESCRIPTOR \_ RANGE1(const D3D12 \_ DESCRIPTOR \_ RANGE1 &o)**
</dt> <dd>

Crea una nuova istanza di un DESCRIPTOR RANGE1 CD3DX12, inizializzato con il contenuto di \_ \_ un'altra struttura [**D3D12 \_ DESCRIPTOR \_ RANGE1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)

</dd> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE1(D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS flags = D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAG \_ NONE, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND)**
</dt> <dd>

Crea una nuova istanza di un descrittore CD3DX12 \_ \_ RANGE1, inizializzando i parametri seguenti:

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_ FLAG DI \_ INTERVALLO \_ DESCRITTORE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = D3D12 \_ DESCRIPTOR \_ RANGE FLAG \_ \_ NONE

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**inline Init(D3D12 \_ DESCRIPTOR \_ RANGE TYPE \_ rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12 \_ DESCRIPTOR RANGE FLAGS flags = \_ \_ D3D12 \_ DESCRIPTOR RANGE FLAG \_ \_ \_ NONE, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR RANGE OFFSET \_ \_ \_ APPEND)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_ FLAG DI \_ INTERVALLO \_ DESCRITTORE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = D3D12 \_ DESCRIPTOR \_ RANGE FLAG \_ \_ NONE

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**static inline Init(D3D12 \_ DESCRIPTOR \_ RANGE1 &range, D3D12 \_ DESCRIPTOR \_ RANGE TYPE \_ rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12 \_ \_ DESCRIPTOR RANGE FLAGS flags = \_ D3D12 \_ DESCRIPTOR RANGE FLAG \_ \_ \_ NONE, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR RANGE OFFSET \_ \_ \_ APPEND)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**D3D12 \_ Intervallo di &DESCRITTORE \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_ FLAG DI \_ INTERVALLO \_ DESCRITTORE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = D3D12 \_ DESCRIPTOR \_ RANGE FLAG \_ \_ NONE

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





