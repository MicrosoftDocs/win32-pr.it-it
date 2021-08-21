---
title: CD3DX12_ROOT_PARAMETER1 struttura (D3dx12.h)
description: Struttura helper per consentire l'inizializzazione semplice di una struttura D3D12 \_ ROOT \_ PARAMETER1.
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- CD3DX12_ROOT_PARAMETER1 struttura
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8530e913b96255050aa5c8cd15a025d0cf894b38b8c84833bfd3e4e22bc9db50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912842"
---
# <a name="cd3dx12_root_parameter1-structure"></a>Struttura CD3DX12 \_ ROOT \_ PARAMETER1

Struttura helper per consentire l'inizializzazione semplice di [**una struttura D3D12 \_ ROOT \_ PARAMETER1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ ROOT \_ PARAMETER1()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un PARAMETRO RADICE1 CD3DX12. \_ \_

</dd> <dt>

**explicit CD3DX12 \_ ROOT \_ PARAMETER1(const D3D12 \_ ROOT \_ PARAMETER1 &o)**
</dt> <dd>

Crea una nuova istanza di un oggetto CD3DX12 ROOT PARAMETER1, inizializzato con il contenuto di \_ \_ un'altra struttura [**D3D12 \_ ROOT \_ PARAMETER1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

</dd> <dt>

**static inline InitAsDescriptorTable(D3D12 \_ ROOT \_ PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* pDescriptorRanges, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT numDescriptorRanges

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges

[**D3D12 \_ VISIBILITÀ \_ SHADER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ SHADER VISIBILITY \_ \_ ALL

</dd> <dt>

**static inline InitAsConstants(D3D12 \_ ROOT \_ PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT num32BitValues

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ VISIBILITÀ \_ SHADER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ SHADER VISIBILITY \_ \_ ALL

</dd> <dt>

**static inline InitAsConstantBufferView(D3D12 \_ ROOT \_ PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT \_ DESCRIPTOR FLAGS flags = \_ D3D12 \_ ROOT \_ DESCRIPTOR FLAG \_ \_ NONE, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ FLAG \_ DI DESCRIZIONE \_ RADICE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT \_ DESCRIPTOR FLAG \_ \_ NONE

[**D3D12 \_ VISIBILITÀ \_ SHADER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ SHADER VISIBILITY \_ \_ ALL

</dd> <dt>

**static inline InitAsShaderResourceView(D3D12 \_ ROOT \_ PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT \_ DESCRIPTOR FLAGS flags = \_ D3D12 \_ ROOT \_ DESCRIPTOR FLAG \_ \_ NONE, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ FLAG \_ DI DESCRIZIONE \_ RADICE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT \_ DESCRIPTOR FLAG \_ \_ NONE

[**D3D12 \_ VISIBILITÀ \_ SHADER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ SHADER VISIBILITY \_ \_ ALL

</dd> <dt>

**static inline InitAsUnorderedAccessView(D3D12 \_ ROOT \_ PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT \_ DESCRIPTOR FLAGS flags = \_ D3D12 \_ ROOT \_ DESCRIPTOR FLAG \_ \_ NONE, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ FLAG \_ DI DESCRIZIONE \_ RADICE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT \_ DESCRIPTOR FLAG \_ \_ NONE

[**D3D12 \_ VISIBILITÀ \_ SHADER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ SHADER VISIBILITY \_ \_ ALL

</dd> <dt>

**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* pDescriptorRanges, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

UINT numDescriptorRanges

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges

[**D3D12 \_ VISIBILITÀ \_ SHADER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ SHADER VISIBILITY \_ \_ ALL

</dd> <dt>

**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

UINT num32BitValues

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ VISIBILITÀ \_ SHADER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ SHADER VISIBILITY \_ \_ ALL

</dd> <dt>

**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT \_ DESCRIPTOR \_ FLAGS flags = D3D12 \_ ROOT \_ DESCRIPTOR FLAG \_ \_ NONE, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ FLAG \_ DI DESCRIZIONE \_ RADICE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT \_ DESCRIPTOR FLAG \_ \_ NONE

[**D3D12 \_ VISIBILITÀ \_ SHADER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ SHADER VISIBILITY \_ \_ ALL

</dd> <dt>

**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT \_ DESCRIPTOR \_ FLAGS flags = D3D12 \_ ROOT \_ DESCRIPTOR FLAG \_ \_ NONE, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ FLAG \_ DI DESCRIZIONE \_ RADICE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT \_ DESCRIPTOR FLAG \_ \_ NONE

[**D3D12 \_ VISIBILITÀ \_ SHADER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ SHADER VISIBILITY \_ \_ ALL

</dd> <dt>

**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT \_ DESCRIPTOR \_ FLAGS flags = D3D12 \_ ROOT \_ DESCRIPTOR FLAG \_ \_ NONE, D3D12 \_ SHADER VISIBILITY = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ FLAG \_ DI DESCRIZIONE \_ RADICE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT \_ DESCRIPTOR FLAG \_ \_ NONE

[**D3D12 \_ VISIBILITÀ \_ SHADER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ SHADER VISIBILITY \_ \_ ALL

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





