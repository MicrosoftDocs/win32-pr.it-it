---
description: Imposta una chiave evento che modifica la frequenza di riproduzione di una traccia di animazione.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: 'Metodo ID3DXAnimationController:: KeyTrackSpeed (D3dx9anim. h)'
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
ms.openlocfilehash: 09705dd03e7767e94b1508cf4951186a509a3c5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323643"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a>Metodo ID3DXAnimationController:: KeyTrackSpeed

Imposta una chiave evento che modifica la frequenza di riproduzione di una traccia di animazione.

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

*Traccia* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore della traccia da modificare.

</dd> <dt>

*NewSpeed* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Nuova velocità della traccia dell'animazione.

</dd> <dt>

*StartTime* \[ in\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Chiave temporale globale. Specifica l'ora globale in cui verrà eseguita la modifica.

</dd> <dt>

*Durata* \[ in\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Tempo di transizione, che specifica il tempo necessario per il completamento della transizione senza problemi.

</dd> <dt>

*Transizione* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**

Specifica il tipo di transizione utilizzato per la transizione tra le velocità. Vedere [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per l'evento di combinazione di priorità. Se uno o più parametri di input non sono validi oppure non è disponibile alcun evento libero, viene restituito **null** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
