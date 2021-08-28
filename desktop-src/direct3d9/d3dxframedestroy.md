---
description: Elimina il sottoalbero dei frame nella radice, inclusa la radice.
ms.assetid: 0bbb529f-01d8-430b-a72b-4af5f7a71253
title: Funzione D3DXFrameDestroy (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameDestroy
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4e20e878b402ad0b8c4d0a9b721cd9300154305b2a06426564d1639ceddd7a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988481"
---
# <a name="d3dxframedestroy-function"></a>Funzione D3DXFrameDestroy

Elimina il sottoalbero dei frame nella radice, inclusa la radice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXFrameDestroy(
  _In_ LPD3DXFRAME             pFrameRoot,
  _In_ LPD3DXALLOCATEHIERARCHY pAlloc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFrameRoot* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Puntatore al nodo radice.

</dd> <dt>

*pAlloc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Interfaccia di allocazione utilizzata per deallocare i nodi della gerarchia dei frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di animazione](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




