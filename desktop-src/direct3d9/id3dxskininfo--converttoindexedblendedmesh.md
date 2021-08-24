---
description: Accetta una mesh e restituisce una nuova mesh con pesi, indici e una tabella di combinazione di osso per vertice. La tabella descrive quali palette di osso influiscono sui subset della mesh.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: Metodo ID3DXSkinInfo::ConvertToIndexedBlendedMesh (D3DX9Mesh.h)
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
ms.openlocfilehash: 9aa2b4bef607197c0f6fea084054d0e4fed1c721388677d45b465aff9c39ce49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790451"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a>Metodo ID3DXSkinInfo::ConvertToIndexedBlendedMesh

Accetta una mesh e restituisce una nuova mesh con pesi, indici e una tabella di combinazione di osso per vertice. La tabella descrive quali palette di osso influiscono sui subset della mesh.

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

*pMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Mesh di input. Vedere [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*Opzioni* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Attualmente inutilizzato.

</dd> <dt>

*paletteSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di matrici di osso disponibili per l'interfaccia della tavolozza delle matrici.

</dd> <dt>

*pAdjacencyIn* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Immettere le informazioni sull'adizia della mesh.

</dd> <dt>

*pAdjacencyOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Output delle informazioni sull'adizia della mesh.

</dd> <dt>

*pFaceRemap* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matrice di DWORD, uno per ogni viso, che identifica il viso della mesh originale corrispondente a ogni viso nella mesh blended. Se il valore fornito per questo argomento è **NULL,** i dati di modifica del mapping dei visi non vengono restituiti.

</dd> <dt>

*ppVertexRemap* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer,**](id3dxbuffer.md) che contiene un valore DWORD per ogni vertice che specifica il mapping dei nuovi vertici ai vertici vecchi. Questo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici. Questo parametro è facoltativo. È possibile usare **NULL.**

</dd> <dt>

*pMaxVertexInfl* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a un valore DWORD che conterrà il numero massimo di influenze ossee necessarie per ogni vertice per questo metodo di skinning.

</dd> <dt>

*pNumBoneCombinations* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al numero di ossi nella tabella delle combinazioni di osso.

</dd> <dt>

*ppBoneCombinationTable* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore alla tabella della combinazione di osso. I dati sono organizzati in una [**struttura D3DXBONECOMBINATION.**](d3dxbonecombination.md)

</dd> <dt>

*ppMesh* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntatore alla nuova mesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Ogni elemento nelle matrici remap specifica l'indice precedente per tale posizione. Ad esempio, se un vertice si è posizionato nella posizione 3 ma è stato mappato nuovamente alla posizione 5, il quinto elemento di pVertexRemap conterrà 3.

Questo metodo non viene eseguito su hardware che non supporta la fusione dei vertici a funzione fissa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
