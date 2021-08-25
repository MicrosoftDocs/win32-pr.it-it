---
description: Reimposta il tempo di animazione globale su zero. Tutti gli eventi in sospeso manterranno le pianificazioni originali, ma nel nuovo intervallo di tempo.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: Metodo ID3DXAnimationController::ResetTime (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ResetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3f5f4ba6f10d5119e479a56e9e207e410b2d1e817d6809e7ceac1c98c8d2ee5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893741"
---
# <a name="id3dxanimationcontrollerresettime-method"></a>Metodo ID3DXAnimationController::ResetTime

Reimposta il tempo di animazione globale su zero. Tutti gli eventi in sospeso manterranno le pianificazioni originali, ma nel nuovo intervallo di tempo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo viene in genere usato quando il valore del tempo di animazione globale è prossimo alla precisione massima dell'archiviazione DOUBLE o 2⁶⁴ - 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




