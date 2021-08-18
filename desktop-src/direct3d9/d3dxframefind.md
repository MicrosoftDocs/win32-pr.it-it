---
description: Trova il frame figlio di un frame radice.
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: Funzione D3DXFrameFind (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f62cacabbf020d1fe9ff9e83c47acc6c58e52c4ab6be031586bda365745f595
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027661"
---
# <a name="d3dxframefind-function"></a>Funzione D3DXFrameFind

Trova il frame figlio di un frame radice.

## <a name="syntax"></a>Sintassi


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFrameRoot* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Puntatore al frame radice. Vedere [**D3DXFRAME.**](d3dxframe.md)

</dd> <dt>

*Nome* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome del frame figlio da trovare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Restituisce il frame figlio se viene trovato oppure **NULL in caso contrario.** Vedere [**D3DXFRAME.**](d3dxframe.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di animazione](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
