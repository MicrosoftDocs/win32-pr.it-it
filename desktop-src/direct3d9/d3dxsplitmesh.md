---
description: Suddivide una mesh in mesh di dimensioni inferiori a quelle specificate.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: Funzione D3DXSplitMesh (D3DX9Mesh. h)
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
ms.openlocfilehash: d1f01cdb4ddd009f5cdf0b7f0310a492840955f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322584"
---
# <a name="d3dxsplitmesh-function"></a>D3DXSplitMesh (funzione)

Suddivide una mesh in mesh di dimensioni inferiori a quelle specificate.

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

*pMeshIn* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh di origine.

</dd> <dt>

*pAdjacencyIn* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per volto che specificano i tre elementi adiacenti per ogni viso nella mesh da semplificare.

</dd> <dt>

*MaxSize* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**

Numero massimo di vertici nel mesh risultante.

</dd> <dt>

*Opzioni* \[ di in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**

Flag di opzione per le nuove mesh.

</dd> <dt>

*pMeshesOut* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Numero di mesh restituite.

</dd> <dt>

*ppMeshArrayOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer contenente una matrice di interfacce [**ID3DXMesh**](id3dxmesh.md) per le nuove mesh. Per una mesh di origine divisa in n mesh, *ppMeshArrayOut* è una matrice di n puntatori **ID3DXMesh** .

</dd> <dt>

*ppAdjacencyArrayOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer contenente una matrice di matrici adiacenza (DWORD) per le nuove mesh. Vedere [**ID3DXBuffer**](id3dxbuffer.md). Questo parametro è facoltativo.

</dd> <dt>

*ppFaceRemapArrayOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer contenente una matrice di matrici di mapping delle facce (DWORD) per le nuove mesh. Vedere [**ID3DXBuffer**](id3dxbuffer.md). Questo parametro è facoltativo.

</dd> <dt>

*ppVertRemapArrayOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer contenente una matrice di matrici di riassociazione dei vertici per le nuove mesh. Vedere [**ID3DXBuffer**](id3dxbuffer.md). Questo parametro è facoltativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Un uso comune di questa funzione consiste nel dividere una mesh con indici a 32 bit (più di 65535 vertici) in più di una mesh, ognuno dei quali ha indici a 16 bit.

Le matrici adiacenza, mapping dei vertici e mapping delle facce sono matrici sono DWORD in cui ogni matrice contiene n puntatori DWORD, seguiti dai dati DWORD a cui fanno riferimento i puntatori. Per ottenere, ad esempio, le informazioni di modifica del mapping delle facce per la faccia 3 nella mesh 2, è possibile usare il codice seguente, presupponendo che i dati di riassociazione volti siano stati restituiti in una variabile denominata *ppFaceRemapArrayOut*.


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
