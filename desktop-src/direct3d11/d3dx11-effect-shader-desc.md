---
title: D3DX11_EFFECT_SHADER_DESC struttura (D3dx11effect.h)
description: Descrive uno shader effetto.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- D3DX11_EFFECT_SHADER_DESC struttura Direct3D 11
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
ms.openlocfilehash: b48695b2e6ff0cca2046606eaad7dbdf137641ce126bd4f5f211e399aaf29d39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096351"
---
# <a name="d3dx11_effect_shader_desc-structure"></a>Struttura \_ \_ DESC D3DX11 EFFECT SHADER \_

Descrive uno shader effetto.

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

Tipo: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Passato a CreateInputLayout. Valido solo per un vertex shader o geometry shader. Vedere [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).

</dd> <dt>

**IsInline**
</dt> <dd>

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

**TRUE** è che lo shader è definito inline. in caso **contrario, FALSE.**

</dd> <dt>

**pBytecode**
</dt> <dd>

Tipo: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Bytecode shader.

</dd> <dt>

**BytecodeLength**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Lunghezza di pBytecode.

</dd> <dt>

**SODecls**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Stringa di dichiarazione stream out (per geometry shader con SO).

</dd> <dt>

**RasterizedStream**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Indica quale flusso viene rasterizzato. Gli shader geometry D3D11 possono eseguire l'output di un massimo di quattro flussi di dati, uno dei quali può essere rasterizzato.

</dd> <dt>

**NumInputSignatureEntries**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di voci nella firma di input.

</dd> <dt>

**NumOutputSignatureEntries**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di voci nella firma di output.

</dd> <dt>

**NumPatchConstantSignatureEntries**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di voci nella firma costante della patch.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 EFFECT SHADER DESC viene usato con \_ \_ \_ [**ID3DX11EffectShaderVariable::GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Effetti 11 Strutture](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

