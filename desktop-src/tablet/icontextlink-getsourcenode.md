---
description: Recupera l'oggetto IContextNode che rappresenta l'origine per questo IContextLink.
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: Metodo IContextLink::GetSourceNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 609f3012608586f7e6c3279cd0dab4232f58ca3e0e31145124622e87684e06f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940411"
---
# <a name="icontextlinkgetsourcenode-method"></a>Metodo IContextLink::GetSourceNode

Recupera [**l'oggetto IContextNode**](icontextnode.md) che rappresenta l'origine per [**questo oggetto IContextLink.**](icontextlink.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppSrcContextNodeId* \[ Cambio\]
</dt> <dd>

Puntatore [**all'oggetto IContextNode**](icontextnode.md) che rappresenta l'origine per [**questo oggetto IContextLink.**](icontextlink.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppSrcContextNodeId* quando non è più necessario usare il nodo di origine.

 

Se [**l'oggetto IContextLink**](icontextlink.md) si collega tra un nodo che contiene la scrittura e un nodo che contiene il disegno, il nodo di origine è in genere il nodo che contiene il disegno.

Se [**l'oggetto IContextLink**](icontextlink.md) ha un tipo di collegamento Encloses (vedere [**IContextLink::GetContextLinkDirection),**](icontextlink-getcontextlinkdirection.md)il nodo di origine è il nodo che racchiude il nodo di destinazione.

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

[**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

