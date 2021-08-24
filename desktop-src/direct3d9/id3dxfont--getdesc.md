---
description: Ottiene una descrizione dell'oggetto tipo di carattere corrente. GetDescW e GetDescA sono identici a questo metodo, ad eccezione del fatto che un puntatore viene restituito rispettivamente a una struttura D3DXFONT \_ DESCW o D3DXFONT \_ DESCA.
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: Metodo ID3DXFont::GetDesc (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2961c69e47bb46eaf782e8f5d4dbfe0be2d82a49f00f98c36b1ee7b141e962b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675431"
---
# <a name="id3dxfontgetdesc-method"></a>Metodo ID3DXFont::GetDesc

Ottiene una descrizione dell'oggetto tipo di carattere corrente. GetDescW e GetDescA sono identici a questo metodo, ad eccezione del fatto che un puntatore viene restituito rispettivamente a una struttura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) o **D3DXFONT \_ DESCA.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXFONT \_ DESC**](d3dxfont-desc.md)\***

Puntatore a una [**struttura \_ DESC D3DXFONT**](d3dxfont-desc.md) che descrive l'oggetto tipo di carattere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo descrive gli oggetti carattere Unicode se è definito UNICODE. In caso contrario, viene chiamato GetDescA, che restituisce un puntatore alla struttura [**\_ DESCA D3DXFONT.**](d3dxfont-desc.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 




