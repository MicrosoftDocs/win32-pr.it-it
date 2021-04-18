---
description: Esegue calcoli del fotogramma tangente su una mesh. Vengono generati i vettori tangenti, binormali e facoltativamente normali. Le singolarità vengono gestite come richiesto raggruppando i bordi e suddividendo i vertici.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: Funzione D3DXComputeTangentFrameEx (D3DX9Mesh. h)
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
ms.openlocfilehash: 58c7e8a1f1f7247d6a3ecc92d5771d68c9c3e5a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322318"
---
# <a name="d3dxcomputetangentframeex-function"></a>D3DXComputeTangentFrameEx (funzione)

Esegue calcoli del fotogramma tangente su una mesh. Vengono generati i vettori tangenti, binormali e facoltativamente normali. Le singolarità vengono gestite come richiesto raggruppando i bordi e suddividendo i vertici.

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

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***

Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di input.

</dd> <dt>

*dwTextureInSemantic* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica la semantica di input delle coordinate di trama. Se D3DX \_ è impostato su default, la funzione presuppone che non esistano coordinate di trama e la funzione avrà esito negativo a meno che non venga specificato il normale calcolo vettoriale.

</dd> <dt>

*dwTextureInIndex* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Se una mesh ha più coordinate di trama, specifica la coordinata di trama da usare per i calcoli del fotogramma tangente. Se è zero, la mesh dispone solo di una singola coordinata di trama.

</dd> <dt>

*dwUPartialOutSemantic* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica la semantica di output per il tipo, in genere D3DDECLUSAGE \_ tangente, che descrive la posizione in cui verrà archiviata la derivata parziale rispetto alla coordinata di trama U. Se D3DX \_ è impostato su default, questo derivato parziale non verrà archiviato.

</dd> <dt>

*dwUPartialOutIndex* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica l'indice semantico in cui archiviare la derivata parziale rispetto alla coordinata di trama U.

</dd> <dt>

*dwVPartialOutSemantic* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica il tipo [**D3DDECLUSAGE**](./d3ddeclusage.md) , in genere D3DDECLUSAGE \_ Binormal, che descrive la posizione in cui verrà archiviata la derivata parziale rispetto alla coordinata di trama V. Se D3DX \_ è impostato su default, questo derivato parziale non verrà archiviato.

</dd> <dt>

*dwVPartialOutIndex* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica l'indice semantico in cui archiviare la derivata parziale rispetto alla coordinata di trama V.

</dd> <dt>

*dwNormalOutSemantic* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica la semantica normale di output, in genere D3DDECLUSAGE \_ normale, che descrive la posizione in cui verrà archiviato il vettore normale in ogni vertice. Se D3DX \_ è impostato su default, questo vettore normale non verrà archiviato.

</dd> <dt>

*dwNormalOutIndex* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica l'indice semantico in cui archiviare il vettore normale a ogni vertice.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più flag [**D3DXTANGENT**](./d3dxtangent.md) che specificano le opzioni di calcolo del frame tangente. Se **null**, verranno specificate le opzioni seguenti:



| Descrizione                                                                                              | [**D3DXTANGENT**](./d3dxtangent.md) Valore del flag                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Ponderare la lunghezza del vettore normale in base all'angolo, in radianti, in base ai due bordi che lasciano il vertice. | &. (D3DXTANGENT \_ PESO \_ per \_ area \| D3DXTANGENT \_ peso \_ uguale)                |
| Calcola le coordinate cartesiane ortogonali dalle coordinate di trama (u, v). Vedere la sezione Osservazioni.                   | &. (D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ U \| D3DXTANGENT \_ ORTHOGONALIZE \_ from \_ V) |
| Non è possibile eseguire il wrapper delle trame nelle direzioni u o v                                                     | &. (D3DXTANGENT \_ a capo \_ UV)                                                      |
| Le derivazioni parziali rispetto alle coordinate di trama vengono normalizzate.                                  | &. (D3DXTANGENT \_ non \_ normalizzare i \_ parziali)                                     |
| I vertici vengono ordinati in senso antiorario intorno a ogni triangolo.                               | &. (D3DXTANGENT \_ \_CW vento)                                                      |
| Usare vettori normali per vertice già presenti nella mesh di input.                                         | &. (D3DXTANGENT \_ Calcola \_ normali)                                            |



 

Se D3DXTANGENT \_ generate \_ sul \_ posto non è impostato, la mesh di input viene clonata. La mesh originale deve quindi disporre di spazio sufficiente per archiviare il vettore normale calcolato e i dati parziali derivati.

</dd> <dt>

*pdwAdjacency* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh. Il numero di byte in questa matrice deve essere almeno 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> <dt>

*fPartialEdgeThreshold* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Specifica il coseno massimo dell'angolo in corrispondenza del quale due derivati parziali sono considerati incompatibili tra loro. Se il prodotto punto della direzione dei due derivati parziali nei triangoli adiacenti è minore o uguale a questa soglia, i vertici condivisi tra questi triangoli verranno divisi.

</dd> <dt>

*fSingularPointThreshold* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Specifica la grandezza massima di una derivata parziale in corrispondenza della quale un vertice verrà considerato singolare. Poiché più triangoli sono un evento imprevisto in un punto in cui sono presenti frame tangente adiacenti, ma si annulla completamente l'uno dall'altro (ad esempio, nella parte superiore di una sfera), la grandezza della derivata parziale diminuirà. Se la grandezza è minore o uguale a questa soglia, il vertice verrà diviso per ogni triangolo che lo contiene.

</dd> <dt>

*fNormalEdgeThreshold* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Analogamente a fPartialEdgeThreshold, specifica il coseno massimo dell'angolo tra due normali che rappresenta una soglia oltre la quale i vertici condivisi tra triangoli verranno divisi. Se il prodotto dot delle due normali è inferiore alla soglia, i vertici condivisi verranno suddivisi, formando un bordo rigido tra triangoli adiacenti. Se il prodotto punto è superiore alla soglia, i triangoli adiacenti avranno le normali interpolate.

</dd> <dt>

*ppMeshOut* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\*\***

Indirizzo di un puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di output che riceve i dati di vettore di tangente, binormali e normali calcolati.

</dd> <dt>

*ppVertexMapping* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***

Indirizzo di un puntatore a un oggetto buffer [**ID3DXBuffer**](id3dxbuffer.md) di output che riceve un mapping dei nuovi vertici calcolati da questo metodo ai vertici originali. Il buffer è una matrice di DWORD, con le dimensioni della matrice definite come numero di vertici in ppMeshOut.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Una versione semplificata di questa funzione è disponibile come [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).

Il vettore normale calcolato a ogni vertice è sempre normalizzato per avere una lunghezza di unità.

La soluzione più affidabile per calcolare le coordinate cartesiane ortogonali consiste nel non impostare i flag D3DXTANGENT \_ ORTHOGONALIZE \_ \_ e D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ V, in modo che le coordinate ortogonali vengano calcolate da entrambe le coordinate di trama e V. Tuttavia, in questo caso, se u o v è zero, la funzione calcolerà le coordinate ortogonali usando D3DXTANGENT \_ ORTHOGONALIZE \_ \_ rispettivamente da v o D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ u.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
