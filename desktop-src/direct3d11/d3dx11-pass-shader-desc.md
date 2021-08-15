---
title: D3DX11_PASS_SHADER_DESC struttura (D3dx11effect.h)
description: Descrive un passaggio dell'effetto.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- D3DX11_PASS_SHADER_DESC struttura Direct3D 11
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
ms.openlocfilehash: 8ec7328ce346b51c3315086dcc193f421081dd77fc3a169bc448fba10bc7fa3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536837"
---
# <a name="d3dx11_pass_shader_desc-structure"></a>Struttura \_ \_ DESC PASS SHADER \_ D3DX11

Descrive un passaggio dell'effetto.

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

Variabile da cui deriva lo shader.

</dd> <dt>

**ShaderIndex**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Elemento di pShaderVariable (se una matrice) o 0 se non applicabile.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 \_ PASS \_ SHADER \_ DESC viene usato con i metodi [**ID3DX11EffectPass**](id3dx11effectpass.md) Get \* ShaderDesc.

Se si tratta di un'assegnazione di shader inline, l'interfaccia restituita sarà una variabile shader anonima, che non è recuperabile in altro modo. Il nome nella descrizione della variabile sarà "$Anonymous". Se non è presente alcuna assegnazione di questo tipo nel blocco pass, pShaderVariable != **NULL,** ma pShaderVariable->IsValid() == **FALSE**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Effetti 11 Strutture](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

