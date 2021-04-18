---
title: Metodo IWMDRMDeviceApp QueryDeviceStatus (WMDRMDeviceApp. h)
description: Il metodo QueryDeviceStatus esegue una query su un dispositivo per lo stato e le funzionalità DRM correnti.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Metodo QueryDeviceStatus Windows Media Gestione dispositivi
- Metodo QueryDeviceStatus Windows Media Gestione dispositivi, interfaccia IWMDRMDeviceApp
- Interfaccia IWMDRMDeviceApp Windows Media Gestione dispositivi, metodo QueryDeviceStatus
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
ms.openlocfilehash: b8e0f4fad5ff9026ce70fc21712506eb4796d76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327877"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a>Metodo IWMDRMDeviceApp:: QueryDeviceStatus

Il metodo **QueryDeviceStatus** esegue una query su un dispositivo per lo stato e le funzionalità DRM correnti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Puntatore a un oggetto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*pdwStatus* \[ out\]
</dt> <dd>

Zero o più dei seguenti valori **DWORD** che descrivono gli aspetti DRM del dispositivo, combinati con un **or** bit per bit. Vedere la sezione Osservazioni.



| Stato                      | Descrizione                                  |
|-----------------------------|----------------------------------------------|
| \_ISWMDRM del dispositivo WMDRM \_      | Il dispositivo supporta Windows Media DRM.       |
| \_NEEDCLOCK del dispositivo WMDRM \_    | Il dispositivo non ha un clock protetto.     |
| il dispositivo WMDRM è stato \_ \_ revocato      | Il dispositivo è stato revocato.                 |
| \_NEEDINDIV client \_ WMDRM    | La protezione DRM deve essere individualizzata. |
| \_REFRESHCLOCK del dispositivo WMDRM \_ | È necessario aggiornare il clock.             |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                              | Descrizione                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                     | Il metodo è riuscito.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | L'argomento di input non è valido.<br/>                               |
| <dl> <dt>**\_ \_ \_ certificato non valido per NS E DRM \_**</dt> </dl>          | Il certificato del dispositivo recuperato dal dispositivo non è valido.<br/> |
| <dl> <dt>**NS \_ E \_ DRM \_ non riescono \_ a \_ ottenere il \_ certificato del dispositivo \_**</dt> </dl> | Non è stato possibile recuperare il certificato del dispositivo dal dispositivo.<br/>     |



 

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato prima di eseguire qualsiasi azione limitata sul contenuto DRM, ad esempio il trasferimento di contenuto DRM al dispositivo o l'acquisizione di informazioni di misurazione. Se i valori recuperati da *pdwStatus* indicano che è necessario eseguire un'azione, ad esempio l'individualizzazione per il desktop o l'acquisizione di un clock per il dispositivo, l'applicazione deve chiamare [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passare il valore *pdwStatus* recuperato da questa funzione al parametro *dwFlags* in **AcquireDeviceData**. Se viene restituito zero, il dispositivo non supporta Windows Media DRM 10 per i dispositivi portatili e non è necessario eseguire alcuna azione. Per ulteriori informazioni, vedere [gestione del contenuto protetto nell'applicazione](handling-protected-content-in-the-application.md) .

## <a name="examples"></a>Esempio

Nell'esempio di codice C++ riportato di seguito viene creato un oggetto **WMDRMDeviceApp** , verifica che il dispositivo sia un dispositivo Windows Media DRM 10, che l'orologio sia accurato e quindi richiede i dati di misurazione.


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
| Intestazione<br/>  | <dl> <dt>WMDRMDeviceApp. h (richiede anche Wmdrmdeviceapp \_ i. c, compilato da WMDRMDeviceApp. idl)</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Gestione del contenuto protetto nell'applicazione**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaccia IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





