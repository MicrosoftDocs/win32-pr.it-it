---
description: Ottiene una descrizione dell'oggetto del tipo di carattere corrente.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'Metodo ID3DX10Font:: getdesc (D3DX10. h)'
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
ms.openlocfilehash: 59a7e361ebb6254fcc49eab30ff44ab39c38fd76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323162"
---
# <a name="id3dx10fontgetdesc-method"></a>Metodo ID3DX10Font:: getdesc

Ottiene una descrizione dell'oggetto del tipo di carattere corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* \[ in\]
</dt> <dd>

Tipo: **[ **d3dx10 \_ Font \_ desc**](d3dx10-font-desc.md)\***

Puntatore a una struttura del [**tipo di carattere d3dx10 che \_ \_**](d3dx10-font-desc.md) descrive l'oggetto del tipo di carattere. Se viene definito UNICODE, viene restituito un puntatore a un \_ DESCW D3DX10FONT; in caso contrario, viene restituito un puntatore a un D3DX10FONT \_ Desca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo descrive gli oggetti Font Unicode se è definito UNICODE. In caso contrario, viene chiamato getdesca, che restituisce un puntatore alla \_ struttura D3DX10FONT Desca.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




