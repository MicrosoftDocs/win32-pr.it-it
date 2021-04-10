---
description: Salda insieme i vertici replicati con attributi uguali. Questo metodo usa i valori Epsilon specificati per i confronti di uguaglianza.
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: Funzione D3DXWeldVertices (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 76e0a6f259bc8ba547a02b2e95cccf718d54e904
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762083"
---
# <a name="d3dxweldvertices-function"></a>D3DXWeldVertices (funzione)

Salda insieme i vertici replicati con attributi uguali. Questo metodo usa i valori Epsilon specificati per i confronti di uguaglianza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a un oggetto [**ID3DXMesh**](id3dxmesh.md) , mesh da cui si saldano i vertici.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più flag di [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).

</dd> <dt>

*pEpsilons* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***

Puntatore a una struttura [**D3DXWeldEpsilons**](d3dxweldepsilons.md) , che specifica i valori Epsilon da usare per questo metodo. Utilizzare **null** per inizializzare tutti i membri della struttura sul valore predefinito 1.0 e-6F.

</dd> <dt>

*pAdjacencyIn* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh di origine. Se il bordo non ha visi adiacenti, il valore è 0xFFFFFFFF. Se questo parametro è impostato su **null**, viene chiamato [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) per creare informazioni adiacenza logiche.

</dd> <dt>

*pAdjacencyOut* \[ in uscita\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh ottimizzata. Se il bordo non ha visi adiacenti, il valore è 0xFFFFFFFF.

</dd> <dt>

*pFaceRemap* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matrice di DWORD, una per ogni volto, che identifica la faccia mesh originale che corrisponde a ogni face nella rete elettrosaldata.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) , che contiene un valore DWORD per ogni vertice che specifica la modalità di mapping dei nuovi vertici ai vertici precedenti. Questo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questa funzione utilizza le informazioni adiacenza fornite per determinare i punti replicati. I vertici vengono uniti in base a un confronto Epsilon. I vertici con posizione uguale devono essere già stati calcolati e rappresentati da dati rappresentativi del punto.

Questa funzione combina i vertici a saldatura logica con componenti simili, ad esempio normali o coordinate di trama all'interno di pEpsilons.

Il codice di esempio seguente chiama questa funzione con la saldatura abilitata. I vertici vengono confrontati usando i valori Epsilon per la posizione del vettore e del vertice normali. Un puntatore viene restituito a una matrice di rimapping visi (*pFaceRemap*).


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
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

 

 
