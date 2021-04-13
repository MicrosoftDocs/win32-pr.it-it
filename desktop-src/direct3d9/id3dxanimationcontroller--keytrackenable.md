---
description: Imposta una chiave evento che Abilita o Disabilita una traccia dell'animazione.
ms.assetid: de81e646-0b94-40d3-89c2-060d118d17b2
title: 'Metodo ID3DXAnimationController:: KeyTrackEnable (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f22c732ff57e948ebcc2e89d790d352e4dc057ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354254"
---
# <a name="id3dxanimationcontrollerkeytrackenable-method"></a>Metodo ID3DXAnimationController:: KeyTrackEnable

Imposta una chiave evento che Abilita o Disabilita una traccia dell'animazione.

## <a name="syntax"></a>Sintassi


```C++
D3DXEVENTHANDLE KeyTrackEnable(
  [in] UINT   Track,
  [in] BOOL   NewEnable,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore della traccia dell'animazione da modificare.

</dd> <dt>

*NewEnable* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Abilita flag. Impostare su **true** per abilitare la traccia dell'animazione oppure su **false** per disabilitare la traccia.

</dd> <dt>

*StartTime* \[ in\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Chiave temporale globale. Specifica l'ora globale in cui verrà eseguita la modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per l'evento di combinazione di priorità. Se Track non è valido, viene restituito **null** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
