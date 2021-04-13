---
description: Imposta la combinazione di chiavi di evento per la traccia di animazione specificata.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'Metodo ID3DXAnimationController:: KeyPriorityBlend (D3dx9anim. h)'
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
ms.openlocfilehash: 31778da9b26ddd79b5f05c69c822ed62a5b5281e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354259"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a>Metodo ID3DXAnimationController:: KeyPriorityBlend

Imposta la combinazione di chiavi di evento per la traccia di animazione specificata.

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

*NewBlendWeight* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Numero compreso tra 0 e 1 utilizzato per unire le tracce.

</dd> <dt>

*StartTime* \[ in\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Tempo globale per l'avvio di Blend.

</dd> <dt>

*Durata* \[ in\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Durata dell'ora globale della Blend.

</dd> <dt>

*Transizione* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**

Specifica il tipo di transizione usato per la durata della Blend. Vedere [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per l'evento di combinazione di priorità. Se uno o più parametri di input non sono validi oppure non è disponibile alcun evento libero, viene restituito **null** .

## <a name="remarks"></a>Commenti

Il controller di animazione si combina in tre fasi: le tracce con priorità bassa vengono combinate per prime, le tracce con priorità alta vengono mescolate secondo e i risultati di entrambe le operazioni vengono combinati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
