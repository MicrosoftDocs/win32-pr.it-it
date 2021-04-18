---
description: Rappresenta una relazione tra due oggetti IContextNode.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: Interfaccia IContextLink (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df1e0d8717ba29532486277aced19f17adb1d79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307448"
---
# <a name="icontextlink-interface"></a>Interfaccia IContextLink

Rappresenta una relazione tra due oggetti [**IContextNode**](icontextnode.md) .

## <a name="members"></a>Membri

L'interfaccia **IContextLink** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextLink** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IContextLink** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md) | Recupera il tipo di relazione rappresentata da questo **IContextLink** .<br/>                                         |
| [**GetDestinationNode**](icontextlink-getdestinationnode.md)           | Recupera l'oggetto [**IContextNode**](icontextnode.md) che rappresenta la destinazione per questo **IContextLink**.<br/> |
| [**GetSourceNode**](icontextlink-getsourcenode.md)                     | Recupera l'oggetto [**IContextNode**](icontextnode.md) che rappresenta l'origine per questo **IContextLink**.<br/>      |



 

## <a name="remarks"></a>Commenti

Di seguito è riportato un esempio di una relazione rappresentata da un oggetto **IContextLink** :

-   Quando si usa un nodo AnalysisHint nell'analisi dell'input penna, l'operazione di analisi dell'input penna crea un oggetto **IContextLink** di tipo AnalysisHint tra il nodo hint di analisi e il nodo che contiene la scrittura all'interno dell'area dell'hint. Il nodo di origine è il nodo hint di analisi e il nodo di destinazione è il nodo che contiene la scrittura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Tipi di nodo di contesto](context-node-types.md)
</dt> </dl>

 

