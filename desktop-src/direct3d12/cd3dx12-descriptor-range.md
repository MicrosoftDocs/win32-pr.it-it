---
title: Struttura CD3DX12_DESCRIPTOR_RANGE (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura di intervallo descrittore D3D12 \_ .
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- Struttura CD3DX12_DESCRIPTOR_RANGE
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
ms.openlocfilehash: b511af1766daaefa7f92d33b71841b3a69c99927
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322269"
---
# <a name="cd3dx12_descriptor_range-structure"></a>\_Struttura dell'intervallo descrittore CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ intervallo descrittore D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .

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

**\_Intervallo descrittore CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ intervallo di descrittori D3DX12 \_ .

</dd> <dt>

**\_intervallo descrittore CD3DX12 esplicito \_ ( \_ intervallo descrittore const D3D12 \_ &o)**
</dt> <dd>

Crea una nuova istanza di un \_ intervallo di descrittori D3DX12 \_ , inizializzato con il contenuto di un'altra struttura di [**\_ \_ intervallo descrittore D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .

</dd> <dt>

**\_Intervallo descrittore CD3DX12 (D3D12 descrittor \_ \_ \_ \_ Type RANGETYPE, uint descrittori numerici, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ descrittor \_ \_ offset range \_ Append)**
</dt> <dd>

Crea una nuova istanza di un \_ intervallo di descrittori D3DX12 \_ , inizializzando i parametri seguenti:

[**D3D12 \_ \_ \_ Tipo di intervallo descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

Descrittori numerici UINT

BaseShaderRegister UINT

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ descrittore \_ \_ offset intervallo \_

</dd> <dt>

**inline init ( \_ tipo di intervallo descrittore D3D12 \_ \_ RangeType, UINT descrittori numerici, UINT BaseShaderRegister, uint registerSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ descrittor \_ \_ offset range \_ Append)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_ \_ Tipo di intervallo descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

Descrittori numerici UINT

BaseShaderRegister UINT

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ descrittore \_ \_ offset intervallo \_

</dd> <dt>

**static inline init (D3D12 \_ descrittor range \_ &Range, D3D12 \_ Descriptor \_ Range \_ Type RANGETYPE, uint descrittori numerici, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ descrittor \_ \_ offset range \_ Append)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ Intervallo \_ &di DEscrittori**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)

[**D3D12 \_ \_ \_ Tipo di intervallo descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

Descrittori numerici UINT

BaseShaderRegister UINT

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ descrittore \_ \_ offset intervallo \_

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Intervallo descrittore D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





