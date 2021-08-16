---
description: Imposta la velocità della traccia. La velocità della traccia è simile a un moltiplicatore usato per velocizzare o rallentare la riproduzione della traccia.
ms.assetid: b3946b61-0676-4690-9844-639fabd8fd7c
title: Metodo ID3DXAnimationController::SetTrackSpeed (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 62cd882dd95446c92dd4192528322ed54708496183a3557aa89d53bc5dac138b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522360"
---
# <a name="id3dxanimationcontrollersettrackspeed-method"></a>Metodo ID3DXAnimationController::SetTrackSpeed

Imposta la velocità della traccia. La velocità della traccia è simile a un moltiplicatore usato per velocizzare o rallentare la riproduzione della traccia.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTrackSpeed(
  [in] UINT  Track,
  [in] FLOAT Speed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificatore della traccia su cui impostare la velocità.

</dd> <dt>

*Velocità* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Nuova velocità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
