---
description: Riordina un oggetto IContextNode figlio specificato in base all'indice specificato.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: Metodo IContextNode::MoveSubNodeToPosition (IACom.h)
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
ms.openlocfilehash: 8d48876be10a2c45daca62b3175a358d31ed128ddd3bcb045c052e2d51308c66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773821"
---
# <a name="icontextnodemovesubnodetoposition-method"></a>Metodo IContextNode::MoveSubNodeToPosition

Riordina un oggetto [**IContextNode figlio**](icontextnode.md) specificato in base all'indice specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSubnodeToMove* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) da spostare.

</dd> <dt>

*ulNewIndex* \[ Pollici\]
</dt> <dd>

Indice per la nuova posizione del sottonodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Restituisce **E \_ INVALIDARG** se *pSubnodeToMove* non è un nodo figlio di [**questo IContextNode.**](icontextnode.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




