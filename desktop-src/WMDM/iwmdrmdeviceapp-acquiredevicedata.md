---
title: Metodo IWMDRMDeviceApp AcquireDeviceData (WMDRMDeviceApp. h)
description: Il metodo AcquireDeviceData Inizializza o reimposta un clock sicuro del dispositivo.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- Metodo AcquireDeviceData Windows Media Gestione dispositivi
- Metodo AcquireDeviceData Windows Media Gestione dispositivi, interfaccia IWMDRMDeviceApp
- Interfaccia IWMDRMDeviceApp Windows Media Gestione dispositivi, metodo AcquireDeviceData
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.AcquireDeviceData
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268572e5dad3dffd0fe15956a0ff145f277fb6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327880"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a>Metodo IWMDRMDeviceApp:: AcquireDeviceData

Il metodo **AcquireDeviceData** Inizializza o reimposta un clock sicuro del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AcquireDeviceData(
  [in]  IWMDMDevice    *pDevice,
  [in]  IWMDMProgress3 *pProgressCallback,
  [in]  DWORD          dwFlags,
  [out] DWORD          *pdwStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Puntatore a un'interfaccia [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) per il dispositivo che segnalerà i dati di misurazione.

</dd> <dt>

*pProgressCallback* \[ in\]
</dt> <dd>

Callback di stato tramite il quale l'applicazione può tenere traccia dello stato di avanzamento dell'evento o annullare l'evento. Lo stato di avanzamento è identificato dal parametro *eventId* dei metodi [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Un **or** logico di uno o entrambi i flag seguenti, che specifica l'azione da eseguire. Questo valore viene recuperato dal parametro *pdwStatus* di [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md). È possibile utilizzare direttamente il flag *pdwStatus* .



| Flag                        | Descrizione                                   |
|-----------------------------|-----------------------------------------------|
| \_NEEDCLOCK del dispositivo WMDRM \_    | Acquisire un clock da un server di clock protetto.   |
| \_REFRESHCLOCK del dispositivo WMDRM \_ | Aggiornare l'orologio da un server di clock protetto. |



 

</dd> <dt>

*pdwStatus* \[ out\]
</dt> <dd>

Uno dei seguenti valori **DWORD** che specifica lo stato restituito dal dispositivo.



| Stato | Descrizione                                                     |
|--------|-----------------------------------------------------------------|
| 0      | L'azione non è supportata.                                    |
| 1      | Non è stato possibile acquisire il clock sicuro del dispositivo dal servizio. |
| 2      | Non è stato possibile impostare il clock sicuro del dispositivo.                     |
| 3      | È stato impostato il clock sicuro del dispositivo.                              |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                                             | Descrizione                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                                    | Il metodo è riuscito.<br/>                                                                                                    |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                                       | Uno o più argomenti non sono validi.<br/>                                                                                     |
| <dl> <dt>**dispositivo NS \_ E \_ dispositivo \_ non \_ WMDRM \_**</dt> </dl>                        | Il dispositivo specificato non è un dispositivo compatibile con Windows Media DRM.<br/>                                                       |
| <dl> <dt>**NS \_ E \_ DRM \_ non riescono \_ a \_ ottenere il \_ \_ Clock sicuro**</dt> </dl>               | Non è stato possibile recuperare la richiesta del clock protetto dal dispositivo o non è possibile recuperare l'URL del clock protetto dalla richiesta di verifica.<br/> |
| <dl> <dt>**NS \_ E \_ DRM \_ non riescono \_ a \_ ottenere il \_ \_ Clock protetto \_ dal \_ Server**</dt> </dl> | Non è stato possibile recuperare la risposta del clock protetto dal server di clock protetto.<br/>                                               |
| <dl> <dt>**NS \_ E \_ DRM \_ non \_ possono \_ impostare \_ il \_ Clock sicuro**</dt> </dl>               | Non è stato possibile inviare la richiesta di clock sicura al dispositivo o il dispositivo non è riuscito a impostare l'orologio.<br/>                          |



 

## <a name="remarks"></a>Commenti

Si tratta di un metodo asincrono. il dispositivo deve attendere il callback [**IWMDMProgress:: end**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) per questa operazione prima di provare a riprodurre eventuali contenuti con licenza.

Un'applicazione può apprendere se il dispositivo deve essere reimpostato o aggiornato chiamando [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).

L'applicazione deve disporre di una connessione Internet per consentire all'utente di acquisire o reimpostare un clock protetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDRMDeviceApp. h (richiede anche Wmdrmdeviceapp \_ i. c, compilato da WMDRMDeviceApp. idl)</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Gestione del contenuto protetto nell'applicazione**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaccia IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**Interfaccia IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**Interfaccia IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





