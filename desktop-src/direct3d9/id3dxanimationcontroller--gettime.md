---
description: Ottiene il tempo di animazione globale.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: Metodo ID3DXAnimationController::GetTime (D3dx9anim.h)
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
ms.openlocfilehash: b6241bbd8c447889a4718369feabf8f26dacc73c58b8e6826c1797d0639422fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987831"
---
# <a name="id3dxanimationcontrollergettime-method"></a>Metodo ID3DXAnimationController::GetTime

Ottiene il tempo di animazione globale.

## <a name="syntax"></a>Sintassi


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Restituisce il tempo di animazione globale.

## <a name="remarks"></a>Commenti

Le animazioni sono progettate usando un'ora di animazione locale e miste all'ora globale con [**AdvanceTime.**](id3dxanimationcontroller--advancetime.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
