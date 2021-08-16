---
description: Notifica a un'applicazione che una richiesta di Connessione o di disconnessione pianificata in precedenza al dispositivo MTP/Bluetooth è stata completata.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: Metodo IConnectionRequestCallback::OnComplete (Devpkey.h)
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
ms.openlocfilehash: b21248cde95d4b58accb7e629efedfc7c05eef7b08f411e240314a6a07690b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843189"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>Metodo IConnectionRequestCallback::OnComplete

Il **metodo OnComplete** notifica a un'applicazione che una richiesta di connessione Connessione o disconnessione pianificata in precedenza al dispositivo MTP/Bluetooth è stata completata

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hrStatus* \[ Pollici\]
</dt> <dd>

Stato della richiesta di connessione o disconnessione di un determinato dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Un'applicazione implementa [**l'interfaccia IConnectionRequestCallback**](iconnectionrequestcallback.md) per ricevere notifiche sulle richieste completate e annullare le richieste in sospeso.

Windows Dispositivi portabili (WPD) chiama questo metodo per notificare a un'applicazione che una richiesta pianificata in precedenza è stata completata. Ogni richiesta può essere rilevata e annullata dal callback fornito dall'applicazione. Pertanto, se l'applicazione deve inviare più richieste contemporaneamente usando lo stesso oggetto [**IPortableDeviceConnector,**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) a ogni richiesta deve essere passato un oggetto [**IConnectionRequestCallback**](iconnectionrequestcallback.md) univoco come parametro di input ai metodi [**IPortableDeviceConnector::Connessione**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) e [**IPortableDeviceConnector::D isconnect.**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                                                                             |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                              |
| Intestazione<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Libreria<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IConnectionRequestCallback**](iconnectionrequestcallback.md)
</dt> </dl>

 

 




