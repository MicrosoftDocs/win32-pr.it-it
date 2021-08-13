---
description: Contiene una raccolta di oggetti che implementano l'interfaccia IContextNode e che sono il risultato di un'operazione di analisi dell'input penna.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: Interfaccia IContextNodes (IACom.h)
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
ms.openlocfilehash: 8e1cc15817fa36c8cecaf06c1da0fd8fb7dae77b77909f2e04b5ebaef8100d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119266151"
---
# <a name="icontextnodes-interface"></a>Interfaccia IContextNodes

Contiene una raccolta di oggetti che implementano [**l'interfaccia IContextNode**](icontextnode.md) e che sono il risultato di un'operazione di analisi dell'input penna.

## <a name="members"></a>Membri

**L'interfaccia IContextNodes** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IContextNodes** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IContextNodes.**



| Metodo                                                       | Descrizione                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**AddContextNode**](icontextnodes-addcontextnode.md)       | Aggiunge un [**oggetto IContextNode**](icontextnode.md) a questa raccolta. <br/>                                  |
| [**GetContextNode**](icontextnodes-getcontextnode.md)       | Recupera [**l'oggetto IContextNode**](icontextnode.md) in corrispondenza dell'indice specificato all'interno di questa raccolta. <br/> |
| [**GetCount**](icontextnodes-getcount.md)                   | Recupera il numero di [**oggetti IContextNode**](icontextnode.md) contenuti in questa raccolta. <br/>       |
| [**RemoveContextNode**](icontextnodes-removecontextnode.md) | Rimuove un [**oggetto IContextNode**](icontextnode.md) da questa raccolta. <br/>                             |



 

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

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

