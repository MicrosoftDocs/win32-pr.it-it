---
description: Contiene una raccolta di oggetti che implementano l'interfaccia IContextNode e che sono il risultato di un'operazione di analisi dell'input penna.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: Interfaccia IContextNodes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 306abcd32dcb0ee55978a6b95ee9f8a2c22cd19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307411"
---
# <a name="icontextnodes-interface"></a>Interfaccia IContextNodes

Contiene una raccolta di oggetti che implementano l'interfaccia [**IContextNode**](icontextnode.md) e che sono il risultato di un'operazione di analisi dell'input penna.

## <a name="members"></a>Membri

L'interfaccia **IContextNodes** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextNodes** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IContextNodes** dispone di questi metodi.



| Metodo                                                       | Descrizione                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**AddContextNode**](icontextnodes-addcontextnode.md)       | Aggiunge un oggetto [**IContextNode**](icontextnode.md) alla raccolta. <br/>                                  |
| [**Getcontextnode**](icontextnodes-getcontextnode.md)       | Recupera l'oggetto [**IContextNode**](icontextnode.md) in corrispondenza dell'indice specificato all'interno di questa raccolta. <br/> |
| [**GetCount**](icontextnodes-getcount.md)                   | Recupera il numero di oggetti [**IContextNode**](icontextnode.md) contenuti in questa raccolta. <br/>       |
| [**RemoveContextNode**](icontextnodes-removecontextnode.md) | Rimuove un oggetto [**IContextNode**](icontextnode.md) da questa raccolta. <br/>                             |



 

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

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

