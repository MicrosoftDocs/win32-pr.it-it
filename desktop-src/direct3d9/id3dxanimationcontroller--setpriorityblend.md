---
description: Imposta il peso di fusione della priorità usato dal controller di animazione.
ms.assetid: b053024b-f219-48b3-906e-161d9cf47556
title: Metodo ID3DXAnimationController::SetPriorityBlend (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e52c08d0731bc89135df4547fcfc88e94b56b826d2ccab338576a22651376d94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069111"
---
# <a name="id3dxanimationcontrollersetpriorityblend-method"></a>Metodo ID3DXAnimationController::SetPriorityBlend

Imposta il peso di fusione della priorità usato dal controller di animazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPriorityBlend(
  [in] FLOAT BlendWeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*BlendWeight* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Peso di fusione della priorità usato dal controller di animazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Il peso della fusione viene usato per unire le tracce con priorità alta e bassa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**GetPriorityBlend**](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
