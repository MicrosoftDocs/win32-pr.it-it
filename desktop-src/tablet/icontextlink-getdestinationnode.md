---
description: Recupera l'oggetto IContextNode che rappresenta la destinazione per questo IContextLink.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'Metodo IContextLink:: GetDestinationNode (IACom. h)'
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
ms.openlocfilehash: 86d34bfcca39f7df9d9010e8dae32747ca8f1d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343726"
---
# <a name="icontextlinkgetdestinationnode-method"></a>Metodo IContextLink:: GetDestinationNode

Recupera l'oggetto [**IContextNode**](icontextnode.md) che rappresenta la destinazione per questo [**IContextLink**](icontextlink.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDstContextNodeId* \[ out\]
</dt> <dd>

Puntatore all'oggetto [**IContextNode**](icontextnode.md) che rappresenta la destinazione per questo [**IContextLink**](icontextlink.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppDstContextNodeId* quando non è più necessario usare il nodo di destinazione.

 

Se l'oggetto [**IContextLink**](icontextlink.md) è collegato tra un nodo che contiene la scrittura e un nodo che contiene il disegno, il nodo di destinazione è in genere il nodo che contiene la scrittura.

Se l'oggetto [**IContextLink**](icontextlink.md) dispone di un tipo di collegamento di racchiude (vedere [**IContextLink:: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), il nodo di destinazione è l'oggetto [**IContextNode**](icontextnode.md) che è incluso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

