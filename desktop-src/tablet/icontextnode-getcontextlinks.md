---
description: Recupera una raccolta di oggetti IContextLink che rappresenta relazioni con altri oggetti IContextNode.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: 'Metodo IContextNode:: GetContextLinks (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de62550a09d0a538ddc680f6d57c35a1016fe255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307439"
---
# <a name="icontextnodegetcontextlinks-method"></a>Metodo IContextNode:: GetContextLinks

Recupera una raccolta di oggetti [**IContextLink**](icontextlink.md) che rappresenta relazioni con altri oggetti [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppContextLinks* \[ out\]
</dt> <dd>

Puntatore a una raccolta di oggetti [**IContextLink**](icontextlink.md) che rappresenta relazioni con altri oggetti [**IContextNode**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppContextLinks* quando non è più necessario usare la raccolta di collegamenti di contesto.

 

Per ottenere informazioni sulle relazioni del nodo padre o figlio, utilizzare [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) o [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md).

Per ulteriori informazioni sui tipi di relazioni descritti dai collegamenti, vedere [**IContextLink**](icontextlink.md) e [**ContextLinkDirection**](contextlinkdirection.md).

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

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

