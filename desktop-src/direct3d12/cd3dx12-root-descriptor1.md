---
title: Struttura CD3DX12_ROOT_DESCRIPTOR1 (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura DESCRIPTOR1 radice D3D12.
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- Struttura CD3DX12_ROOT_DESCRIPTOR1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cb64509c82c11180ca3e1d2937dff5d077897d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323558"
---
# <a name="cd3dx12_root_descriptor1-structure"></a>\_ \_ Struttura DESCRIPTOR1 radice CD3DX12

Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ DESCRIPTOR1 radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_ROOT_DESCRIPTOR1  : public D3D12_ROOT_DESCRIPTOR1{
       CD3DX12_ROOT_DESCRIPTOR1();
       explicit CD3DX12_ROOT_DESCRIPTOR1(const D3D12_ROOT_DESCRIPTOR1 &o);
       CD3DX12_ROOT_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void static inline Init(D3D12_ROOT_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ radice \_ DESCRIPTOR1 ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ DESCRIPTOR1 radice CD3DX12 \_ .

</dd> <dt>

**Explicit CD3DX12 \_ root \_ DESCRIPTOR1 (const D3D12 \_ root \_ DESCRIPTOR1 &o)**
</dt> <dd>

Crea una nuova istanza di un \_ DESCRIPTOR1 radice CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura [**\_ \_ DESCRIPTOR1 radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .

</dd> <dt>

**CD3DX12 \_ root \_ DESCRIPTOR1 (uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descrittor Flags \_ = D3D12 \_ \_ flag descrittore radice \_ \_ None)**
</dt> <dd>

Crea una nuova istanza di un \_ DESCRIPTOR1 radice CD3DX12 \_ , inizializzando i parametri seguenti:

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None

</dd> <dt>

**inline init (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ radice \_ descrittore flag Flags \_ = D3D12 \_ radice \_ Descriptor \_ flag \_ None)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None

</dd> <dt>

**static inline init (D3D12 \_ radice \_ DESCRIPTOR1 &Table, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ radice \_ descrittore Flags \_ = D3D12 \_ \_ flag descrittore radice \_ \_ None)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_DESCRIPTOR1 radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &tabella

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_DESCRIPTOR1 radice \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





