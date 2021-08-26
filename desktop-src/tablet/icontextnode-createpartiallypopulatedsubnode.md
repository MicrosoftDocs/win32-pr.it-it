---
description: Crea un oggetto IContextNode figlio che contiene solo informazioni su tipo, identificatore e posizione.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: Metodo IContextNode::CreatePartiallyPopulatedSubNode (IACom.h)
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
ms.openlocfilehash: 7233c6e0303f0634c71a67fde13f237feb2b2f6c6518dd8edc0b1624b4e2b6b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940291"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a>Metodo IContextNode::CreatePartiallyPopulatedSubNode

Crea un oggetto [**IContextNode**](icontextnode.md) figlio che contiene solo informazioni su tipo, identificatore e posizione.

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

*pNodeType* \[ Pollici\]
</dt> <dd>

Tipo di nodo di contesto da creare.

</dd> <dt>

*pNodeId* \[ Pollici\]
</dt> <dd>

Identificatore per il nuovo nodo.

</dd> <dt>

*pNodeLocation* \[ Pollici\]
</dt> <dd>

Posizione del nuovo nodo.

</dd> <dt>

*pPartiallyPopulatedContextNodeCreated* \[ Cambio\]
</dt> <dd>

Puntatore al nuovo [**IContextNode parzialmente popolato.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* *in pPartiallyPopulatedContextNodeCreated* quando non è più necessario usare il nodo di contesto.

 

Il nuovo [**IContextNode**](icontextnode.md) viene aggiunto alla raccolta di nodi figlio di questo nodo di contesto (vedere [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md) Quando sono presenti nodi figlio esistenti, **l'oggetto IContextNode** appena creato viene aggiunto come ultimo nodo figlio.

Per altre informazioni su tipo, identificatore e percorso, vedere [**IContextNode::GetType**](icontextnode-gettype.md), [**IContextNode::GetId**](icontextnode-getid.md)e [**IContextNode::GetLocation**](icontextnode-getlocation.md).

Questo metodo viene usato per il proxy dati come modo per creare un [**oggetto IContextNode**](icontextnode.md) nell'albero del nodo di contesto prima che tutte le informazioni su di esso sono disponibili. Per altre informazioni, vedere [Proxy di dati con l'analisi dell'input penna](data-proxy-with-ink-analysis.md).

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

[**Area IAnalysis**](ianalysisregion.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Tipi di nodo di contesto](context-node-types.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

