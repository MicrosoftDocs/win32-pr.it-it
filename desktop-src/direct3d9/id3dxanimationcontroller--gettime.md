---
description: Ottiene il tempo di animazione globale.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: 'Metodo ID3DXAnimationController:: getTime (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bfc3c2c1d5bb0bbbb3c364b47f22f0790f8d102
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323058"
---
# <a name="id3dxanimationcontrollergettime-method"></a>Metodo ID3DXAnimationController:: getTime

Ottiene il tempo di animazione globale.

## <a name="syntax"></a>Sintassi


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Restituisce il tempo di animazione globale.

## <a name="remarks"></a>Commenti

Le animazioni sono progettate usando un'ora di animazione locale e vengono combinate in tempi globali con [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
