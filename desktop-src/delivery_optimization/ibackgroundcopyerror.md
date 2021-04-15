---
title: Interfaccia IBackgroundCopyError (Deliveryoptimization. h)
description: Utilizzare l'interfaccia IBackgroundCopyError per determinare la provocazione di un errore e se il processo di trasferimento può proseguire.
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
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476372"
---
# <a name="ibackgroundcopyerror-interface"></a>Interfaccia IBackgroundCopyError

Utilizzare l'interfaccia **IBackgroundCopyError** per determinare la provocazione di un errore e se il processo di trasferimento può proseguire.

Viene creato un oggetto Error solo quando lo stato del processo è BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR. Non crea un oggetto Error quando un metodo di interfaccia **IBackgroundCopyXXXX** ha esito negativo. L'oggetto Error è disponibile fino a quando non inizia il trasferimento dei dati (lo stato del processo viene modificato in BG_JOB_STATE_TRANSFERRING) per il processo.

Per ottenere un oggetto **IBackgroundCopyError** , chiamare il metodo [**Metodo ibackgroundcopyjob:: GetError**](ibackgroundcopyjob-geterror.md) .

## <a name="members"></a>Membri

L'interfaccia **IBackgroundCopyError** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyError** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IBackgroundCopyError** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetError**](ibackgroundcopyerror-geterror-method.md) | Recupera il codice di errore e identifica il contesto in cui si è verificato l'errore.<br/> |
| [**GetFile**](ibackgroundcopyerror-getfile-method.md)   | Recupera un puntatore di interfaccia all'oggetto file associato all'errore.<br/>     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError viene definito come 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: GetError**](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

