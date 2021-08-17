---
description: Tessella una superficie triangolare di ordine superiore in una mesh triangolare.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: Funzione D3DXTessellateTriPatch (D3DX9Mesh.h)
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
ms.openlocfilehash: 1cae3ff9709cb74e15c176abc0e738e4f12d1417eec1d040b90269b7e3cbc6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122713"
---
# <a name="d3dxtessellatetripatch-function"></a>Funzione D3DXTessellateTriPatch

Tessella una superficie triangolare di ordine superiore in una mesh triangolare.

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

*pVB* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**

Vertex buffer contenente i dati della patch.

</dd> <dt>

*pNumSegs* \[ Pollici\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre valori a virgola mobile che identificano il numero di segmenti in cui ogni bordo del triangolo deve essere diviso quando è a tessella. Vedere [**D3DTRIPATCH \_ INFO**](d3dtripatch-info.md).

</dd> <dt>

*pInDecl* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Struttura di dichiarazione dei vertici che definisce i dati dei vertici. Vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*pTriPatchInfo* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3TRIPATCH \_ INFO**](d3dtripatch-info.md) \***

Descrive una patch triangolare. Vedere [**D3DTRIPATCH \_ INFO**](d3dtripatch-info.md).

</dd> <dt>

*pMesh* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore alla mesh creata. Vedere [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Usare [**D3DXTriPatchSize**](d3dxtripatchsize.md) per ottenere il numero di vertici e indici di output di cui la funzione a tessellazione necessita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
