---
title: Struttura CD3DX12_ROOT_DESCRIPTOR_TABLE1 (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura Tabella1 del descrittore radice D3D12 \_ .
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- Struttura CD3DX12_ROOT_DESCRIPTOR_TABLE1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3538e5e1e199fdb6f8c7473af4996ccd7b7f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323564"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a>\_ \_ Struttura Tabella1 del descrittore radice CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ \_ Tabella1 del descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Descrittore radice CD3DX12 \_ \_ Tabella1 ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ \_ descrittore radice CD3DX12 \_ Tabella1.

</dd> <dt>

**descrittore radice CD3DX12 esplicito \_ \_ \_ Tabella1 (const D3D12 \_ radice \_ descrittore \_ Tabella1 &o)**
</dt> <dd>

Crea una nuova istanza di un \_ \_ descrittore radice CD3DX12 \_ Tabella1, inizializzato con il contenuto di un'altra struttura [**\_ \_ \_ Tabella1 del descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .

</dd> <dt>

**\_Descrittore radice CD3DX12 \_ \_ Tabella1 (uint numDescriptorRanges, const D3D12 \_ descrittore \_ nell'intervallo 1 pDescriptorRanges \* \_ )**
</dt> <dd>

Crea una nuova istanza di un \_ \_ descrittore radice CD3DX12 \_ Tabella1, inizializzando i parametri seguenti:

NumDescriptorRanges UINT

[**\_ descrittore \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) const nell'intervallo 1 \* \_ pDescriptorRanges

</dd> <dt>

**inline init (UINT numDescriptorRanges, const D3D12 \_ Descriptor \_ nell'intervallo 1 \* \_ pDescriptorRanges)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

NumDescriptorRanges UINT

[**\_ descrittore \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) const nell'intervallo 1 \* \_ pDescriptorRanges

</dd> <dt>

**static inline init (D3D12 \_ root \_ descriptor \_ Tabella1 &RootDescriptorTable, uint numDescriptorRanges, const D3D12 \_ Descriptor \_ nell'intervallo 1 pDescriptorRanges \* \_ )**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_Descrittore radice \_ Tabella1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable

NumDescriptorRanges UINT

[**\_ descrittore \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) const nell'intervallo 1 \* \_ pDescriptorRanges

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Descrittore radice D3D12 \_ \_ Tabella1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





