---
title: Struttura CD3DX12_ROOT_PARAMETER (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di \_ una \_ struttura di parametri radice D3D12.
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- Struttura CD3DX12_ROOT_PARAMETER
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322204"
---
# <a name="cd3dx12_root_parameter-structure"></a>\_Struttura di \_ parametri radice CD3DX12

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ parametri radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Parametro radice CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ parametro radice CD3DX12 \_ .

</dd> <dt>

**parametro radice CD3DX12 esplicito \_ \_ (parametro radice D3D12 const \_ \_ &o)**
</dt> <dd>

Crea una nuova istanza di un \_ parametro radice CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ parametri radice di D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .

</dd> <dt>

**static inline InitAsDescriptorTable ( \_ parametro radice D3D12 \_ &ROOTPARAM, uint numDescriptorRanges, CONSt D3D12 \_ descrittore \_ Range \* pDescriptorRanges, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

NumDescriptorRanges UINT

[**D3D12 \_ \_Intervallo DEscrittore**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges

consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**static inline InitAsConstants ( \_ parametro radice D3D12 \_ &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

Num32BitValues UINT

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**static inline InitAsConstantBufferView ( \_ parametro radice D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**static inline InitAsShaderResourceView ( \_ parametro radice D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**static inline InitAsUnorderedAccessView ( \_ parametro radice D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**inline InitAsDescriptorTable (UINT numDescriptorRanges, const D3D12 \_ Descriptor \_ Range \* pDescriptorRanges, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

NumDescriptorRanges UINT

[**D3D12 \_ \_Intervallo DEscrittore**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges

consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**inline InitAsConstants (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

Num32BitValues UINT

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**inline InitAsConstantBufferView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**inline InitAsShaderResourceView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> <dt>

**inline InitAsUnorderedAccessView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ shader \_ Visibility Visibility = D3D12 \_ shader \_ visibility \_ All)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

consenso esplicito [**D3D12 \_ Visibilità della \_ visibilità dello shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ shader \_ visibility \_ All

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Parametro radice \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





