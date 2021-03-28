---
title: Struttura D3DX11_PASS_SHADER_DESC (D3dx11effect. h)
description: Descrive un passaggio di effetto.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- Struttura D3DX11_PASS_SHADER_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cac6e842dabeaabc60451737fae56eb2cb61915
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982547"
---
# <a name="d3dx11_pass_shader_desc-structure"></a>D3DX11 \_ passare la \_ \_ struttura desc shader

Descrive un passaggio di effetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**pShaderVariable**
</dt> <dd>

Tipo: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***

</dd> <dd>

Variabile da cui proviene questo shader.

</dd> <dt>

**ShaderIndex**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Elemento di pShaderVariable (se una matrice) o 0 se non applicabile.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 \_ pass \_ shader \_ desc viene usato con i metodi [**ID3DX11EffectPass**](id3dx11effectpass.md) Get \* ShaderDesc.

Se si tratta di un'assegnazione shader inline, l'interfaccia restituita sarà una variabile shader anonima, che non può essere recuperata in altro modo. Il nome nella variabile Description sarà "$Anonymous". Se non è presente alcuna assegnazione di questo tipo nel blocco Pass, pShaderVariable! = **null**, ma pShaderVariable->IsValid () = = **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Effects 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

