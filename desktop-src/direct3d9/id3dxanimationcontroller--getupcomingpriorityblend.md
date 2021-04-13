---
description: Restituisce un handle di evento per l'evento di Blend di priorità successivo pianificato per essere eseguito dopo un evento specificato.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: 'Metodo ID3DXAnimationController:: GetUpcomingPriorityBlend (D3dx9anim. h)'
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
ms.openlocfilehash: 72f9b8854041094d43d9e8250ab61b5f59a67848
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401926"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a>Metodo ID3DXAnimationController:: GetUpcomingPriorityBlend

Restituisce un handle di evento per l'evento di Blend di priorità successivo pianificato per essere eseguito dopo un evento specificato.

## <a name="syntax"></a>Sintassi


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hEvent* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per un evento specificato dopo il quale cercare un evento di combinazione di priorità successivo. Se impostato su **null**, il metodo restituirà l'evento di Blend di priorità pianificato successivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per l'evento di Blend di priorità successivo pianificato. Viene restituito **null** se non è pianificato alcun nuovo evento di Blend di priorità.

## <a name="remarks"></a>Commenti

Questo metodo può essere utilizzato in modo iterativo per individuare un evento di Blend di priorità desiderato passando ripetutamente **null** per hEvent.

> [!Note]  
> Non scorrere ulteriormente dopo che il metodo ha restituito **null**.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




