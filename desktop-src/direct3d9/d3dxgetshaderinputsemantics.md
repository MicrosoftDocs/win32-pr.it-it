---
description: Ottiene la semantica per gli input dello shader. Utilizzare questo metodo per determinare il formato del vertice di input.
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: Funzione D3DXGetShaderInputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2032f241d6ca5c22506c0875a21f9d5b431920df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322659"
---
# <a name="d3dxgetshaderinputsemantics-function"></a>D3DXGetShaderInputSemantics (funzione)

Ottiene la semantica per gli input dello shader. Utilizzare questo metodo per determinare il formato del vertice di input.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXGetShaderInputSemantics(
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

Puntatore a una matrice di strutture [**D3DXSEMANTIC**](d3dxsemantic.md) . La funzione riempirà questa matrice con la semantica per ogni elemento di input a cui fa riferimento lo shader. Si presuppone che questa matrice contenga almeno gli elementi MAXD3DDECLLENGTH. Tuttavia, la chiamata a **D3DXGetShaderInputSemantics** con PSemantics = **null** restituirà il numero di elementi necessari per pcount.

</dd> <dt>

*pcount* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Restituisce il numero di elementi in pSemantics.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Usare **D3DXGetShaderInputSemantics** per restituire un elenco di semantica di input richiesto dallo shader. Questo è il modo per individuare il formato del vertice di input per un shader HLSL (High-Level Shader Language). Se lo shader contiene input aggiuntivi che la dichiarazione del vertice non è presente, è possibile creare un flusso di vertici aggiuntivo con uno stride pari a 0 con i componenti mancanti con i valori predefiniti. È ad esempio possibile usare questa tecnica per fornire il colore del vertice predefinito per i modelli che non lo specificano.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
