---
description: Acquisisce una mesh e restituisce una nuova mesh con pesi di Blend per vertice, indici e una tabella combinata Bone. La tabella descrive le tavolozze ossee che influiscono sui subset della mesh.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: 'Metodo ID3DXSkinInfo:: ConvertToIndexedBlendedMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87c8a4b943a647e52d7260f1ff53b32b40756761
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323372"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a>Metodo ID3DXSkinInfo:: ConvertToIndexedBlendedMesh

Acquisisce una mesh e restituisce una nuova mesh con pesi di Blend per vertice, indici e una tabella combinata Bone. La tabella descrive le tavolozze ossee che influiscono sui subset della mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Mesh di input. Vedere [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*Opzioni* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Attualmente non usato.

</dd> <dt>

*paletteSize* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di matrici di osso disponibili per la personalizzazione della tavolozza della tabella.

</dd> <dt>

*pAdjacencyIn* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Informazioni adiacenza mesh di input.

</dd> <dt>

*pAdjacencyOut* \[ in\]
</dt> <dd>

Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Informazioni adiacenza mesh di output.

</dd> <dt>

*pFaceRemap* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matrice di DWORD, una per ogni volto, che identifica la faccia mesh originale che corrisponde a ogni face nella mesh di Blend. Se il valore fornito per questo argomento è **null**, non vengono restituiti i dati di riassociazione della faccia.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) , che contiene un valore DWORD per ogni vertice che specifica la modalità di mapping dei nuovi vertici ai vertici precedenti. Questo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici. Questo parametro è facoltativo; È possibile utilizzare **null** .

</dd> <dt>

*pMaxVertexInfl* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a un valore DWORD che conterrà il numero massimo di influenze dell'osso necessarie per ogni vertice per questo metodo di skinning.

</dd> <dt>

*pNumBoneCombinations* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al numero di ossa nella tabella delle combinazioni di osso.

</dd> <dt>

*ppBoneCombinationTable* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore alla tabella delle combinazioni di osso. I dati sono organizzati in una struttura [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntatore alla nuova mesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Ogni elemento nelle matrici di riassociazione consente di specificare l'indice precedente per tale posizione. Se, ad esempio, un vertice era nella posizione 3 ma è stato rimappato alla posizione 5, il quinto elemento di pVertexRemap conterrà 3.

Questo metodo non viene eseguito su hardware che non supporta la fusione di vertici a funzione fissa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
