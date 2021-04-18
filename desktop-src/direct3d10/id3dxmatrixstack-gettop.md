---
description: Recupera la matrice corrente all'inizio dello stack.
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: 'Metodo ID3DXMATRIXStack:: GetTop (D3DX10. h)'
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
ms.openlocfilehash: c545287ff3a4e7f9bfdccf21b9351fef06367433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323666"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a>Metodo ID3DXMATRIXStack:: GetTop (D3DX10. h)

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

Il puntatore D3DXMATRIX restituito da questo metodo non è garantito come valido dopo le operazioni di stack successive.

Si noti che questo metodo non rimuove la matrice corrente dall'inizio dello stack. piuttosto restituisce solo la matrice corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
