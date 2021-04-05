---
description: Reimposta il tempo di animazione globale su zero. Tutti gli eventi in sospeso manterranno le pianificazioni originali, ma nel nuovo intervallo di tempo.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: 'Metodo ID3DXAnimationController:: ResetTime (D3dx9anim. h)'
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
ms.openlocfilehash: 1206cc8514f3e7eb235f1072bf2a66c4b5bf1e7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762209"
---
# <a name="id3dxanimationcontrollerresettime-method"></a>Metodo ID3DXAnimationController:: ResetTime

Reimposta il tempo di animazione globale su zero. Tutti gli eventi in sospeso manterranno le pianificazioni originali, ma nel nuovo intervallo di tempo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo viene in genere utilizzato quando il valore del tempo di animazione globale è prossimo alla precisione massima della doppia archiviazione o 2 ⁶ ⁴-1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




