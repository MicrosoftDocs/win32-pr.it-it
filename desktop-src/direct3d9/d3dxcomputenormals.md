---
description: Calcola le normali unità per ogni vertice in una rete mesh. Fornito per supportare le applicazioni legacy. Usare D3DXComputeTangentFrameEx per ottenere risultati migliori.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: Funzione D3DXComputeNormals (D3DX9Mesh. h)
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
ms.openlocfilehash: 3f95e5e353c318429f5340d1a831f9ca3050ba3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969406"
---
# <a name="d3dxcomputenormals-function"></a>D3DXComputeNormals (funzione)

Calcola le normali unità per ogni vertice in una rete mesh. Fornito per supportare le applicazioni legacy. Usare [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) per ottenere risultati migliori.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Puntatore a un'interfaccia [**ID3DXBaseMesh**](id3dxbasemesh.md) , che rappresenta l'oggetto mesh normalizzato.

</dd> <dt>

*pAdjacency* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella rete progressiva creata. Questo parametro è facoltativo e deve essere impostato su **null** se non è usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Per la mesh di input deve essere specificato il flag [D3DFVF \_ Normal](d3dfvf.md) nel formato di vertice flessibile (FVF).

Un normale per un vertice viene generato calcolando la media dei normali di tutti i visi che condividono tale vertice.

Se viene specificato adiacenza, i vertici replicati vengono ignorati e "smussati". Se adiacenza non viene specificato, i vertici replicati avranno le normali medie in solo dai visi che vi fanno riferimento in modo esplicito.

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
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
