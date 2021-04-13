---
description: Restituisce la posizione dell'ora nell'intervallo di tempo locale di un set di animazioni.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'Metodo ID3DXAnimationSet:: GetPeriodicPosition (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3c4f2e8e57efdfe0681b8ae691e0b5de42624e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355934"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a>Metodo ID3DXAnimationSet:: GetPeriodicPosition

Restituisce la posizione dell'ora nell'intervallo di tempo locale di un set di animazioni.

## <a name="syntax"></a>Sintassi


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Posizione* \[ in\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Ora locale del set di animazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Posizione dell'ora misurata nell'intervallo di tempo del set di animazioni. Questo valore verrà limitato in base al periodo del set di animazioni.

## <a name="remarks"></a>Commenti

La posizione temporale restituita da questo metodo può essere utilizzata come parametro PeriodicPosition di [**ID3DXAnimationSet:: GetSRT**](id3dxanimationset--getsrt.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
