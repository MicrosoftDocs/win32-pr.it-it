---
description: Suddivide una mesh in mesh inferiori alle dimensioni specificate.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: Funzione D3DXSplitMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aee07e79286867ce11ce394e852fdfc01c6a1e41dc75b8c979838844b4f09d2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298253"
---
# <a name="d3dxsplitmesh-function"></a>Funzione D3DXSplitMesh

Suddivide una mesh in mesh inferiori alle dimensioni specificate.

## <a name="syntax"></a>Sintassi


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMeshIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a [**un'interfaccia ID3DXMesh,**](id3dxmesh.md) che rappresenta la mesh di origine.

</dd> <dt>

*pAdjacencyIn* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per viso che specificano i tre elementi adiacenti per ogni viso nella mesh da semplificare.

</dd> <dt>

*MaxSize* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**

Numero massimo di vertici nella mesh risultante.

</dd> <dt>

*Opzioni* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**

Flag di opzione per le nuove mesh.

</dd> <dt>

*pMeshesOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Numero di mesh restituite.

</dd> <dt>

*ppMeshArrayOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer contenente una matrice di [**interfacce ID3DXMesh**](id3dxmesh.md) per le nuove mesh. Per una mesh di origine suddivisa in n mesh, *ppMeshArrayOut* è una matrice di n **puntatori ID3DXMesh.**

</dd> <dt>

*ppAdjacencyArrayOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer contenente una matrice di matrici di adipenze (DWORD) per le nuove mesh. Vedere [**ID3DXBuffer**](id3dxbuffer.md). Questo parametro è facoltativo.

</dd> <dt>

*ppFaceRemapArrayOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer contenente una matrice di matrici di rimap dei viso (DWORD) per le nuove mesh. Vedere [**ID3DXBuffer**](id3dxbuffer.md). Questo parametro è facoltativo.

</dd> <dt>

*ppVertRemapArrayOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer contenente una matrice di matrici di remap dei vertici per le nuove mesh. Vedere [**ID3DXBuffer**](id3dxbuffer.md). Questo parametro è facoltativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Un uso comune di questa funzione è suddividere una mesh con indici a 32 bit (più di 65535 vertici) in più di una mesh, ognuno dei quali ha indici a 16 bit.

Le matrici adipenze, di ridefinizione dei vertici e di ridefinizione dei visi sono matrici DWORD in cui ogni matrice contiene n puntatori DWORD, seguiti dai dati DWORD a cui fanno riferimento i puntatori. Ad esempio, per ottenere le informazioni di ridefinizione del viso per il viso 3 nella mesh 2, è possibile usare il codice seguente, presupponendo che i dati di ridefinizione del viso siano stati restituiti in una variabile denominata *ppFaceRemapArrayOut*.


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
