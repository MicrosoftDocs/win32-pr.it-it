---
description: Eseguire il skining del software su una matrice di vertici.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: Metodo ID3DX10SkinInfo::D oSoftwareSkinning (D3DX10. h)
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
ms.openlocfilehash: 54dfe909e36be0273e0679a824ff0674b0e3b38c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322744"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a>ID3DX10SkinInfo::D Metodo oSoftwareSkinning

Eseguire il skining del software su una matrice di vertici.

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

*StartVertex* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Un indice in base 0 in pSrcVertices.

</dd> <dt>

*VertexCount* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di vertici da trasformare.

</dd> <dt>

*pSrcVertices* \[ in\]
</dt> <dd>

Tipo: **void \***

Puntatore a una matrice di vertici da trasformare.

</dd> <dt>

*SrcStride* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Dimensione, in byte, di un vertice in pSrcVertices.

</dd> <dt>

*pDestVertices* \[ in uscita\]
</dt> <dd>

Tipo: **void \***

Puntatore a una matrice di vertici, che verrà riempito con i vertici trasformati.

</dd> <dt>

*DestStride* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Dimensione, in byte, di un vertice in pDestVertices.

</dd> <dt>

*pBoneMatrices* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Matrice di matrici che verrà usata per trasformare i punti di cui è stato eseguito il mapping a ogni osso, in modo che i vertici mappati a Bone \[ i \] verranno trasformati da pBoneMatrices \[ i \] . Questa matrice verrà utilizzata per trasformare le matrici solo se il valore di pChannelDescs è impostato su **false**. in caso contrario, verrà utilizzato pInverseTransposeBoneMatrices.

</dd> <dt>

*pInverseTransposeBoneMatrices* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Se questo valore è **null**, verrà impostato su un valore uguale a pBoneMatrices. Questa matrice di matrici verrà utilizzata per trasformare i vertici solo se il valore di pChannelDescs è impostato su **true**; in caso contrario, verrà utilizzato pBoneMatrices.

</dd> <dt>

*pChannelDescs* \[ in\]
</dt> <dd>

Tipo: **[ **d3dx10 \_ Skin \_ Channel**](d3dx10-skinning-channel.md)\***

Puntatore a una \_ struttura del canale di skinning di d3dx10 \_ , che determina il membro del vertice decl in cui verrà eseguita la skining del software.

</dd> <dt>

*NumChannels* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Il numero di strutture del canale di D3DX10 \_ Skinning \_ in pChannelDescs.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere: E \_ INVALIDARG.

## <a name="remarks"></a>Commenti

Di seguito è riportato un esempio di come usare la skining del software:


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
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
