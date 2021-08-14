---
title: Proprietà ResourceLocator.MustUnderstandOptions (WSManDisp.h)
description: Ottiene o imposta il valore MustUnderstandOptions per l'oggetto ResourceLocator.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- Proprietà MustUnderstandOptions Windows gestione remota
- Proprietà MustUnderstandOptions Windows, oggetto ResourceLocator
- Oggetto ResourceLocator Windows gestione remota, proprietà MustUnderstandOptions
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a49c3af0372553c221dae902a5fdca0e026bb874f612b8e21f41e6a6870f7ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323739"
---
# <a name="resourcelocatormustunderstandoptions-property"></a>ResourceLocator.MustUnderstandOptions - proprietà

Ottiene o imposta il **valore MustUnderstandOptions** per [**l'oggetto ResourceLocator.**](resourcelocator.md) È possibile fornire un [**oggetto ResourceLocator**](resourcelocator.md) anziché specificare un URI di risorsa nelle operazioni dell'oggetto [**Session,**](session.md) ad esempio [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md)

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a>Valore proprietà

Indica, quando **è True,** che il servizio che implementa il [protocollo WS-Management](ws-management-protocol.md) deve restituire un errore se non è in grado di elaborare l'opzione .

## <a name="remarks"></a>Commenti

**IWSManResourceLocator::MustUnderstandOptions è** la proprietà C++ corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





