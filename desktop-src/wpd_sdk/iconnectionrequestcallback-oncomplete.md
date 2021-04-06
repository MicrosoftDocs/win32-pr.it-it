---
description: Notifica a un'applicazione che una richiesta di connessione o disconnessione pianificata in precedenza al dispositivo MTP/Bluetooth è stata completata.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'Metodo IConnectionRequestCallback:: OnComplete (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883166"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>Metodo IConnectionRequestCallback:: OnComplete

Il metodo **OnComplete** notifica a un'applicazione che una richiesta di connessione o disconnessione pianificata in precedenza al dispositivo MTP/Bluetooth è stata completata

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hrStatus* \[ in\]
</dt> <dd>

Stato della richiesta di connessione o disconnessione di un dispositivo specifico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Un'applicazione implementa l'interfaccia [**IConnectionRequestCallback**](iconnectionrequestcallback.md) per ricevere notifiche sulle richieste completate e per annullare richieste in sospeso.

Dispositivi portatili Windows (WPD) chiama questo metodo per notificare a un'applicazione che una richiesta pianificata in precedenza è stata completata. Ogni richiesta può essere rilevata e annullata dal callback fornito dall'applicazione. Pertanto, se l'applicazione deve inviare più richieste contemporaneamente usando lo stesso oggetto [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , a ogni richiesta deve essere passato un oggetto [**IConnectionRequestCallback**](iconnectionrequestcallback.md) univoco come parametro di input ai metodi [**IPortableDeviceConnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) e [**IPortableDeviceConnector::D di connessione**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                                                                             |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                              |
| Intestazione<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>PortableDeviceConnectApi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>PortableDeviceConnectApi. idl</dt> </dl>                                                                |
| Libreria<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IConnectionRequestCallback**](iconnectionrequestcallback.md)
</dt> </dl>

 

 




