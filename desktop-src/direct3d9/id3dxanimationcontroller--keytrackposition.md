---
description: Imposta una chiave evento che modifica l'ora locale di una traccia di animazione.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: 'Metodo ID3DXAnimationController:: KeyTrackPosition (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d027069efa9fb49cad3d2344da593eae4c3c844c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355509"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a>Metodo ID3DXAnimationController:: KeyTrackPosition

Imposta una chiave evento che modifica l'ora locale di una traccia di animazione.

## <a name="syntax"></a>Sintassi


```C++
D3DXEVENTHANDLE KeyTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE NewPosition,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore della traccia da modificare.

</dd> <dt>

*NewPosition* \[ in\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Nuova ora locale della traccia dell'animazione.

</dd> <dt>

*StartTime* \[ in\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Chiave temporale globale. Specifica l'ora globale in cui verrà eseguita la modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per l'evento di combinazione di priorità. Viene restituito **null** se Track non è valido o se non è disponibile alcun evento free.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
