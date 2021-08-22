---
description: Ottiene una descrizione dell'oggetto tipo di carattere corrente.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: Metodo ID3DX10Font::GetDesc (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d684a0bf485db441a0a6bf23cd36496cc13fdfe766eaa890682259b76b3800c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990441"
---
# <a name="id3dx10fontgetdesc-method"></a>Metodo ID3DX10Font::GetDesc

Ottiene una descrizione dell'oggetto tipo di carattere corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ FONT \_ DESC**](d3dx10-font-desc.md)\***

Puntatore a una [**struttura D3DX10 \_ FONT \_ DESC**](d3dx10-font-desc.md) che descrive l'oggetto tipo di carattere. Se viene definito UNICODE, viene restituito un puntatore a un D3DX10FONT DESCW; in caso contrario, viene restituito un puntatore \_ a un D3DX10FONT \_ DESCA.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo descrive gli oggetti carattere Unicode se è definito UNICODE. In caso contrario, viene chiamato GetDescA, che restituisce un puntatore alla struttura DESCA D3DX10FONT. \_

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




