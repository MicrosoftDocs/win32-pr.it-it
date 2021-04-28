---
description: 'Funzione D3DXSHPRTCompSplitMeshSC: usata con i risultati compressi della versione vertice del simulatore PRT (Precomputed Radiance Transfer).'
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: Funzione D3DXSHPRTCompSplitMeshSC (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e51a86ec9b12992d49364d3a7c614751dacafac3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093899"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a>Funzione D3DXSHPRTCompSplitMeshSC

Usato con i risultati compressi della versione dei vertici del simulatore di trasferimento di raggi pre-ricalcolo (PRT). Dopo [**aver chiamato D3DXSHPRTCompSuperCluster,**](d3dxshprtcompsupercluster.md) questa funzione può essere usata per dividere la mesh in un gruppo di visi/vertici per ogni super cluster. Ogni super cluster contiene tutti i visi che contengono tutti i vertici classificati in uno dei relativi cluster. Tutti i vertici connessi a questo set di visi sono inclusi anche nella matrice restituita ppVertStatus che indica se il vertice appartiene o meno al cluster super.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pClusterIDs* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

*ID cluster NumVertices* (estratti da un buffer compresso).

</dd> <dt>

*NumVertices* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di vertici nella mesh originale.

</dd> <dt>

*NumCs* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di cluster (parametro di input per la compressione).

</dd> <dt>

*pSClusterIDs* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Matrice di *numC di dimensioni* che conterranno ID cluster super.

</dd> <dt>

*NumSCS* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di cluster super allocati in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).

</dd> <dt>

*pInputIB* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Dati index buffer non elaborati per la mesh. Il formato dipende da *InputIBIs32Bit.*

</dd> <dt>

*InputIBIs32Bit* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Se **TRUE,** la index buffer è impostata su 32 bit. in caso contrario, 16 bit.

</dd> <dt>

*NumFaces* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di visi nella mesh originale *(pInputIB* è 3 volte la lunghezza).

</dd> <dt>

*ppIBData* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Oggetto index buffer che conterrà i visi divisi risultanti. Formato determinato da *InputIBIs32Bit*. Allocato dalla funzione.

</dd> <dt>

*pIBDataLength* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Lunghezza di *ppIBData*, assegnata nella funzione.

</dd> <dt>

*OutputIBIs32Bit* \[ in, out\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Se **TRUE,** alloca una matrice di interi senza segno; In caso contrario, alloca una matrice short senza segno.

</dd> <dt>

*ppFaceRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Mapping di ogni viso in *ppIBData* ai visi originali. La lunghezza \* *è pIBDataLength*/3.

</dd> <dt>

*ppVertData* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Nuova struttura dei dati dei vertici. Dimensione di *pVertDataLength.*

</dd> <dt>

*pVertDataLength* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Numero di nuovi vertici nella mesh suddivisa. Assegnato nella funzione .

</dd> <dt>

*pSCClusterList* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Matrice di *numCs* di lunghezza in cui *pSCData* indicizza (campi *pClusterIDs)* per ogni supercluster, contiene cluster ordinati per \* supercluster.

</dd> <dt>

*pSCData* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***

Struttura per cluster super. Contiene indici in *ppIBData*, *pSCClusterList* e *ppVertData*.

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

[Funzioni di trasferimento della radiance pre-ricalcolate](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
