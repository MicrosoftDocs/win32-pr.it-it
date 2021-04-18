---
description: Recupera la matrice corrente all'inizio dello stack.
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: 'Metodo ID3DXMATRIXStack:: GetTop (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e635f2a825bf73234322066910c15af636ec9d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322338"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a>Metodo ID3DXMATRIXStack:: GetTop (D3dx9math. h)

Recupera la matrice corrente all'inizio dello stack.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Questo metodo restituisce un puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice corrente.

## <a name="remarks"></a>Commenti

Il puntatore [**D3DXMATRIX**](d3dxmatrix.md) restituito da questo metodo non è garantito come valido dopo le operazioni di stack successive.

Si noti che questo metodo non rimuove la matrice corrente dall'inizio dello stack. piuttosto restituisce solo la matrice corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P USH**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




