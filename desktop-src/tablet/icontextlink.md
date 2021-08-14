---
description: Rappresenta una relazione tra due oggetti IContextNode.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: Interfaccia IContextLink (IACom.h)
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
ms.openlocfilehash: 7dc9244fed59604a56817f15801de94b64c476762e186cc6f7c36186e8d0b26d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719915"
---
# <a name="icontextlink-interface"></a>Interfaccia IContextLink

Rappresenta una relazione tra due [**oggetti IContextNode.**](icontextnode.md)

## <a name="members"></a>Membri

**L'interfaccia IContextLink** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IContextLink** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IContextLink** include questi metodi.



| Metodo                                                                  | Descrizione                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md) | Recupera il tipo di relazione rappresentato da **IContextLink.**<br/>                                         |
| [**GetDestinationNode**](icontextlink-getdestinationnode.md)           | Recupera [**l'oggetto IContextNode**](icontextnode.md) che rappresenta la destinazione per **questo oggetto IContextLink.**<br/> |
| [**GetSourceNode**](icontextlink-getsourcenode.md)                     | Recupera [**l'oggetto IContextNode**](icontextnode.md) che rappresenta l'origine per **questo oggetto IContextLink.**<br/>      |



 

## <a name="remarks"></a>Commenti

Di seguito è riportato un esempio di relazione rappresentata da un **oggetto IContextLink:**

-   Quando un nodo AnalysisHint viene usato nell'analisi dell'input penna, l'operazione di analisi dell'input penna crea un oggetto **IContextLink** di tipo AnalysisHint tra il nodo hint di analisi e il nodo che contiene la scrittura all'interno dell'area dell'hint. Il nodo di origine è il nodo hint di analisi e il nodo di destinazione è il nodo che contiene la scrittura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
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

 

