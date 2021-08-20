---
title: Metodo ResourceLocator.ClearOptions (WSManDisp.h)
description: Rimuove tutte le opzioni dall'oggetto ResourceLocator.
ms.assetid: 1b4d7f15-c56f-4b0d-9614-8376012abca7
ms.tgt_platform: multiple
keywords:
- Metodo ClearOptions Windows Gestione remota
- Metodo ClearOptions Windows gestione remota, oggetto ResourceLocator
- Oggetto ResourceLocator Windows gestione remota, metodo ClearOptions
topic_type:
- apiref
api_name:
- ResourceLocator.ClearOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef695b949c62c0d56de45914e1a54996d4d7599f029d136ad78b03ac687365aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112912"
---
# <a name="resourcelocatorclearoptions-method"></a>Metodo ResourceLocator.ClearOptions

Rimuove tutte [*le opzioni*](windows-remote-management-glossary.md) [**dall'oggetto ResourceLocator.**](resourcelocator.md) È possibile fornire un [**oggetto ResourceLocator**](resourcelocator.md) anziché specificare un URI di risorsa nelle operazioni dell'oggetto [**Session,**](session.md) ad esempio [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md)

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.ClearOptions()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="remarks"></a>Commenti

**IWSManResourceLocator::ClearOptions** è il metodo C++ corrispondente.

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

 

 





