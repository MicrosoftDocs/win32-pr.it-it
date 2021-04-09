---
description: Crea un nuovo oggetto IContextNode figlio.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: 'Metodo IContextNode:: CreateSubNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 02c10cc50b90b96cc1ce4aadfa97f86a6c516ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879365"
---
# <a name="icontextnodecreatesubnode-method"></a>Metodo IContextNode:: CreateSubNode

Crea un nuovo oggetto [**IContextNode**](icontextnode.md) figlio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNodeType* \[ in\]
</dt> <dd>

**GUID** che rappresenta il tipo di [**IContextNode**](icontextnode.md) da creare.

</dd> <dt>

*ppContextNodeCreated* \[ out\]
</dt> <dd>

Puntatore al nuovo [**IContextNode**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppContextNodeCreated* quando non è più necessario usare il nodo di contesto.

 

Il nuovo [**IContextNode**](icontextnode.md) viene aggiunto alla raccolta di nodi figlio del nodo di contesto (vedere [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)). Quando sono presenti nodi figlio esistenti, il **IContextNode** appena creato viene aggiunto come ultimo nodo figlio.

Per un elenco dei tipi di nodo di contesto, vedere [tipi di nodo di contesto](context-node-types.md).

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

[**IContextNode::D eleteSubNode**](icontextnode-deletesubnode.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

