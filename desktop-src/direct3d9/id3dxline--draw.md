---
description: Disegna un elenco di linee nello spazio dello schermo. L'input è sotto forma di matrice che definisce i punti (di D3DXVECTOR2) sull'elenco di linee.
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: Metodo ID3DXLine::D raw (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3cb8d55efffb58afefd7c42a6105131da83c48e1731b9d814d5af73f8c3f4f41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987351"
---
# <a name="id3dxlinedraw-method"></a>Metodo ID3DXLine::D raw

Disegna un elenco di linee nello spazio dello schermo. L'input è sotto forma di matrice che definisce i punti (di [**D3DXVECTOR2)**](d3dxvector2.md)nell'elenco di linee.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Draw(
  [in] const D3DXVECTOR2 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVertexList* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Matrice di vertici che costituiscono la linea. Vedere [**D3DXVECTOR2.**](d3dxvector2.md)

</dd> <dt>

*dwVertexListCount* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di vertici nell'elenco dei vertici.

</dd> <dt>

*Colore* \[ Pollici\]
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
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
