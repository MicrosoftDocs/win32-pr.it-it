---
description: Crea un oggetto IContextNode figlio contenente solo le informazioni sul tipo, l'identificatore e la posizione.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: 'Metodo IContextNode:: CreatePartiallyPopulatedSubNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreatePartiallyPopulatedSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7947ba4665bdb101e955246fcc99352a24a4397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879366"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a>Metodo IContextNode:: CreatePartiallyPopulatedSubNode

Crea un oggetto [**IContextNode**](icontextnode.md) figlio contenente solo le informazioni sul tipo, l'identificatore e la posizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNodeType* \[ in\]
</dt> <dd>

Tipo di nodo di contesto da creare.

</dd> <dt>

*pNodeId* \[ in\]
</dt> <dd>

Identificatore del nuovo nodo.

</dd> <dt>

*pNodeLocation* \[ in\]
</dt> <dd>

Posizione del nuovo nodo.

</dd> <dt>

*pPartiallyPopulatedContextNodeCreated* \[ out\]
</dt> <dd>

Puntatore alla nuova [**IContextNode**](icontextnode.md)popolata parzialmente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *pPartiallyPopulatedContextNodeCreated* quando non è più necessario usare il nodo di contesto.

 

Il nuovo [**IContextNode**](icontextnode.md) viene aggiunto alla raccolta di nodi figlio del nodo di contesto (vedere [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)). Quando sono presenti nodi figlio esistenti, il **IContextNode** appena creato viene aggiunto come ultimo nodo figlio.

Per ulteriori informazioni sul tipo, sull'identificatore e sulla posizione, vedere [**IContextNode:: GetType**](icontextnode-gettype.md), [**IContextNode:: GetId**](icontextnode-getid.md)e [**IContextNode:: getLocation**](icontextnode-getlocation.md).

Questo metodo viene utilizzato per il proxy di dati come un modo per creare un oggetto [**IContextNode**](icontextnode.md) nell'albero del nodo di contesto prima che siano disponibili tutte le informazioni su di esso. Per altre informazioni, vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

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

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Tipi di nodo di contesto](context-node-types.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

