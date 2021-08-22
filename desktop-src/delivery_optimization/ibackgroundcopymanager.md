---
title: Interfaccia IBackgroundCopyManager (Deliveryoptimization.h)
description: Crea processi di trasferimento, recupera un oggetto enumeratore che contiene i processi nella coda e recupera singoli processi dalla coda.
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- Interfaccia IBackgroundCopyManager
- Interfaccia IBackgroundCopyManager, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cf1ca14443823a5448a63c04d19d00957d4064353183d79aa7762f729115301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542153"
---
# <a name="ibackgroundcopymanager-interface"></a>Interfaccia IBackgroundCopyManager

Crea processi di trasferimento, recupera un oggetto enumeratore che contiene i processi nella coda e recupera singoli processi dalla coda.

## <a name="members"></a>Membri

**L'interfaccia IBackgroundCopyManager** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyManager** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IBackgroundCopyManager** include questi metodi.



| Metodo                                                | Descrizione                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [**CreateJob**](ibackgroundcopymanager-createjob.md) | Crea un processo di trasferimento.<br/>                   |
| [**GetJob**](ibackgroundcopymanager-getjob.md)       | Recupera un processo specificato dalla coda.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager è definito come 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

