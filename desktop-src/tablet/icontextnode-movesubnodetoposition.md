---
description: Riordina un oggetto IContextNode figlio specificato nell'indice specificato.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'Metodo IContextNode:: MoveSubNodeToPosition (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307421"
---
# <a name="icontextnodemovesubnodetoposition-method"></a>Metodo IContextNode:: MoveSubNodeToPosition

Riordina un oggetto [**IContextNode**](icontextnode.md) figlio specificato nell'indice specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSubnodeToMove* \[ in\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) da spostare.

</dd> <dt>

*ulNewIndex* \[ in\]
</dt> <dd>

Indice per la nuova posizione del sottonodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Restituisce **E \_ INVALIDARG** se *pSubnodeToMove* non è un nodo figlio di questo [**IContextNode**](icontextnode.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode:: CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




