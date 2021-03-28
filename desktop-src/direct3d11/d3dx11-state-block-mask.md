---
title: Struttura D3DX11_STATE_BLOCK_MASK (D3dx11effect. h)
description: Indica lo stato del dispositivo.
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- Struttura D3DX11_STATE_BLOCK_MASK Direct3D 11
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
ms.openlocfilehash: 41236c541fc251902a7a0a5ad6030a28dd36e3a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355359"
---
# <a name="d3dx11_state_block_mask-structure"></a>\_Struttura della \_ maschera di blocco dello stato D3DX11 \_

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

**VS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato del vertex shader.

</dd> <dt>

**VSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di Sampler vertex shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del campionatore.

</dd> <dt>

**VSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di risorse vertex shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**VSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer costanti del vertex shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del buffer costante.

</dd> <dt>

**VSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di interfacce vertex shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di interfaccia.

</dd> <dt>

**HS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato di Hull shader.

</dd> <dt>

**HSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di Sampler di Hull shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del campionatore.

</dd> <dt>

**HSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di risorse dello shader Hull. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**HSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer costanti dello shader Hull. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del buffer costante.

</dd> <dt>

**HSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di interfacce dello shader Hull. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di interfaccia.

</dd> <dt>

**DS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato del Domain shader.

</dd> <dt>

**DSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di Sampler di Domain shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del campionatore.

</dd> <dt>

**DSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di risorse dello shader di dominio. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**DSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer di costanti dello shader di dominio. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del buffer.

</dd> <dt>

**DSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di interfacce dello shader di dominio. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di interfaccia.

</dd> <dt>

**GS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato di Geometry shader.

</dd> <dt>

**GSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di Sampler geometry shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del campionatore.

</dd> <dt>

**GSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di risorse dello shader di geometria. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**GSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer costanti dello shader di geometria. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del buffer.

</dd> <dt>

**GSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di interfacce di shader Geometry. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di interfaccia.

</dd> <dt>

**PS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato del pixel shader.

</dd> <dt>

**PSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di Sampler pixel shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del campionatore.

</dd> <dt>

**PSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di risorse pixel shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**PSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer costanti pixel shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del buffer costante.

</dd> <dt>

**PSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di interfacce pixel shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di interfaccia.

</dd> <dt>

**PSUnorderedAccessViews**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare il pixel shader le visualizzazioni di accesso non ordinate.

</dd> <dt>

**CS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato di compute shader.

</dd> <dt>

**CSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di Sampler di compute shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del campionatore.

</dd> <dt>

**CSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di risorse di calcolo shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**CSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer costanti compute shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot del buffer costante.

</dd> <dt>

**CSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di interfacce di calcolo shader. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di interfaccia.

</dd> <dt>

**CSUnorderedAccessViews**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare le visualizzazioni di accesso non ordinato del compute shader.

</dd> <dt>

**IAVertexBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matrice di buffer dei vertici. La matrice è una maschera di bit a più byte in cui ogni bit rappresenta uno slot di risorse.

</dd> <dt>

**IAIndexBuffer**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato del buffer dell'indice.

</dd> <dt>

**IAInputLayout**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato del layout di input.

</dd> <dt>

**IAPrimitiveTopology**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato della topologia primitiva.

</dd> <dt>

**OMRenderTargets**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare gli Stati delle destinazioni di rendering.

</dd> <dt>

**OMDepthStencilState**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato dello stencil di profondità.

</dd> <dt>

**OMBlendState**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato di Blend.

</dd> <dt>

**RSViewports**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare gli Stati dei viewport.

</dd> <dt>

**RSScissorRects**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare gli Stati dei rettangoli a forbice.

</dd> <dt>

**RSRasterizerState**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato del rasterizzatore.

</dd> <dt>

**SOBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare gli Stati dei buffer di flusso.

</dd> <dt>

**Predicazione**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore booleano che indica se salvare lo stato predicazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una maschera di blocco di stato indica che il dispositivo è stato modificato da un passaggio o da una tecnica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Effects 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

