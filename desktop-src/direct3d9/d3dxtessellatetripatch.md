---
description: Tessellates una patch di superficie di ordine superiore triangolare in una mesh triangolare.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: Funzione D3DXTessellateTriPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateTriPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61d5a426f9fe3331b85c4a881219319622283820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762017"
---
# <a name="d3dxtessellatetripatch-function"></a>D3DXTessellateTriPatch (funzione)

Tessellates una patch di superficie di ordine superiore triangolare in una mesh triangolare.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXTessellateTriPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3TRIPATCH_INFO         *pTriPatchInfo,
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

Puntatore a una matrice di tre valori a virgola mobile che identificano il numero di segmenti in cui deve essere diviso ogni bordo della patch del triangolo quando tassellati. Vedere [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).

</dd> <dt>

*pInDecl* \[ in\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Struttura di dichiarazione vertici che definisce i dati dei vertici. Vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*pTriPatchInfo* \[ in\]
</dt> <dd>

Tipo: **const [**D3TRIPATCH \_ info**](d3dtripatch-info.md) \***

Descrive una patch di triangolo. Vedere [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).

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

Usare [**D3DXTriPatchSize**](d3dxtripatchsize.md) per ottenere il numero di vertici e indici di output necessari per la funzione mosaico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
