---
title: Struttura CD3DX12_DESCRIPTOR_RANGE1 (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura nell'intervallo 1 del descrittore D3D12 \_ .
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- Struttura CD3DX12_DESCRIPTOR_RANGE1
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
ms.openlocfilehash: 6386d8094d573fba9cd3af44b0148215ee621e2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322266"
---
# <a name="cd3dx12_descriptor_range1-structure"></a>\_Struttura nell'intervallo 1 del descrittore CD3DX12 \_

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura [**\_ \_ nell'intervallo 1 del descrittore D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .

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

**\_Descrittore CD3DX12 \_ nell'intervallo 1 ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ descrittore CD3DX12 \_ nell'intervallo 1.

</dd> <dt>

**descrittore CD3DX12 esplicito \_ \_ nell'intervallo 1 (CONSt D3D12 \_ descrittore \_ nell'intervallo 1 &o)**
</dt> <dd>

Crea una nuova istanza di un \_ descrittore CD3DX12 \_ nell'intervallo 1, inizializzato con il contenuto di un'altra struttura di [**\_ descrittore D3D12 \_ nell'intervallo 1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .

</dd> <dt>

**\_Descrittore CD3DX12 \_ nell'intervallo 1 ( \_ tipo di intervallo descrittore D3D12 \_ \_ RANGETYPE, uint descrittori numerici, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ descrittor range Flags Flags \_ \_ = D3D12 \_ descrittor \_ Range flag \_ \_ None, uint offsetInDescriptorsFromTableStart = D3D12 \_ descrittor \_ \_ offset \_ Append)**
</dt> <dd>

Crea una nuova istanza di un \_ descrittore CD3DX12 \_ nell'intervallo 1, inizializzando i parametri seguenti:

[**D3D12 \_ \_ \_ Tipo di intervallo descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

Descrittori numerici UINT

BaseShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Flag \_ intervallo \_ descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flag = D3D12 \_ flag intervallo descrittore \_ \_ \_ None

UINT offsetInDescriptorsFromTableStart = D3D12 \_ descrittore \_ \_ offset intervallo \_

</dd> <dt>

**inline init ( \_ tipo di intervallo descrittore D3D12 \_ \_ RangeType, UINT descrittori numerici, UINT BaseShaderRegister, uint registerSpace = 0, D3D12 \_ Descriptor \_ Range FLAGs Flags \_ = D3D12 \_ descrittor \_ Range flag \_ \_ None, uint offsetInDescriptorsFromTableStart = D3D12 \_ descrittor \_ \_ offset intervallo \_ )**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_ \_ Tipo di intervallo descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

Descrittori numerici UINT

BaseShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Flag \_ intervallo \_ descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flag = D3D12 \_ flag intervallo descrittore \_ \_ \_ None

UINT offsetInDescriptorsFromTableStart = D3D12 \_ descrittore \_ \_ offset intervallo \_

</dd> <dt>

**static inline init (D3D12 \_ descrittor \_ nell'intervallo 1 &Range, D3D12 \_ descrittor \_ Range \_ Type RANGETYPE, uint descrittori numerici, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ descrittor \_ Range \_ Flags Flags = D3D12 \_ descrittor \_ Range \_ flag \_ None, uint offsetInDescriptorsFromTableStart = D3D12 \_ descrittor \_ \_ offset range \_ Append)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ Descrittore \_ nell'intervallo 1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &intervallo

[**D3D12 \_ \_ \_ Tipo di intervallo descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

Descrittori numerici UINT

BaseShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Flag \_ intervallo \_ descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flag = D3D12 \_ flag intervallo descrittore \_ \_ \_ None

UINT offsetInDescriptorsFromTableStart = D3D12 \_ descrittore \_ \_ offset intervallo \_

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Descrittore D3D12 \_ nell'intervallo 1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





