---
description: Restituisce un handle di evento per l'evento successivo pianificato per verificarsi dopo un evento specificato in una traccia di animazione.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: Metodo ID3DXAnimationController::GetUpcomingTrackEvent (D3dx9anim.h)
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
ms.openlocfilehash: a6e2730a9649400af8cc0229cb69ab695044681fde43a29a1a784d212f8d2641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279031"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a>Metodo ID3DXAnimationController::GetUpcomingTrackEvent

Restituisce un handle di evento per l'evento successivo pianificato per verificarsi dopo un evento specificato in una traccia di animazione.

## <a name="syntax"></a>Sintassi


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tenere traccia* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificatore di traccia.

</dd> <dt>

*hEvent* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per un evento specificato dopo il quale cercare un evento seguente. Se impostato su **NULL,** il metodo restituirà l'evento pianificato successivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle dell'evento per l'evento successivo pianificato per l'esecuzione sulla traccia specificata. Se non è pianificato alcun nuovo evento, viene restituito **NULL.**

## <a name="remarks"></a>Commenti

Questo metodo può essere usato in modo iterativo per individuare un evento desiderato passando ripetutamente **NULL** per hEvent.

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

 

 
