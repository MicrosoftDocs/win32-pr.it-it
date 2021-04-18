---
description: Elimina un oggetto IContextLink dalla raccolta di collegamenti dell'oggetto IContextNode.
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: Metodo IContextNode::D eleteContextLink (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac5676635bec961129078ed8689169d1a81cd87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307441"
---
# <a name="icontextnodedeletecontextlink-method"></a>IContextNode::D Metodo eleteContextLink

Elimina un oggetto [**IContextLink**](icontextlink.md) dalla raccolta di collegamenti dell'oggetto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContextLinkToDelete* \[ in\]
</dt> <dd>

Oggetto [**IContextLink**](icontextlink.md) da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Un collegamento di contesto ha un nodo di origine e un nodo di destinazione (vedere [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md) e [**IContextLink:: GetDestinationNode**](icontextlink-getdestinationnode.md)). Questo metodo rimuove il [**IContextLink**](icontextlink.md) dalla raccolta di collegamenti di contesto di entrambi i nodi di origine e di destinazione (vedere [**IContextNode:: GetContextLinks**](icontextnode-getcontextlinks.md)).

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

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




