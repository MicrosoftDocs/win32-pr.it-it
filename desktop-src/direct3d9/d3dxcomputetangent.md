---
description: Calcola i vettori tangenti per le coordinate di trama specificate nella fase della trama. Fornito per supportare le applicazioni legacy. Usare D3DXComputeTangentFrameEx per ottenere risultati migliori.
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: Funzione D3DXComputeTangent (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cdb6a9dae3bdbad0f239fa61ba066d7b1bffb14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322613"
---
# <a name="d3dxcomputetangent-function"></a>D3DXComputeTangent (funzione)

Calcola i vettori tangenti per le coordinate di trama specificate nella fase della trama. Fornito per supportare le applicazioni legacy. Usare [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) per ottenere risultati migliori.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Mesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) che rappresenta la mesh di input.

</dd> <dt>

*TexStageIndex* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice che rappresenta la fase della trama.

</dd> <dt>

*TangentIndex* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice che fornisce l'indice di utilizzo per i dati della tangente. La dichiarazione di vertice implica l'utilizzo. Questo indice modifica l'utilizzo con l'indice Usage. Per ulteriori informazioni sulla dichiarazione di un vertice, vedere [dichiarazione di vertici (Direct3D 9)](vertex-declaration.md).

</dd> <dt>

*BinormIndex* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice che fornisce l'indice di utilizzo per i dati binormali. La dichiarazione di vertice implica l'utilizzo. Questo indice modifica l'utilizzo con l'indice Usage. Per ulteriori informazioni sulla dichiarazione di un vertice, vedere [dichiarazione di vertici (Direct3D 9)](vertex-declaration.md).

</dd> <dt>

A *capo automatico* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Impostare questo valore su 0 per nessun ritorno a capo o su 1 per il wrapping nelle direzioni u e V.

</dd> <dt>

*pAdjacency* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per ogni volto da riempire con indici facciali adiacenti. Il numero di byte in questa matrice deve essere almeno ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Se la dichiarazione del vertice mesh specifica i campi tangente o binormale, **D3DXComputeTangent** aggiornerà tutti i dati tangente o binormali specificati dall'utente. In alternativa, impostare TangentIndex su [D3DX \_ default](other-d3dx-constants.md) in modo da non aggiornare i dati della tangente specificati dall'utente oppure impostare BinormIndex su D3DX \_ default per non aggiornare i dati binormali forniti dall'utente. Impossibile impostare TexStageIndex su D3DX \_ default.

**D3DXComputeTangent** dipende dalla dichiarazione del vertice mesh contenente il campo Binormal (BinormIndex), il campo tangente (TangentIndex) o entrambi. In caso contrario, la funzione avrà esito negativo.

Questa funzione chiama semplicemente [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con i parametri di input seguenti:


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
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
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
