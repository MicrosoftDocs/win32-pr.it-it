---
description: 'Funzione D3DXSHPRTCompSuperCluster: usata con i risultati compressi della versione vertice del simulatore PRT (Precomputed Radiance Transfer).'
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: Funzione D3DXSHPRTCompSuperCluster (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55556046c7fa8e0a8e7666a9d2dd0a20d81b5f3cf59253f499cbd7d0fba41fbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749830"
---
# <a name="d3dxshprtcompsupercluster-function"></a>Funzione D3DXSHPRTCompSuperCluster

Usato con i risultati compressi della versione vertice del simulatore PRT (Pre-computed Radiance Transfer). Genera "supercluster", ovvero gruppi di cluster che possono essere disegnati nella stessa chiamata di disegno. Per raggruppare i cluster viene usato un algoritmo greedy che riduce al minimo la sovrapposizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pClusterIDs* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore a un ID cluster NumVerts (estratto da un buffer compresso).

</dd> <dt>

*pScene* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a una mesh che rappresenta la scena composita passata al simulatore. Vedere [**ID3DXMesh.**](id3dxmesh.md)

</dd> <dt>

*MaxNumClusters* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero massimo di cluster allocati per ogni super cluster.

</dd> <dt>

*NumClusters* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di cluster calcolati nel simulatore.

</dd> <dt>

*pSClusterIDs* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di *lunghezza NumClusters*. Contiene l'indice del super cluster a cui è stato assegnato il cluster corrispondente.

</dd> <dt>

*pNumSCs* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Numero di super cluster allocati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trasferimento di radiance pre-ricalcolate](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
