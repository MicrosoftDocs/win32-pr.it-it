---
description: Imposta una chiave evento che modifica il peso di una traccia di animazione. Il peso viene usato come moltiplicatore quando si combinano più tracce.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: 'Metodo ID3DXAnimationController:: KeyTrackWeight (D3dx9anim. h)'
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
ms.openlocfilehash: 74f5e38392f6b4ac192f02b9d85421c8357a16ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323293"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a>Metodo ID3DXAnimationController:: KeyTrackWeight

Imposta una chiave evento che modifica il peso di una traccia di animazione. Il peso viene usato come moltiplicatore quando si combinano più tracce.

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

*Traccia* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore della traccia da modificare.

</dd> <dt>

*NewWeight* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Nuovo peso della traccia.

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

Specifica il tipo di transizione utilizzato per la transizione tra pesi. Vedere [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per l'evento di combinazione di priorità. Se uno o più parametri di input non sono validi oppure non è disponibile alcun evento libero, viene restituito **null** .

## <a name="remarks"></a>Commenti

Il peso viene usato come un moltiplicatore per determinare la quantità di questa traccia da unire insieme ad altre tracce.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
