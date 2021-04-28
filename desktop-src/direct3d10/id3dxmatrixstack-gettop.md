---
description: "Metodo ID3DXMATRIXStack::GetTop (D3DX10.h): recupera la matrice corrente all'inizio dello stack."
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: Metodo ID3DXMATRIXStack::GetTop (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d96cfe8124b47a9b6ce546379af1313a02ea26
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108039"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a>Metodo ID3DXMATRIXStack::GetTop (D3DX10.h)

Recupera la matrice corrente all'inizio dello stack.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Questo metodo restituisce un puntatore a una struttura D3DXMATRIX che rappresenta la matrice corrente.

## <a name="remarks"></a>Commenti

Non è garantito che il puntatore D3DXMATRIX restituito da questo metodo sia valido dopo le successive operazioni dello stack.

Si noti che questo metodo non rimuove la matrice corrente dall'inizio dello stack. restituisce invece solo la matrice corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
