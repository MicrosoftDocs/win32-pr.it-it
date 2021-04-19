---
title: Struttura CD3DX12_ROOT_PARAMETER1 (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura PARAMETRO1 radice D3D12.
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- Struttura CD3DX12_ROOT_PARAMETER1
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
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323556"
---
# <a name="cd3dx12_root_parameter1-structure"></a>\_ \_ Struttura PARAMETRO1 radice CD3DX12

Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ parametro1 radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .

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

**CD3DX12 \_ radice \_ parametro1 ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ parametro1 radice CD3DX12 \_ .

</dd> <dt>

**Explicit CD3DX12 \_ root \_ parametro1 (const D3D12 \_ root \_ parametro1 &o)**
</dt> <dd>

Crea una nuova istanza di un \_ parametro1 radice CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura [**\_ \_ parametro1 radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .

</dd> <dt>

**static inline InitAsDescriptorTable (D3D12 \_ root \_ parametro1 &ROOTPARAM, uint numDescriptorRanges, const D3D12 \_ Descriptor \_ nell'intervallo 1 \* pDescriptorRanges, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ RADICE \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

NumDescriptorRanges UINT

[**\_ descrittore \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) const nell'intervallo 1 \* pDescriptorRanges

[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**static inline InitAsConstants (D3D12 \_ root \_ parametro1 &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ RADICE \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

Num32BitValues UINT

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**static inline InitAsConstantBufferView (D3D12 \_ root \_ parametro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descrittor Flags \_ = D3D12 \_ \_ flag descrittore radice \_ \_ None, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ RADICE \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None

[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**static inline InitAsShaderResourceView (D3D12 \_ root \_ parametro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descrittor Flags \_ = D3D12 \_ \_ flag descrittore radice \_ \_ None, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ RADICE \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None

[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**static inline InitAsUnorderedAccessView (D3D12 \_ root \_ parametro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descrittor Flags \_ = D3D12 \_ \_ flag descrittore radice \_ \_ None, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ RADICE \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None

[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**inline InitAsDescriptorTable (UINT numDescriptorRanges, const D3D12 \_ Descriptor \_ nell'intervallo 1 \* pDescriptorRanges, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

NumDescriptorRanges UINT

[**\_ descrittore \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) const nell'intervallo 1 \* pDescriptorRanges

[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**inline InitAsConstants (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

Num32BitValues UINT

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**inline InitAsConstantBufferView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ radice \_ descrittore flag Flags \_ = D3D12 \_ radice \_ descrittore flag \_ \_ None, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None

[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**inline InitAsShaderResourceView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ radice \_ descrittore flag Flags \_ = D3D12 \_ radice \_ descrittore flag \_ \_ None, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None

[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**inline InitAsUnorderedAccessView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ radice \_ descrittore flag Flags \_ = D3D12 \_ radice \_ descrittore flag \_ \_ None, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Flag \_ descrittore \_ radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = D3D12 \_ radice \_ descrittore flag \_ \_ None

[**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Parametro1 radice \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





