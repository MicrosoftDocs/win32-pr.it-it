---
description: Ottiene la semantica per tutti gli elementi di output dello shader.
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: Funzione D3DXGetShaderOutputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderOutputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 264db967d2959c2f6e5096e0362e9db576ba9f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530901"
---
# <a name="d3dxgetshaderoutputsemantics-function"></a>D3DXGetShaderOutputSemantics (funzione)

Ottiene la semantica per tutti gli elementi di output dello shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFunction* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore al flusso DWORD della funzione shader.

</dd> <dt>

*pSemantics* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***

Puntatore a una matrice di strutture [**D3DXSEMANTIC**](d3dxsemantic.md) . La funzione riempirà questa matrice con la semantica per ogni elemento di output a cui fa riferimento lo shader. Si presuppone che questa matrice contenga almeno gli elementi MAXD3DDECLLENGTH. Tuttavia, la chiamata a **D3DXGetShaderOutputSemantics** con PSemantics = **null** restituirà il numero di elementi necessari per pcount.

</dd> <dt>

*pcount* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Restituisce il numero di elementi in pSemantics.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
