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
ms.openlocfilehash: 0c22c8a3a14fd8af3e9104889b421068c7ff1457
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117859"
---
# <a name="d3dxshprtcompsupercluster-function"></a>Funzione D3DXSHPRTCompSuperCluster

Usato con i risultati compressi della versione dei vertici del simulatore di trasferimento di raggi pre-ricalcolo (PRT). Genera "supercluster", ovvero gruppi di cluster che possono essere disegnati nella stessa chiamata di disegno. Per raggruppare i cluster viene usato un algoritmo greedy che riduce al minimo il ridisegno.

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

Puntatore a una mesh che rappresenta la scena composita passata al simulatore. Vedere [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*MaxNumClusters* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero massimo di cluster allocati per cluster super.

</dd> <dt>

*NumCluster* \[ Pollici\]
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

 

 
