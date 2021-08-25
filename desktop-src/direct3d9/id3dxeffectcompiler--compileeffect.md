---
description: Compilare un effetto.
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: Metodo ID3DXEffectCompiler::CompileEffect (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f3769f3f7433aadc55e766d68ecc152a4e26444cf506344f80e3f11a0bca8fcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951661"
---
# <a name="id3dxeffectcompilercompileeffect-method"></a>Metodo ID3DXEffectCompiler::CompileEffect

Compilare un effetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opzioni di compilazione identificate da vari flag. Il compilatore HLSL Direct3D 10 è ora l'impostazione predefinita. Per [informazioni dettagliate, vedere Flag D3DXSHADER.](d3dxshader-flags.md)

</dd> <dt>

*ppEffect* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer contenente l'effetto compilato. Per altre informazioni sull'accesso al buffer, vedere [**ID3DXBuffer.**](id3dxbuffer.md)

</dd> <dt>

*ppErrorMsgs* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer contenente almeno il primo messaggio di errore di compilazione che si è verificato. Sono inclusi gli errori del compilatore degli effetti e gli errori di compilazione del linguaggio di alto livello. Per altre informazioni sull'accesso al buffer, vedere [**ID3DXBuffer.**](id3dxbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK.

Se gli argomenti non sono validi, il metodo restituirà D3DERR \_ INVALIDCALL.

Se il metodo ha esito negativo, il valore restituito sarà E \_ FAIL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> </dl>

 

 
