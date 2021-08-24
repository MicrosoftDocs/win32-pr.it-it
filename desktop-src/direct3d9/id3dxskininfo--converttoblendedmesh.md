---
description: Accetta una mesh e restituisce una nuova mesh con pesi di fusione per vertice e una tabella di combinazioni di combinazioni di vertici. La tabella descrive gli elementi che influiscono sui subset della mesh.
ms.assetid: c26a9e84-5731-4394-a047-5f1ffe7688d9
title: Metodo ID3DXSkinInfo::ConvertToBlendedMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 026808748f0d94a4b5282bfdad6590e3c030ddf6ce0009bec5e59852e9984163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747681"
---
# <a name="id3dxskininfoconverttoblendedmesh-method"></a>Metodo ID3DXSkinInfo::ConvertToBlendedMesh

Accetta una mesh e restituisce una nuova mesh con pesi di fusione per vertice e una tabella di combinazioni di combinazioni di vertici. La tabella descrive gli elementi che influiscono sui subset della mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConvertToBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
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

Mesh di input. Vedere [**ID3DXMesh.**](id3dxmesh.md)

</dd> <dt>

*Opzioni* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Attualmente inutilizzato.

</dd> <dt>

*pAdjacencyIn* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Informazioni sull'adicenza della mesh di input.

</dd> <dt>

*pAdjacencyOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Informazioni sull'adienza della mesh di output.

</dd> <dt>

*pFaceRemap* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matrice di DWORD, uno per viso, che identifica la faccia mesh originale che corrisponde a ogni viso nella mesh mista. Se il valore fornito per questo argomento è **NULL,** i dati di modifica del mapping dei visi non vengono restituiti.

</dd> <dt>

*ppVertexRemap* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer,**](id3dxbuffer.md) che contiene un valore DWORD per ogni vertice che specifica il mapping dei nuovi vertici ai vertici vecchi. Questo nuovo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici. Questo parametro è facoltativo. È possibile usare **NULL.**

</dd> <dt>

*pMaxVertexInfl* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a un valore DWORD che conterrà il numero massimo di fattori di influenza di colore richiesti per ogni vertice per questo metodo di interfaccia.

</dd> <dt>

*pNumBoneCombinations* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al numero di animali nella tabella delle combinazioni di combinazioni.

</dd> <dt>

*ppBoneCombinationTable* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore alla tabella delle combinazioni di combinazioni. I dati sono organizzati in [**una struttura D3DXBONECOMBINATION.**](d3dxbonecombination.md)

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

Ogni elemento nella matrice remap specifica l'indice precedente per tale posizione. Ad esempio, se un vertice si è posizionato nella posizione 3 ma è stato mappato nuovamente alla posizione 5, il quinto elemento di pVertexRemap conterrà 3.

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

 

 
