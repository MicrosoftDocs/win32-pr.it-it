---
description: Restituisce un handle di evento all'evento successivo pianificato in modo che venga eseguito dopo un evento specificato in una traccia di animazione.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: 'Metodo ID3DXAnimationController:: GetUpcomingTrackEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969310"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a>Metodo ID3DXAnimationController:: GetUpcomingTrackEvent

Restituisce un handle di evento all'evento successivo pianificato in modo che venga eseguito dopo un evento specificato in una traccia di animazione.

## <a name="syntax"></a>Sintassi


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore di traccia.

</dd> <dt>

*hEvent* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per un evento specificato dopo il quale cercare un evento successivo. Se impostato su **null**, il metodo restituirà l'evento pianificato successivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per l'evento successivo pianificato per l'esecuzione nella traccia specificata. Se non è pianificato alcun nuovo evento, viene restituito **null** .

## <a name="remarks"></a>Commenti

Questo metodo può essere utilizzato in modo iterativo per individuare un evento desiderato passando ripetutamente **null** per hEvent.

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

 

 
