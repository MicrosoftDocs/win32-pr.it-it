---
description: Aggiunge un nuovo oggetto IContextLink alla raccolta di collegamenti di contesto dell'oggetto IContextNode.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: Metodo IContextNode::AddContextLink (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 515ade35baed591060e76818d2b3e00a3654a89a9d42dda21d170ee54b2773ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967440"
---
# <a name="icontextnodeaddcontextlink-method"></a>Metodo IContextNode::AddContextLink

Aggiunge un nuovo [**oggetto IContextLink**](icontextlink.md) alla raccolta di collegamenti di contesto dell'oggetto [**IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDestinationNode* \[ Pollici\]
</dt> <dd>

[**IContextNode di destinazione per**](icontextnode.md) il nuovo oggetto [**IContextLink.**](icontextlink.md)

</dd> <dt>

*linkDirection* \[ Pollici\]
</dt> <dd>

Direzione [**dell'oggetto IContextLink**](icontextlink.md) da creare.

</dd> <dt>

*ppContextLinkToAdd* \[ Cambio\]
</dt> <dd>

Puntatore al nuovo [**oggetto IContextLink.**](icontextlink.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppContextLinkToAdd* quando non è più necessario usare il nodo di contesto.

 

Questo [**oggetto IContextNode**](icontextnode.md) è il nodo di origine (vedere [**IContextLink::GetSourceNode)**](icontextlink-getsourcenode.md)per il [**nuovo oggetto IContextLink.**](icontextlink.md)

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

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**IContextNode::D eleteContextLink**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

