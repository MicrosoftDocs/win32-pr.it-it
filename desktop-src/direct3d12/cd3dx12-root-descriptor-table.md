---
title: Struttura CD3DX12_ROOT_DESCRIPTOR_TABLE (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura di tabella del descrittore radice D3D12 \_ .
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- Struttura CD3DX12_ROOT_DESCRIPTOR_TABLE
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f675624526a959e6cf92172383b12590c36fc408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322206"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a>\_Struttura della \_ tabella descrittore radice CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ \_ tabella del descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_ \_ Tabella descrittore radice CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ \_ tabella del descrittore radice CD3DX12 \_ .

</dd> <dt>

**\_ \_ tabella descrittore radice CD3DX12 esplicita \_ ( \_ \_ tabella descrittore radice D3D12 const \_ &o)**
</dt> <dd>

Crea una nuova istanza di una \_ tabella del \_ descrittore radice CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura della [**\_ \_ \_ tabella del descrittore radice di D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .

</dd> <dt>

**\_ \_ Tabella descrittore radice CD3DX12 \_ (uint numDescriptorRanges, const D3D12 \_ Descriptor \_ Range \* \_ pDescriptorRanges)**
</dt> <dd>

Crea una nuova istanza di una \_ tabella del \_ descrittore radice CD3DX12 \_ , inizializzando i parametri seguenti:

NumDescriptorRanges UINT

[**D3D12 \_ \_Intervallo descrittore**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> <dt>

**inline init (UINT numDescriptorRanges, const D3D12 \_ Descriptor \_ Range \* \_ pDescriptorRanges)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

NumDescriptorRanges UINT

[**D3D12 \_ \_Intervallo descrittore**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> <dt>

**static inline init ( \_ \_ tabella descrittore radice D3D12 \_ &RootDescriptorTable, uint numDescriptorRanges, const D3D12 \_ Descriptor \_ Range \* \_ pDescriptorRanges)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_ \_ Tabella descrittore radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable

NumDescriptorRanges UINT

[**D3D12 \_ \_Intervallo descrittore**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ Tabella descrittore radice D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





