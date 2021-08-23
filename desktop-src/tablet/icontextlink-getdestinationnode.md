---
description: Recupera l'oggetto IContextNode che rappresenta la destinazione per questo IContextLink.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: Metodo IContextLink::GetDestinationNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1a11d9021d4299a1823fee57ed9a80237b4896459b0396a8ba4b140bd377bb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967455"
---
# <a name="icontextlinkgetdestinationnode-method"></a>Metodo IContextLink::GetDestinationNode

Recupera [**l'oggetto IContextNode**](icontextnode.md) che rappresenta la destinazione per [**questo oggetto IContextLink.**](icontextlink.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDstContextNodeId* \[ Cambio\]
</dt> <dd>

Puntatore [**all'oggetto IContextNode**](icontextnode.md) che rappresenta la destinazione per [**questo oggetto IContextLink.**](icontextlink.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppDstContextNodeId* quando non è più necessario usare il nodo di destinazione.

 

Se [**l'oggetto IContextLink**](icontextlink.md) si collega tra un nodo che contiene la scrittura e un nodo che contiene il disegno, il nodo di destinazione è in genere il nodo che contiene la scrittura.

Se [**l'oggetto IContextLink**](icontextlink.md) ha un tipo di collegamento Encloses (vedere [**IContextLink::GetContextLinkDirection),**](icontextlink-getcontextlinkdirection.md)il nodo di destinazione è l'oggetto [**IContextNode**](icontextnode.md) incluso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

