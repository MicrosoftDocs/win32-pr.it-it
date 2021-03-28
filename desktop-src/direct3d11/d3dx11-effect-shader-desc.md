---
title: Struttura D3DX11_EFFECT_SHADER_DESC (D3dx11effect. h)
description: Descrive un effetto shader.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- Struttura D3DX11_EFFECT_SHADER_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c518d4f7930d0651e519d23218121b8ed4bed288
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886319"
---
# <a name="d3dx11_effect_shader_desc-structure"></a>\_ \_ Struttura desc shader Effect \_ D3DX11

Descrive un effetto shader.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DX11_EFFECT_SHADER_DESC {
  const BYTE *pInputSignature;
  BOOL       IsInline;
  const BYTE *pBytecode;
  UINT       BytecodeLength;
  LPCSTR     SODecls[D3D11_SO_STREAM_COUNT];
  UINT       RasterizedStream;
  UINT       NumInputSignatureEntries;
  UINT       NumOutputSignatureEntries;
  UINT       NumPatchConstantSignatureEntries;
} D3DX11_EFFECT_SHADER_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**pInputSignature**
</dt> <dd>

Tipo: **const [**byte**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Passato a CreateInputLayout. Valido solo in un vertex shader o in un geometry shader. Vedere [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).

</dd> <dt>

**IsInline**
</dt> <dd>

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

**True** se lo shader è definito inline; in caso contrario, **false**.

</dd> <dt>

**pBytecode**
</dt> <dd>

Tipo: **const [**byte**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Bytecode dello shader.

</dd> <dt>

**BytecodeLength**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Lunghezza di pBytecode.

</dd> <dt>

**SODecls**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Stringa di dichiarazione del flusso in uscita (per la geometria shader con).

</dd> <dt>

**RasterizedStream**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Indica il flusso rasterizzato. D3D11 Geometry shaders può restituire fino a quattro flussi di dati, uno dei quali può essere rasterizzato.

</dd> <dt>

**NumInputSignatureEntries**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di voci nella firma di input.

</dd> <dt>

**NumOutputSignatureEntries**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di voci nella firma di output.

</dd> <dt>

**NumPatchConstantSignatureEntries**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di voci nella firma costante della patch.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 \_ Effect \_ shader \_ desc viene usato con [**ID3DX11EffectShaderVariable:: GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Effects 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

