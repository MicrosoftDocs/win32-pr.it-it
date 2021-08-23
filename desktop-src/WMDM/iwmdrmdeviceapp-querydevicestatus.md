---
title: Metodo QueryDeviceStatus IWMDRMDeviceApp (WMDRMDeviceApp.h)
description: Il metodo QueryDeviceStatus esegue una query su un dispositivo per verificare lo stato e le funzionalità DRM correnti.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Metodo QueryDeviceStatus windows Media Device Manager
- Metodo QueryDeviceStatus windows Media Device Manager , interfaccia IWMDRMDeviceApp
- Interfaccia IWMDRMDeviceApp windows Media Device Manager, metodo QueryDeviceStatus
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.QueryDeviceStatus
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b169412104a5e22ae973542457d08bead328ea4ded5a34691499ea8dbfd8b7b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055644"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a>Metodo IWMDRMDeviceApp::QueryDeviceStatus

Il **metodo QueryDeviceStatus** esegue una query su un dispositivo per verificare lo stato e le funzionalità DRM correnti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Puntatore a [**un oggetto IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)

</dd> <dt>

*pdwStatus* \[ Cambio\]
</dt> <dd>

Zero o più dei valori **DWORD seguenti** che descrivono gli aspetti DRM del dispositivo, combinati con or bit per **bit.** Vedere la sezione Osservazioni.



| Stato                      | Descrizione                                  |
|-----------------------------|----------------------------------------------|
| DISPOSITIVO WMDRM \_ \_ ISWMDRM      | Il dispositivo supporta Windows DRM multimediale.       |
| DISPOSITIVO WMDRM \_ \_ NEEDCLOCK    | Il dispositivo non ha un orologio sicuro.     |
| DISPOSITIVO WMDRM \_ \_ REVOCATO      | Il dispositivo è stato revocato.                 |
| WMDRM \_ CLIENT \_ NEEDINDIV    | La sicurezza DRM deve essere individualizzata. |
| AGGIORNAMENTO DEL \_ DISPOSITIVO WMDRMCLOCK \_ | L'orologio deve essere aggiornato.             |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                              | Descrizione                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                     | Il metodo è riuscito.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | L'argomento di input non è valido.<br/>                               |
| <dl> <dt>**CERTIFICATO \_ NS E \_ DRM \_ NON \_ VALIDO**</dt> </dl>          | Il certificato del dispositivo recuperato dal dispositivo non è valido.<br/> |
| <dl> <dt>**NS \_ E \_ \_ DRM: IMPOSSIBILE OTTENERE IL CERTIFICATO DEL \_ \_ \_ \_ DISPOSITIVO**</dt> </dl> | Impossibile recuperare il certificato del dispositivo dal dispositivo.<br/>     |



 

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato prima di eseguire azioni limitate sul contenuto DRM, ad esempio il trasferimento del contenuto DRM nel dispositivo o l'acquisizione di informazioni di misurazione. Se i valori recuperati da *pdwStatus* indicano che è necessario eseguire alcune azioni, ad esempio l'individualizzazione per il desktop o l'acquisizione di un clock per il dispositivo, l'applicazione deve chiamare [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passare il valore *pdwStatus* recuperato da questa funzione al *parametro dwFlags* in **AcquireDeviceData.** Se viene restituito zero, il dispositivo non supporta Windows Media DRM 10 per dispositivi portatili e non è necessario eseguire alcuna azione. Per [altre informazioni, vedere Gestione del contenuto](handling-protected-content-in-the-application.md) protetto nell'applicazione.

## <a name="examples"></a>Esempio

L'esempio di codice C++ seguente crea un oggetto **WMDRMDeviceApp,** verifica che il dispositivo sia un dispositivo Windows Media DRM 10, che l'orologio sia accurato e quindi richiede i dati di misurazione.


```C++
HRESULT hr = S_OK;
// Create the WMDRMDeviceApp object.
CComPtr<IWMDRMDeviceApp> pDRM;
hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

// Find out first if the device is a WMDRM 10 device, and if it requires
// any clock updates.
DWORD status = 0;
hr = pDRM->QueryDeviceStatus(pDevice, &status);

if (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. Nothing can be updated,
    return E_FAIL;                   // and metering cannot be performed.
else if (status & WMDRM_DEVICE_REVOKED) // Device is revoked.
    return E_FAIL;
else if (status & WMDRM_DEVICE_NEEDCLOCK || 
    status & WMDRM_CLIENT_NEEDINDIV ||
    status & WMDRM_DEVICE_REFRESHCLOCK)
{
    // Need to update device clock. 
    // Using custom function, which is synchronous.
    hr = myAcquireDeviceData(pDRM, pDevice, this, status, &result);
    if (hr != S_OK || result != 0)    // Couldn't perform the updates.
        return E_FAIL;    
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDRMDeviceApp.h (richiede anche Wmdrmdeviceapp \_ i.c, compilato da WMDRMDeviceApp.idl)</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Gestione del contenuto protetto nell'applicazione**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaccia IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





