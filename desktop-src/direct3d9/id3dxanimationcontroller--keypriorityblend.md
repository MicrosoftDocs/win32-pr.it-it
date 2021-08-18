---
description: Imposta i tasti evento di fusione per la traccia di animazione specificata.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: Metodo ID3DXAnimationController::KeyPriorityBlend (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33d2b4e18fc93dff3054a98442c86a4c05467898afe09fc3bc82ccbd2f0ba456
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279041"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a>Metodo ID3DXAnimationController::KeyPriorityBlend

Imposta i tasti evento di fusione per la traccia di animazione specificata.

## <a name="syntax"></a>Sintassi


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewBlendWeight* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Numero compreso tra 0 e 1 usato per unire le tracce.

</dd> <dt>

*StartTime* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Ora globale per avviare la fusione.

</dd> <dt>

*Durata* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Durata temporale globale della fusione.

</dd> <dt>

*Transizione* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md)**

Specifica il tipo di transizione utilizzato per la durata della fusione. Vedere [**D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle dell'evento per l'evento di combinazione di priorità. **Viene** restituito NULL se uno o più parametri di input non sono validi o se non è disponibile alcun evento gratuito.

## <a name="remarks"></a>Commenti

Il controller di animazione si combina in tre fasi: le tracce con priorità bassa vengono combinate per prime, le tracce con priorità alta vengono combinate in seconda e quindi i risultati di entrambe le fasi vengono sfusi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
