---
description: Usato con i risultati compressi della versione Vertex del simulatore di trasferimento di luminosità pre-calcolata (PRT).
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: Funzione D3DXSHPRTCompSuperCluster (D3DX9Mesh. h)
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
ms.openlocfilehash: 1daf25dddfaf738ecc2fed9605429a19170177ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354709"
---
# <a name="d3dxshprtcompsupercluster-function"></a>D3DXSHPRTCompSuperCluster (funzione)

Usato con i risultati compressi della versione Vertex del simulatore di trasferimento di luminosità pre-calcolata (PRT). Genera "Supercluster", ovvero gruppi di cluster che possono essere disegnati nella stessa chiamata di disegno. Per raggruppare i cluster viene usato un algoritmo greedy che riduce al minimo il sovralievo.

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

*pClusterIDs* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore a un ID cluster NumVerts (Estratto da un buffer compresso).

</dd> <dt>

*pScene* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a una mesh che rappresenta una scena composita passata al simulatore. Vedere [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*MaxNumClusters* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero massimo di cluster allocati per cluster Super.

</dd> <dt>

*NumClusters* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di cluster calcolati nel simulatore.

</dd> <dt>

*pSClusterIDs* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di lunghezza *NumClusters*. Contiene l'indice del cluster Super a cui è stato assegnato il cluster corrispondente.

</dd> <dt>

*pNumSCs* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Numero di cluster superati allocati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trasferimento Radiance pre-calcolate](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
