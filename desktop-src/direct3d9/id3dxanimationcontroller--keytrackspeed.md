---
description: Imposta un tasto evento che modifica la frequenza di riproduzione di una traccia di animazione.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: Metodo ID3DXAnimationController::KeyTrackSpeed (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 21ad7b0b1423a25ede319a623cad0a8b453af481d4aac5fae4e5bcce252dd31e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791191"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a>Metodo ID3DXAnimationController::KeyTrackSpeed

Imposta un tasto evento che modifica la frequenza di riproduzione di una traccia di animazione.

## <a name="syntax"></a>Sintassi


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
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

*NewSpeed* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Nuova velocità della traccia di animazione.

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

Specifica il tipo di transizione usato per la transizione tra le velocità. Vedere [**D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per l'evento di blend di priorità. **Se** uno o più parametri di input non sono validi o se non è disponibile alcun evento gratuito, viene restituito NULL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
