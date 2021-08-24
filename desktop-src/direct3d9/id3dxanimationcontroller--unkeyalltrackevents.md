---
description: Rimuove tutti gli eventi da una traccia di animazione specificata.
ms.assetid: 25c4d04a-0d75-4113-ad90-db84aa937098
title: Metodo ID3DXAnimationController::UnkeyAllTrackEvents (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyAllTrackEvents
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 196f1041d725f8aed39e54626e00b849f2be09587d5ccd40fbc3d8a091fc1b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791111"
---
# <a name="id3dxanimationcontrollerunkeyalltrackevents-method"></a>Metodo ID3DXAnimationController::UnkeyAllTrackEvents

Rimuove tutti gli eventi da una traccia di animazione specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnkeyAllTrackEvents(
  [in] UINT Track
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificatore della traccia in cui devono essere rimossi tutti gli eventi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo impedisce l'esecuzione di tutti gli eventi pianificati in precedenza nella traccia e rimuove tutti i dati associati a tali eventi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
