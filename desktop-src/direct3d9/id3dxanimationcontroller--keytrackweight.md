---
description: Imposta un tasto evento che modifica lo spessore di una traccia di animazione. Il peso viene usato come moltiplicatore quando si combinano più tracce.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: Metodo ID3DXAnimationController::KeyTrackWeight (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16bd95c675486b17f3071a279a01916e3db557c598830282f4d5b288dbc1f0fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026631"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a>Metodo ID3DXAnimationController::KeyTrackWeight

Imposta un tasto evento che modifica lo spessore di una traccia di animazione. Il peso viene usato come moltiplicatore quando si combinano più tracce.

## <a name="syntax"></a>Sintassi


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificatore della traccia da modificare.

</dd> <dt>

*NewWeight* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Nuovo peso della traccia.

</dd> <dt>

*StartTime* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Chiave temporale globale. Specifica l'ora globale in cui verrà apportata la modifica.

</dd> <dt>

*Durata* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Tempo di transizione, che specifica il tempo necessario per completare la transizione senza problemi.

</dd> <dt>

*Transizione* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md)**

Specifica il tipo di transizione utilizzato per la transizione tra pesi. Vedere [**D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per l'evento di blend di priorità. **Se** uno o più parametri di input non sono validi o se non è disponibile alcun evento gratuito, viene restituito NULL.

## <a name="remarks"></a>Commenti

Il peso viene usato come moltiplicatore per determinare la quantità di questa traccia da unire ad altre tracce.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
