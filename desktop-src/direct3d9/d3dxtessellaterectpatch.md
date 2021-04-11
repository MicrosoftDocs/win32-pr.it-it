---
description: Tessellates una patch della superficie di ordine superiore rettangolare in una mesh triangolare.
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: Funzione D3DXTessellateRectPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateRectPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 887f0035b50efd860149410e50dd6abff301968d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234997"
---
# <a name="d3dxtessellaterectpatch-function"></a>D3DXTessellateRectPatch (funzione)

Tessellates una patch della superficie di ordine superiore rettangolare in una mesh triangolare.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXTessellateRectPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3DRECTPATCH_INFO       *pRectPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVB* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**

Buffer vertex che contiene i dati della patch.

</dd> <dt>

*pNumSegs* \[ in\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di quattro valori a virgola mobile che identificano il numero di segmenti in cui ogni bordo della patch rettangolo deve essere diviso quando tassellati. Vedere [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).

</dd> <dt>

*pInDecl* \[ in\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Struttura di dichiarazione vertici che definisce i dati dei vertici. Vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*pRectPatchInfo* \[ in\]
</dt> <dd>

Tipo: **const [**D3DRECTPATCH \_ info**](d3drectpatch-info.md) \***

Descrive una patch rettangolare. Vedere [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).

</dd> <dt>

*pMesh* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore alla mesh creata. Vedere [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Usare [**D3DXRectPatchSize**](d3dxrectpatchsize.md) per ottenere il numero di vertici e indici di output necessari per la funzione mosaico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
