---
description: Sposta i dati del tratto da questo IContextNode al IContextNode specificato.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: 'Metodo IContextNode:: ReparentStrokeByIdToNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ReparentStrokeByIdToNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3984153a0551de999563b8775ceb5acba1696e39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307418"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a>Metodo IContextNode:: ReparentStrokeByIdToNode

Sposta i dati del tratto da questo [**IContextNode**](icontextnode.md) al **IContextNode** specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lStrokeId* \[ in\]
</dt> <dd>

Identificatore del tratto da spostare.

</dd> <dt>

*pContextNodeDestination* \[ in\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) in cui spostare i dati del tratto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

L'oggetto [**IContextNode**](icontextnode.md) specificato deve essere uno dei tipi seguenti dalle costanti dei [tipi di nodo di contesto](context-node-types.md) : **InkWord**, **InkDrawing**, **InkBullet** o **UnclassifiedInk**. Il tentativo di spostare un tratto in un altro tipo di oggetto **IContextNode** restituisce un valore restituito di **E \_ INVALIDARG**.

Questo metodo può essere chiamato da qualsiasi oggetto [**IContextNode**](icontextnode.md) , inclusi oggetti **IContextNode** foglia non input penna. È necessario fare riferimento al tratto specificato da uno dei discendenti di questo oggetto **IContextNode** oppure viene restituito **E \_ INVALIDARG** .

Se il [**IContextNode**](icontextnode.md) o **IContextNode** in *pContextNodeDestination* è confermato, viene restituito **E \_ INVALIDARG** (vedere [**IContextNode:: deconfirmed**](icontextnode-isconfirmed.md)).

L'analizzatore input penna non elimina i nodi di contesto vuoti dall'albero dei risultati in risposta a questo metodo.

-   Un nodo foglia input penna che non fa riferimento a dati di tratto è un nodo vuoto.
-   Un nodo contenitore che non fa riferimento A nodi figlio è un nodo vuoto.

Un nodo vuoto genera errori se si trova nell'albero durante un'operazione di analisi dell'input penna. Per rimuovere un nodo dalla struttura ad albero dell'analizzatore di input penna, chiamare il metodo [**IContextNode::D eletesubnode**](icontextnode-deletesubnode.md) del nodo padre (vedere [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md)).

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

[**IContextNode:: setratti**](icontextnode-setstrokes.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




