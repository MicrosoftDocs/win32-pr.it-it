---
description: Sposta i dati del tratto da questo oggetto IContextNode all'oggetto IContextNode specificato.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: Metodo IContextNode::ReparentStrokeByIdToNode (IACom.h)
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
ms.openlocfilehash: a915425900bccb15145546658d51d50dcaee14880f8f219bd1908efaa17bd3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008411"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a>Metodo IContextNode::ReparentStrokeByIdToNode

Sposta i dati del tratto [**da questo oggetto IContextNode**](icontextnode.md) all'oggetto **IContextNode specificato.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lStrokeId* \[ Pollici\]
</dt> <dd>

Identificatore del tratto da spostare.

</dd> <dt>

*pContextNodeDestination* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) in cui spostare i dati del tratto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

[**L'oggetto IContextNode**](icontextnode.md) specificato deve essere uno dei tipi seguenti delle costanti Context [Node Types:](context-node-types.md) **InkWord,** **InkDrawing,** **InkBullet** o **UnclassifiedInk.** Il tentativo di spostare un tratto in qualsiasi altro tipo di **oggetto IContextNode** comporta un valore restituito **E \_ INVALIDARG**.

Questo metodo può essere chiamato da qualsiasi [**oggetto IContextNode,**](icontextnode.md) inclusi gli oggetti **IContextNode** foglia non input penna. Il tratto specificato deve fare riferimento a uno dei discendenti di questo **oggetto IContextNode** oppure viene restituito **E \_ INVALIDARG.**

Se viene confermato [**questo IContextNode**](icontextnode.md) o **IContextNode** in *pContextNodeDestination,* viene restituito **E \_ INVALIDARG** (vedere [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)).

L'analizzatore input penna non elimina nodi di contesto vuoti dall'albero dei risultati in risposta a questo metodo.

-   Un nodo foglia di input penna che non fa riferimento ai dati del tratto è un nodo vuoto.
-   Un nodo contenitore che non fa riferimento ad alcun nodo figlio è un nodo vuoto.

Un nodo vuoto genera errori se si trova nell'albero durante un'operazione di analisi dell'input penna. Per rimuovere un nodo dall'albero dell'analizzatore input penna, chiamare il metodo [**IContextNode::D eleteSubNode**](icontextnode-deletesubnode.md) del nodo padre (vedere [**IContextNode::GetParentNode).**](icontextnode-getparentnode.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::SetStrokes**](icontextnode-setstrokes.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




