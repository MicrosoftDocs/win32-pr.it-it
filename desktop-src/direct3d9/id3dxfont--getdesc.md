---
description: Ottiene una descrizione dell'oggetto del tipo di carattere corrente. GetDescW e getdesca sono identici a questo metodo, ad eccezione del fatto che un puntatore viene restituito a una \_ struttura D3DXFONT DESCW o D3DXFONT \_ desca, rispettivamente.
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'Metodo ID3DXFont:: getdesc (D3dx9core. h)'
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
ms.openlocfilehash: 3310971e360fb9994a30d62349d3e7e4b764c7d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322618"
---
# <a name="id3dxfontgetdesc-method"></a>Metodo ID3DXFont:: getdesc

Ottiene una descrizione dell'oggetto del tipo di carattere corrente. GetDescW e getdesca sono identici a questo metodo, ad eccezione del fatto che un puntatore viene restituito a una struttura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) o **D3DXFONT \_ Desca** , rispettivamente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXFONT \_ desc**](d3dxfont-desc.md)\***

Puntatore a una struttura [**D3DXFONT \_ desc**](d3dxfont-desc.md) che descrive l'oggetto del tipo di carattere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo descrive gli oggetti Font Unicode se è definito UNICODE. In caso contrario, viene chiamato getdesca, che restituisce un puntatore alla struttura [**D3DXFONT \_ Desca**](d3dxfont-desc.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 




