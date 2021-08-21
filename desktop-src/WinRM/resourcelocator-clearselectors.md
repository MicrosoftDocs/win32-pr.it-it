---
title: Metodo ResourceLocator.ClearSelectors (WSManDisp.h)
description: Rimuove tutti i selettori da un oggetto ResourceLocator.
ms.assetid: 759880e6-5026-45de-b7e1-a4f5a16c32a0
ms.tgt_platform: multiple
keywords:
- Metodo ClearSelectors Windows Gestione remota
- Metodo ClearSelectors Windows gestione remota, oggetto ResourceLocator
- Oggetto ResourceLocator Windows gestione remota, metodo ClearSelectors
topic_type:
- apiref
api_name:
- ResourceLocator.ClearSelectors
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d54fda16aa67086304e62b4c762769cc7dea832437a939f3928eda665623f5ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112837"
---
# <a name="resourcelocatorclearselectors-method"></a>Metodo ResourceLocator.ClearSelectors

Rimuove tutti i [*selettori da*](windows-remote-management-glossary.md) un [**oggetto ResourceLocator.**](resourcelocator.md) È possibile fornire un [**oggetto ResourceLocator**](resourcelocator.md) anziché specificare un URI di risorsa nelle operazioni dell'oggetto [**Session,**](session.md) ad esempio [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md)

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.ClearSelectors()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="remarks"></a>Commenti

**IWSManResourceLocator::ClearSelectors è** il metodo C++ corrispondente.

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

 

 





