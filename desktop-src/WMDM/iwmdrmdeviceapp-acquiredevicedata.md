---
title: Metodo AcquireDeviceData IWMDRMDeviceApp (WMDRMDeviceApp.h)
description: Il metodo AcquireDeviceData inizializza o reimposta un orologio sicuro del dispositivo.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- Metodo AcquireDeviceData windows Media Device Manager
- Metodo AcquireDeviceData windows Media Device Manager, interfaccia IWMDRMDeviceApp
- Interfaccia IWMDRMDeviceApp windows Media Device Manager, metodo AcquireDeviceData
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
ms.openlocfilehash: 9280a358c7124a3f16e3d303026f36506610b6dc6fe0453fdf3e7b2432682719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055645"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a>Metodo IWMDRMDeviceApp::AcquireDeviceData

Il **metodo AcquireDeviceData** inizializza o reimposta un orologio sicuro del dispositivo.

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

*pDevice* \[ Pollici\]
</dt> <dd>

Puntatore a [**un'interfaccia IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) per il dispositivo che segnala i dati di misurazione.

</dd> <dt>

*pProgressCallback* \[ Pollici\]
</dt> <dd>

Callback di stato tramite il quale l'applicazione può tenere traccia dello stato di avanzamento dell'evento o annullare l'evento. Lo stato di avanzamento è identificato *dal parametro EventId* dei [**metodi IWMDMProgress3.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

OR **logico** di uno o entrambi i flag seguenti, che specifica l'azione da eseguire. Questo valore viene recuperato dal *parametro pdwStatus* di [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2::QueryDeviceStatus2.**](iwmdrmdeviceapp2-querydevicestatus2.md) È possibile usare direttamente il flag *pdwStatus.*



| Flag                        | Descrizione                                   |
|-----------------------------|-----------------------------------------------|
| WMDRM \_ DEVICE \_ NEEDCLOCK    | Acquisire un orologio da un server di clock sicuro.   |
| WMDRM \_ DEVICE \_ REFRESHCLOCK | Aggiornare l'orologio da un server di clock protetto. |



 

</dd> <dt>

*pdwStatus* \[ Cambio\]
</dt> <dd>

Uno dei valori **DWORD** seguenti che specifica lo stato restituito dal dispositivo.



| Stato | Descrizione                                                     |
|--------|-----------------------------------------------------------------|
| 0      | L'azione non è supportata.                                    |
| 1      | Non è stato possibile acquisire l'orologio sicuro del dispositivo dal servizio. |
| 2      | Non è stato possibile impostare l'orologio sicuro del dispositivo.                     |
| 3      | È stato impostato l'orologio sicuro del dispositivo.                              |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                                             | Descrizione                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                    | Il metodo è riuscito.<br/>                                                                                                    |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                                       | Uno o più argomenti non sono validi.<br/>                                                                                     |
| <dl> <dt>**DISPOSITIVO NS \_ E \_ NON DISPOSITIVO \_ \_ \_ WMDRM**</dt> </dl>                        | Il dispositivo specificato non è un Windows compatibile con Media DRM.<br/>                                                       |
| <dl> <dt>**NS \_ E \_ DRM \_ UNABLE \_ TO \_ GET \_ SECURE \_ CLOCK**</dt> </dl>               | Non è stato possibile recuperare la richiesta di orologio sicuro dal dispositivo o non è stato possibile recuperare l'URL dell'orologio protetto dalla richiesta.<br/> |
| <dl> <dt>**NS \_ E \_ DRM \_ UNABLE \_ TO \_ GET \_ SECURE \_ CLOCK \_ FROM \_ SERVER**</dt> </dl> | Impossibile recuperare la risposta dell'orologio protetto dal server di clock protetto.<br/>                                               |
| <dl> <dt>**NS \_ E \_ DRM \_ UNABLE \_ TO \_ SET \_ SECURE \_ CLOCK**</dt> </dl>               | Non è stato possibile inviare la richiesta di orologio sicuro al dispositivo o il dispositivo non è riuscito a impostare l'orologio.<br/>                          |



 

## <a name="remarks"></a>Commenti

Si tratta di un metodo asincrono. il dispositivo deve attendere il callback [**IWMDMProgress::End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) per questa operazione prima di provare a riprodurre contenuto concesso in licenza.

Un'applicazione può scoprire se il dispositivo deve essere reimpostato o aggiornato chiamando [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2::QueryDeviceStatus2.**](iwmdrmdeviceapp2-querydevicestatus2.md)

L'applicazione deve disporre di una connessione Internet per consentire l'acquisizione o la reimpostazione di un orologio protetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDRMDeviceApp.h (richiede anche Wmdrmdeviceapp \_ i.c, compilato da WMDRMDeviceApp.idl)</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



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

 

 





