---
description: Contiene una raccolta di oggetti che implementano l'interfaccia IContextLink.
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: Interfaccia IContextLinks (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 44eb7117fe3b01b3e31829222c6ab3f601d5bbbec8ea0591a9f80d087dcaee22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008481"
---
# <a name="icontextlinks-interface"></a>Interfaccia IContextLinks

Contiene una raccolta di oggetti che implementano [**l'interfaccia IContextLink.**](icontextlink.md)

## <a name="members"></a>Membri

**L'interfaccia IContextLinks** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IContextLinks** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IContextLinks** include questi metodi.



| Metodo                                                 | Descrizione                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**GetContextLink**](icontextlinks-getcontextlink.md) | Recupera L'oggetto [**IContextLink in**](icontextlink.md) corrispondenza dell'indice specificato.<br/>               |
| [**GetCount**](icontextlinks-getcount.md)             | Recupera il numero di [**oggetti IContextLink**](icontextlink.md) in questa raccolta.<br/> |



 

## <a name="remarks"></a>Commenti

L'accesso viene in genere eseguito [**tramite il metodo IContextNode::GetContextLinks.**](icontextnode-getcontextlinks.md)

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

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[**IContextNode::D eleteContextLink**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

