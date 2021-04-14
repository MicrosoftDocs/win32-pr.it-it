---
description: Usato con i risultati compressi della versione Vertex del simulatore di trasferimento di luminosità pre-calcolata (PRT).
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: Funzione D3DXSHPRTCompSplitMeshSC (D3DX9Mesh. h)
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
ms.openlocfilehash: 18742d12b6e1ae106dcf832baccccb2416465880
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401948"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a>D3DXSHPRTCompSplitMeshSC (funzione)

Usato con i risultati compressi della versione Vertex del simulatore di trasferimento di luminosità pre-calcolata (PRT). Dopo la chiamata a [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) , questa funzione può essere usata per suddividere la mesh in un gruppo di visi/vertici per cluster Super. Ogni cluster Super contiene tutti i visi che contengono tutti i vertici classificati in uno dei relativi cluster. Tutti i vertici connessi a questo set di visi sono inclusi anche con la matrice restituita ppVertStatus che indica se il vertice appartiene o meno al cluster Super.

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

*pClusterIDs* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

ID cluster *numVertices* (estratti da un buffer compresso).

</dd> <dt>

*NumVertices* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di vertici nel mesh originale.

</dd> <dt>

*NumCs* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di cluster (parametro di input per la compressione).

</dd> <dt>

*pSClusterIDs* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Matrice di dimensioni *NumCs* che conterrà gli ID del cluster superati.

</dd> <dt>

*NumSCs* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di cluster superati allocati in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).

</dd> <dt>

*pInputIB* \[ in\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Buffer indice non elaborato per mesh. Il formato dipende da *InputIBIs32Bit*.

</dd> <dt>

*InputIBIs32Bit* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **true**, il buffer dell'indice è impostato su 32 bit; in caso contrario, 16 bit.

</dd> <dt>

*NumFaces* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di visi nella mesh originale (*pInputIB* è 3 volte questa lunghezza).

</dd> <dt>

*ppIBData* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer dell'indice non elaborato che conterrà i visi divisi risultanti. Formato determinato da *InputIBIs32Bit*. Allocato per funzione.

</dd> <dt>

*pIBDataLength* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Lunghezza di *ppIBData*, assegnata nella funzione.

</dd> <dt>

*OutputIBIs32Bit* \[ in uscita\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **true**, alloca una matrice di Unsigned Integer; in caso contrario, alloca una matrice short senza segno.

</dd> <dt>

*ppFaceRemap* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Mapping di ogni viso in *ppIBData* ai visi originali. La lunghezza è \* *pIBDataLength*/3.

</dd> <dt>

*ppVertData* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Nuova struttura di dati dei vertici. Dimensioni di *pVertDataLength*.

</dd> <dt>

*pVertDataLength* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Numero di nuovi vertici in una mesh divisa. Funzione assegnata.

</dd> <dt>

*pSCClusterList* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Matrice di lunghezza *NumCs* che *pSCData* gli indici (campi *pClusterIDs* \* ) per ogni Supercluster, contiene i cluster ordinati in base al Supercluster.

</dd> <dt>

*pSCData* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***

Struttura per cluster Super. Contiene indici in *ppIBData*, *pSCClusterList* e *ppVertData*.

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

 

 
