---
description: Vettori di calcolo tangente, binormali e normali per una rete mesh.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: Funzione D3DXComputeTangentFrame (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b95d8f046499716a2c7972593093dfb409b11f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323426"
---
# <a name="d3dxcomputetangentframe-function"></a>D3DXComputeTangentFrame (funzione)

Vettori di calcolo tangente, binormali e normali per una rete mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***

Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di input.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più flag [**D3DXTANGENT**](./d3dxtangent.md) .

Utilizzare **null** per specificare le opzioni seguenti:

-   Ponderare la lunghezza del vettore normale in base all'angolo, in radianti, in base ai due bordi che lasciano il vertice.
-   Calcola le coordinate cartesiane ortogonali dalle coordinate di trama UV.
-   Non è possibile eseguire il wrapper delle trame nelle direzioni U o V
-   Le derivazioni parziali rispetto alle coordinate di trama vengono normalizzate.
-   I vertici vengono ordinati in senso antiorario intorno a ogni triangolo.
-   Usare vettori normali per vertice già presenti nella mesh di input.
-   I risultati verranno archiviati nella mesh di input originale. La funzione avrà esito negativo se è necessario creare nuovi vertici.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questa funzione chiama semplicemente [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con i parametri di input seguenti:


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



Le singolarità vengono gestite come richiesto raggruppando i bordi e suddividendo i vertici. Se è necessario suddividere i vertici, la funzione avrà esito negativo. Il vettore normale calcolato a ogni vertice è sempre normalizzato per avere una lunghezza di unità.

La soluzione più affidabile per calcolare le coordinate cartesiane ortogonali consiste nel non impostare i flag D3DXTANGENT \_ ORTHOGONALIZE \_ \_ e D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ V, in modo che le coordinate ortogonali vengano calcolate da entrambe le coordinate di trama UV. Tuttavia, in questo caso, se U o V è zero, la funzione calcolerà le coordinate ortogonali usando D3DXTANGENT \_ ORTHOGONALIZE \_ \_ rispettivamente da V o D3DXTANGENT \_ ORTHOGONALIZE \_ from \_ U.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> <dt>

[**D3DXTANGENT**](./d3dxtangent.md)
</dt> </dl>

 

 
