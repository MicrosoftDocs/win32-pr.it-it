---
title: Interfaccia IBackgroundCopyError (Deliveryoptimization.h)
description: Usare l'interfaccia IBackgroundCopyError per determinare la causa di un errore e se il processo di trasferimento può continuare.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- Interfaccia IBackgroundCopyError
- Interfaccia IBackgroundCopyError, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73e4dd3a74529bb95d1e80597579d6a0aa5885302b9b26d851dc341c9cd1a9a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101653"
---
# <a name="ibackgroundcopyerror-interface"></a>Interfaccia IBackgroundCopyError

Usare **l'interfaccia IBackgroundCopyError** per determinare la causa di un errore e se il processo di trasferimento può continuare.

DO crea un oggetto errore solo quando lo stato del processo è BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR. DO non crea un oggetto errore quando un metodo di interfaccia **IBackgroundCopyXXXX** ha esito negativo. L'oggetto errore è disponibile fino a quando DO non inizia a trasferire i dati (lo stato del processo cambia in BG_JOB_STATE_TRANSFERRING) per il processo.

Per ottenere un **oggetto IBackgroundCopyError,** chiamare il [**metodo IBackgroundCopyJob::GetError.**](ibackgroundcopyjob-geterror.md)

## <a name="members"></a>Membri

**L'interfaccia IBackgroundCopyError** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyError** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IBackgroundCopyError.**



| Metodo                                                   | Descrizione                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetError**](ibackgroundcopyerror-geterror-method.md) | Recupera il codice di errore e identifica il contesto in cui si è verificato l'errore.<br/> |
| [**GetFile**](ibackgroundcopyerror-getfile-method.md)   | Recupera un puntatore a interfaccia all'oggetto file associato all'errore.<br/>     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError è definito come 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetError**](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

