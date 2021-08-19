---
description: Calcola le normali unità per ogni vertice in una mesh. Fornito per supportare le applicazioni legacy. Usare D3DXComputeTangentFrameEx per ottenere risultati migliori.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: Funzione D3DXComputeNormals (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d136e7c3d01b595273127c500ccc52cd310357df2147f3df5d97df9dbd38d38d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069311"
---
# <a name="d3dxcomputenormals-function"></a>Funzione D3DXComputeNormals

Calcola le normali unità per ogni vertice in una mesh. Fornito per supportare le applicazioni legacy. Usare [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) per ottenere risultati migliori.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Puntatore a [**un'interfaccia ID3DXBaseMesh**](id3dxbasemesh.md) che rappresenta l'oggetto mesh normalizzato.

</dd> <dt>

*pAdjacency* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per viso che specificano i tre elementi adiacenti per ogni viso nella mesh progressiva creata. Questo parametro è facoltativo e deve essere impostato su **NULL** se non è usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è S \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

La mesh di input deve avere il flag [D3DFVF \_ NORMAL](d3dfvf.md) specificato nel formato FVF (Flexible Vertex Format).

Una normale per un vertice viene generata mediando le normali di tutte le visi che condividono tale vertice.

Se viene fornita l'adizia, i vertici replicati vengono ignorati e "smussati". Se l'adizia non viene fornita, i vertici replicati avranno valori normali in media solo dai visi che vi fanno riferimento in modo esplicito.

Questa funzione chiama semplicemente [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con i parametri di input seguenti:


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
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

 

 
