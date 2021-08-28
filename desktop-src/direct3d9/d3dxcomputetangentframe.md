---
description: Calcolare vettori tangenti, binormali e normali per una mesh.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: Funzione D3DXComputeTangentFrame (D3DX9Mesh.h)
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
ms.openlocfilehash: 532b265f387179d88581f6f0a05227162de6a8402e324e7be2e13a16ca4a3ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849831"
---
# <a name="d3dxcomputetangentframe-function"></a>Funzione D3DXComputeTangentFrame

Calcolare vettori tangenti, binormali e normali per una mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***

Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di input.

</dd> <dt>

*dwOptions* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o [**più flag D3DXTANGENT.**](./d3dxtangent.md)

Usare **NULL** per specificare le opzioni seguenti:

-   Ponderare la lunghezza normale del vettore in base all'angolo, in radianti, sottotendato dai due bordi che lasciano il vertice.
-   Calcolare le coordinate cartesiane ortogonali dalle coordinate della trama UV.
-   Le trame non vengono incapsulate nelle direzioni U o V
-   I derivati parziali rispetto alle coordinate della trama vengono normalizzati.
-   I vertici vengono ordinati in senso antiorario intorno a ogni triangolo.
-   Usare vettori normali per vertice già presenti nella mesh di input.
-   I risultati verranno archiviati nella mesh di input originale. La funzione avrà esito negativo se è necessario creare nuovi vertici.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è S \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questa funzione chiama semplicemente [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con i parametri di input seguenti:


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



Le singolarità vengono gestite in base alle esigenze raggruppando gli bordi e suddividendo i vertici. Se è necessario suddividere i vertici, la funzione avrà esito negativo. Il vettore normale calcolato in ogni vertice viene sempre normalizzato in modo da avere una lunghezza unità.

La soluzione più affidabile per il calcolo delle coordinate cartesiane ortogonali consiste nel non impostare flag D3DXTANGENT \_ ORTHOGONALIZE \_ FROM you e \_ D3DXTANGENT \_ ORTHOGONALIZE FROM V, in modo che le coordinate \_ \_ ortogonali siano calcolate da entrambe le coordinate della trama UV. Tuttavia, in questo caso, se U o V è zero, la funzione calcola le coordinate ortogonali usando D3DXTANGENT \_ ORTHOGONALIZE FROM V o \_ \_ D3DXTANGENT \_ ORTHOGONALIZE \_ FROM U \_ rispettivamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> <dt>

[**D3DXTANGENT**](./d3dxtangent.md)
</dt> </dl>

 

 
