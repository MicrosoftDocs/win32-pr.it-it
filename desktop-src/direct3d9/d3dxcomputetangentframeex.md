---
description: Esegue calcoli dei fotogrammi tangenti su una mesh. Vengono generati vettori tangenti, binormali e facoltativamente normali. Le singolarità vengono gestite in base alle esigenze raggruppando i bordi e suddividendo i vertici.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: Funzione D3DXComputeTangentFrameEx (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrameEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d091b7ca243e4833cd6aa36a409fca32069e52a267ec3f588b338777ed34338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988671"
---
# <a name="d3dxcomputetangentframeex-function"></a>Funzione D3DXComputeTangentFrameEx

Esegue calcoli dei fotogrammi tangenti su una mesh. Vengono generati vettori tangenti, binormali e facoltativamente normali. Le singolarità vengono gestite in base alle esigenze raggruppando i bordi e suddividendo i vertici.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeTangentFrameEx(
  _In_        ID3DXMesh   *pMesh,
  _In_        DWORD       dwTextureInSemantic,
  _In_        DWORD       dwTextureInIndex,
  _In_        DWORD       dwUPartialOutSemantic,
  _In_        DWORD       dwUPartialOutIndex,
  _In_        DWORD       dwVPartialOutSemantic,
  _In_        DWORD       dwVPartialOutIndex,
  _In_        DWORD       dwNormalOutSemantic,
  _In_        DWORD       dwNormalOutIndex,
  _In_        DWORD       dwOptions,
  _In_  const DWORD       *pdwAdjacency,
  _In_        FLOAT       fPartialEdgeThreshold,
  _In_        FLOAT       fSingularPointThreshold,
  _In_        FLOAT       fNormalEdgeThreshold,
  _Out_       ID3DXMesh   **ppMeshOut,
  _Out_       ID3DXBuffer **ppVertexMapping
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***

Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di input.

</dd> <dt>

*dwTextureInSemantic* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica la semantica di input delle coordinate di trama. Se D3DX DEFAULT, la funzione presuppone che non siano presenti coordinate di trama e la funzione avrà esito negativo a meno che non venga specificato il normale \_ calcolo del vettore.

</dd> <dt>

*dwTextureInIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Se una mesh ha più coordinate di trama, specifica la coordinata di trama da usare per i calcoli dei fotogrammi tangenti. Se zero, la mesh ha una sola coordinata di trama.

</dd> <dt>

*dwUPartialOutSemantic* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica la semantica di output per il tipo, in genere D3DDECLUSAGE TANGENT, che descrive dove verrà archiviata la derivata parziale rispetto alla \_ coordinata di trama U. Se D3DX \_ DEFAULT, questo derivato parziale non verrà archiviato.

</dd> <dt>

*dwUPartialOutIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica l'indice semantico in corrispondenza del quale archiviare la derivata parziale rispetto alla coordinata di trama U.

</dd> <dt>

*dwVPartialOutSemantic* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica il [**tipo D3DDECLUSAGE,**](./d3ddeclusage.md) in genere D3DDECLUSAGE BINORMAL, che descrive dove verrà archiviata la derivata parziale rispetto alla coordinata della \_ trama V. Se D3DX \_ DEFAULT, questo derivato parziale non verrà archiviato.

</dd> <dt>

*dwVPartialOutIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica l'indice semantico in corrispondenza del quale archiviare la derivata parziale rispetto alla coordinata di trama V.

</dd> <dt>

*dwNormalOutSemantic* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica la semantica normale di output, in genere D3DDECLUSAGE NORMAL, che descrive dove verrà archiviato il vettore normale in \_ ogni vertice. Se D3DX \_ DEFAULT, questo vettore normale non verrà archiviato.

</dd> <dt>

*dwNormalOutIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica l'indice semantico in corrispondenza del quale archiviare il vettore normale in corrispondenza di ogni vertice.

</dd> <dt>

*dwOptions* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [**flag D3DXTANGENT**](./d3dxtangent.md) che specificano le opzioni di calcolo dei fotogrammi tangenti. Se **NULL,** verranno specificate le opzioni seguenti:



| Descrizione                                                                                              | [**D3DXTANGENT**](./d3dxtangent.md) Valore flag                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Ponderare la lunghezza normale del vettore in base all'angolo, in radianti, sottriato dai due bordi che lasciano il vertice. | & ! ( D3DXTANGENT \_ PESO \_ PER \_ AREA \| D3DXTANGENT \_ WEIGHT EQUAL \_ )                |
| Calcolare le coordinate cartesiane ortogonali dalle coordinate della trama (u, v). Vedere la sezione Osservazioni.                   | & ! ( D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U \| D3DXTANGENT \_ ORTHOGONALIZE \_ FROM V \_ ) |
| Non viene eseguito il wrapping delle trame nelle direzioni u o v                                                     | & ! ( D3DXTANGENT \_ WRAP \_ UV )                                                      |
| I derivati parziali rispetto alle coordinate della trama vengono normalizzati.                                  | & ! ( D3DXTANGENT \_ NON \_ NORMALIZZARE \_ PARZIALI )                                     |
| I vertici vengono ordinati in senso antiorario intorno a ogni triangolo.                               | & ! ( D3DXTANGENT \_ WIND \_ CW )                                                      |
| Usare vettori normali per vertice già presenti nella mesh di input.                                         | & ! ( D3DXTANGENT \_ CALCULATE \_ NORMALS )                                            |



 

Se D3DXTANGENT GENERATE IN PLACE non è \_ \_ \_ impostato, la mesh di input viene clonata. La mesh originale deve quindi avere spazio sufficiente per archiviare il vettore normale calcolato e i dati derivati parziali.

</dd> <dt>

*pdwAdjacency* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per ogni viso che specifica i tre elementi adiacenti per ogni viso nella mesh. Il numero di byte in questa matrice deve essere di almeno 3 \* [**dimensioni GetNumFaces(DWORD).**](id3dxbasemesh--getnumfaces.md) \*

</dd> <dt>

*fPartialEdgeThreshold* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Specifica il coseno massimo dell'angolo in corrispondenza del quale due derivati parziali sono considerati incompatibili tra loro. Se il prodotto del punto della direzione dei due derivati parziali nei triangoli adiacenti è minore o uguale a questa soglia, i vertici condivisi tra questi triangoli verranno divisi.

</dd> <dt>

*fSingularPointThreshold* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Specifica la grandezza massima di una derivata parziale in corrispondenza della quale un vertice verrà considerato singolare. Poiché più triangoli sono imprevisti su un punto con fotogrammi tangenti vicini, ma si annullano completamente a vicenda (ad esempio nella parte superiore di una sfera), la grandezza della derivata parziale diminuisce. Se la grandezza è minore o uguale a questa soglia, il vertice verrà suddiviso per ogni triangolo che lo contiene.

</dd> <dt>

*fNormalEdgeThreshold* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Analogamente a fPartialEdgeThreshold, specifica il coseno massimo dell'angolo tra due normali, ovvero una soglia oltre la quale verranno suddivisi i vertici condivisi tra i triangoli. Se il prodotto del punto delle due normali è minore della soglia, i vertici condivisi verranno suddivisi, formando un bordo rigido tra i triangoli adiacenti. Se il prodotto punto è superiore alla soglia, i triangoli adiacenti avranno le normali interpolate.

</dd> <dt>

*ppMeshOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\*\***

Indirizzo di un puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di output che riceve i dati del vettore tangente, binormale e normale calcolati.

</dd> <dt>

*ppVertexMapping* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***

Indirizzo di un puntatore a un oggetto buffer [**ID3DXBuffer**](id3dxbuffer.md) di output che riceve un mapping dei nuovi vertici calcolati da questo metodo ai vertici originali. Il buffer è una matrice di DWORD, con le dimensioni della matrice definite come numero di vertici in ppMeshOut.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è S \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Una versione semplificata di questa funzione è disponibile [**come D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).

Il vettore normale calcolato in ogni vertice viene sempre normalizzato in modo da avere lunghezza unità.

La soluzione più affidabile per il calcolo delle coordinate cartesiane ortogonali consiste nel non impostare i flag D3DXTANGENT \_ ORTHOGONALIZE FROM you e \_ \_ D3DXTANGENT \_ ORTHOGONALIZE FROM V, in modo che le coordinate \_ \_ ortogonali siano calcolate dalle coordinate della trama sia dall'utente che da v. In questo caso, tuttavia, se u o v è zero, la funzione calcola le coordinate ortogonali usando D3DXTANGENT \_ ORTHOGONALIZE FROM V o \_ \_ D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U, rispettivamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
