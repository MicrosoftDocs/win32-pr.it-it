---
description: Eseguire la skinning del software su una matrice di vertici.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: Metodo ID3DX10SkinInfo::D oSoftwareSkinning (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.DoSoftwareSkinning
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20f68f51d6886d53d74cd31691e52c362c60d2bf9be2beb0656564cb20fcb80a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729811"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a>Metodo ID3DX10SkinInfo::D oSoftwareSkinning

Eseguire la skinning del software su una matrice di vertici.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DoSoftwareSkinning(
  [in]      UINT                    StartVertex,
  [in]      UINT                    VertexCount,
  [in]      void                    *pSrcVertices,
  [in]      UINT                    SrcStride,
  [in, out] void                    *pDestVertices,
  [in]      UINT                    DestStride,
  [in]      D3DXMATRIX              *pBoneMatrices,
  [in]      D3DXMATRIX              *pInverseTransposeBoneMatrices,
  [in]      D3DX10_SKINNING_CHANNEL *pChannelDescs,
  [in]      UINT                    NumChannels
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartVertex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice in base 0 in pSrcVertices.

</dd> <dt>

*VertexCount* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di vertici da trasformare.

</dd> <dt>

*pSrcVertices* \[ Pollici\]
</dt> <dd>

Tipo: **\* void**

Puntatore a una matrice di vertici da trasformare.

</dd> <dt>

*SrcStride* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Dimensione, in byte, di un vertice in pSrcVertices.

</dd> <dt>

*pDestVertices* \[ in, out\]
</dt> <dd>

Tipo: **\* void**

Puntatore a una matrice di vertici, che verrà riempita con i vertici trasformati.

</dd> <dt>

*DestStride* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Dimensione, in byte, di un vertice in pDestVertices.

</dd> <dt>

*pBoneMatrices* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Matrice di matrici che verrà utilizzata per trasformare i punti mappati a ogni osso, in modo che i vertici mappati all'osso i verranno trasformati da \[ \] pBoneMatrices \[ i \] . Questa matrice verrà usata per trasformare le matrici solo se il valore IsNormal in pChannelDescs è impostato su **FALSE,** in caso contrario verrà usato pInverseTransposeBoneMatrices.

</dd> <dt>

*pInverseTransposeBoneMatrices* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Se questo valore è **NULL,** verrà impostato su pBoneMatrices. Questa matrice di matrici verrà usata per trasformare i vertici solo se il valore IsNormal in pChannelDescs è impostato su **TRUE,** in caso contrario verrà usato pBoneMatrices.

</dd> <dt>

*pChannelDescs* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ SKINNING \_ CHANNEL**](d3dx10-skinning-channel.md)\***

Puntatore a una struttura D3DX10 SKINNING CHANNEL, che determina il membro del vertice che declerà l'interfaccia software su cui \_ \_ verrà eseguita l'interfaccia.

</dd> <dt>

*NumChannels* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di strutture D3DX10 \_ SKINNING \_ CHANNEL in pChannelDescs.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere E \_ INVALIDARG.

## <a name="remarks"></a>Commenti

Di seguito è riportato un esempio di come usare la skinning del software:


```
//vertex definition
struct MyVertex
{
    D3DXVECTOR3 Position;
    D3DXVECTOR2 Weight;
    D3DXVECTOR2 TexCoord;
};

//create vertex data
const UINT numVertices = 16;
MyVertex vertices[numVertices] = {...};
MyVertex destVertices[numVertices];

//create bone matrices
D3DXMATRIX boneMatrices[2];
D3DXMatrixIdentity(&boneMatrices[0]);
D3DXMatrixRotationX(&boneMatrices[1], 3.14159f / 180.0f);

//create bone indices and weights
UINT boneIndices[numVertices] = {...};
float boneWeights[2][numVertices] = {...};

//create skin info, populate it with bones and vertices, and then map them to each other
ID3DX10SkinInfo *pSkinInfo = NULL;
D3DX10CreateSkinInfo(&pSkinInfo);
pSkinInfo->AddBones(2);
pSkinInfo->AddVertices(numVertices);
pSkinInfo->AddBoneInfluences(0, numVertices, boneIndices, boneWeights[0]);
pSkinInfo->AddBoneInfluences(1, numVertices, boneIndices, boneWeights[1]);

//create channel desc
D3DX10_SKINNING_CHANNEL channelDesc;
channelDesc.SrcOffset = 0;
channelDesc.DestOffset = 0;
channelDesc.IsNormal = FALSE;

//do the skinning
pSkinInfo->DoSoftwareSkinning(0, numVertices,
                              vertices, sizeof(MyVertex), 
                              destVertices, sizeof(MyVertex), 
                              boneMatrices, NULL, 
                              &channelDesc, 1);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
