---
description: Disegna una striscia di linea nello spazio dello schermo con una matrice di trasformazione input specificata.
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: Metodo ID3DXLine::D rawTransform (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52407a8c92e626f8fe4d2df817017f81806cbae9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323476"
---
# <a name="id3dxlinedrawtransform-method"></a>ID3DXLine::D Metodo rawTransform

Disegna una striscia di linea nello spazio dello schermo con una matrice di trasformazione input specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVertexList* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Matrice di vertici che costituiscono la riga. Vedere [**D3DXVECTOR3**](d3dxvector3.md).

</dd> <dt>

*dwVertexListCount* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di vertici nell'elenco dei vertici.

</dd> <dt>

*pTransform* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matrice scale, Rotate e translate (SRT) per la trasformazione dei punti. Vedere [**D3DXMATRIX**](d3dxmatrix.md). Se questa matrice è una matrice di proiezione, tutte le righe di Stippled verranno disegnate con un modello punteggiatura con la prospettiva corretta. In alternativa, è possibile trasformare i vertici e usare [**ID3DXLine::D RAW**](id3dxline--draw.md) per tracciare la riga con un modello stipple senza prospettive-correct.

</dd> <dt>

*Colore* \[ in\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Colore della linea. Vedere [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
