---
description: Restituisce un handle di evento per l'evento di blend di priorità successivo pianificato dopo un evento specificato.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: Metodo ID3DXAnimationController::GetUpcomingPriorityBlend (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c58bf5e2a8736db98e0461988f984709e756d269d09c74dd673356676702ff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849081"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a>Metodo ID3DXAnimationController::GetUpcomingPriorityBlend

Restituisce un handle di evento per l'evento di blend di priorità successivo pianificato dopo un evento specificato.

## <a name="syntax"></a>Sintassi


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hEvent* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per un evento specificato dopo il quale cercare un evento di blend di priorità seguente. Se impostato su **NULL,** il metodo restituirà il successivo evento di blend di priorità pianificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per il successivo evento di combinazione di priorità pianificato. Se non è pianificato alcun nuovo evento di combinazione di priorità, viene restituito **NULL.**

## <a name="remarks"></a>Commenti

Questo metodo può essere usato in modo iterativo per individuare un evento di blend di priorità desiderato passando ripetutamente **NULL** per hEvent.

> [!Note]  
> Non eseguire ulteriori iterazioni dopo che il metodo ha restituito **NULL.**

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




