---
title: D3DX11_STATE_BLOCK_MASK struttura (D3dx11effect.h)
description: Indica lo stato del dispositivo.
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- D3DX11_STATE_BLOCK_MASK struttura Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_STATE_BLOCK_MASK
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8087f45ad94fe3e45f78a1be9d86b30f6f7e3f2c9161b9c4498865b12582436e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124936"
---
# <a name="d3dx11_state_block_mask-structure"></a>Struttura D3DX11 \_ STATE \_ BLOCK \_ MASK

Indica lo stato del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DX11_STATE_BLOCK_MASK {
  BYTE VS;
  BYTE VSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE VSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE VSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE VSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE HS;
  BYTE HSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE HSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE HSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE HSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE DS;
  BYTE DSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE DSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE DSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE DSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE GS;
  BYTE GSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE GSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE GSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE GSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PS;
  BYTE PSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE PSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE PSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE PSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PSUnorderedAccessViews;
  BYTE CS;
  BYTE CSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE CSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE CSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE CSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE CSUnorderedAccessViews;
  BYTE IAVertexBuffers[D3DX11_BYTES_FROM_BITS(D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE IAIndexBuffer;
  BYTE IAInputLayout;
  BYTE IAPrimitiveTopology;
  BYTE OMRenderTargets;
  BYTE OMDepthStencilState;
  BYTE OMBlendState;
  BYTE RSViewports;
  BYTE RSScissorRects;
  BYTE RSRasterizerState;
  BYTE SOBuffers;
  BYTE Predication;
} D3DX11_STATE_BLOCK_MASK;
```



## <a name="members"></a>Members

<dl> <dt>

**Vs**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato del vertex shader.

</dd> <dt>

**VsSamplers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di campionatori di vertex shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di campionamento.

</dd> <dt>

**VsShaderResources**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di risorse vertex shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**VSConstantBuffers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer costanti vertex shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di buffer costante.

</dd> <dt>

**Interfacce VSInterface**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di interfacce vertex shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di interfaccia.

</dd> <dt>

**Hs**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato dello hull shader.

</dd> <dt>

**HSSamplers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di campionatori di hull shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di campionamento.

</dd> <dt>

**HSShaderResources**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di risorse di tipo hull shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**HSConstantBuffers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer costanti di hull shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di buffer costante.

</dd> <dt>

**Interfacce HS**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di interfacce di hull shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di interfaccia.

</dd> <dt>

**DS**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato dello shader del dominio.

</dd> <dt>

**DSSamplers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di campionatori domain-shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di campionamento.

</dd> <dt>

**DSShaderResources**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di risorse domain shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**DSConstantBuffers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer costanti domain-shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot del buffer.

</dd> <dt>

**Interfacce DS**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di interfacce domain-shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di interfaccia.

</dd> <dt>

**GS**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato dello shader geometrico.

</dd> <dt>

**GSSamplers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di campionatori geometry shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di campionamento.

</dd> <dt>

**GSShaderResources**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di risorse geometry shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**GSConstantBuffers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer costanti geometry shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot del buffer.

</dd> <dt>

**Interfacce GS**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di interfacce geometry shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di interfaccia.

</dd> <dt>

**Ps**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo pixel shader stato.

</dd> <dt>

**PSSamplers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di campionatori di pixel shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di campionamento.

</dd> <dt>

**PSShaderResources**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di risorse pixel shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**PSConstantBuffers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer costanti pixel shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di buffer costante.

</dd> <dt>

**Interfacce PSInterface**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di interfacce pixel shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di interfaccia.

</dd> <dt>

**PSUnorderedAccessViews**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare il pixel shader viste di accesso non ordinate.

</dd> <dt>

**CS**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato del compute shader.

</dd> <dt>

**CSSamplers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di campionatori compute shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di campionamento.

</dd> <dt>

**CSShaderResources**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di risorse compute shader. La matrice è una maschera di bit multi-byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**CSConstantBuffers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer costanti compute shader. La matrice è una maschera di bit multi-byte in cui ogni bit rappresenta uno slot di buffer costante.

</dd> <dt>

**Interfacce CSInterfaces**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di interfacce compute shader. La matrice è una maschera di bit multi byte in cui ogni bit rappresenta uno slot di interfaccia.

</dd> <dt>

**CSUnorderedAccessViews**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare le visualizzazioni di accesso non ordinate del compute shader.

</dd> <dt>

**IAVertexBuffers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer dei vertici. La matrice è una maschera di bit multi-byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**IAIndexBuffer**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo index buffer stato.

</dd> <dt>

**IAInputLayout**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato del layout di input.

</dd> <dt>

**IAPrimitiveTopology**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato della topologia primitiva.

</dd> <dt>

**OMRenderTargets**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare gli stati delle destinazioni di rendering.

</dd> <dt>

**OMDepthStencilState**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato depth-stencil.

</dd> <dt>

**OMBlendState**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato di blend.

</dd> <dt>

**RSViewports**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare gli stati dei viewport.

</dd> <dt>

**RSScissorRects**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare gli stati dei rettangoli di forbice.

</dd> <dt>

**RSRasterizerState**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato di rasterizzazione.

</dd> <dt>

**SOBuffers**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare gli stati dei buffer di flusso in uscita.

</dd> <dt>

**Predicazione**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato del predicato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una maschera di blocco di stato indica che il dispositivo indica che un passaggio o una tecnica cambia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Effetti 11 Strutture](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

