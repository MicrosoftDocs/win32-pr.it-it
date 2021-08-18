---
title: Metodo IWMDRMDeviceApp GenerateMeterChallenge (WMDRMDeviceApp.h)
description: Il metodo GenerateMeterChallenge acquisisce i dati di misurazione da un dispositivo.
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- Metodo GenerateMeterChallenge windows Media Device Manager
- Metodo GenerateMeterChallenge windows Media Device Manager, interfaccia IWMDRMDeviceApp
- Interfaccia IWMDRMDeviceApp windows Media Device Manager, metodo GenerateMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.GenerateMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e91ac5049740d360ae0c5f53959b3d952188bfa2a569c58a9e7cf86ae0c22577
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584550"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a>Metodo IWMDRMDeviceApp::GenerateMeterChallenge

Il **metodo GenerateMeterChallenge acquisisce** i dati di misurazione da un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Puntatore a [**un'interfaccia IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) Se l'applicazione passa **NULL,** vengono usate le informazioni di misurazione archiviate nel computer anziché le informazioni di misurazione da un dispositivo connesso.

</dd> <dt>

*bstrMeterCert* \[ Pollici\]
</dt> <dd>

Certificato di misurazione dell'applicazione, come **BSTR.** Si tratta di un certificato firmato ricevuto da Microsoft.

</dd> <dt>

*pbstrMeterURL* \[ Cambio\]
</dt> <dd>

URL a cui devono essere inviati i dati di misurazione. Questa viene allocata da Windows Gestione dispositivi multimediali e deve essere libera dal chiamante usando **SysFreeString.**

</dd> <dt>

*pbstrMeterData* \[ Cambio\]
</dt> <dd>

Dati di misurazione da inviare al servizio di misurazione. Questa viene allocata da Windows Gestione dispositivi multimediali e deve essere libera dal chiamante usando **SysFreeString.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                      | Descrizione                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                             | Il metodo è riuscito.<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | Uno o più argomenti non sono validi.<br/>                               |
| <dl> <dt>**DRM \_ E \_ INVALIDXMLTAG**</dt> </dl>             | Il formato XML non è corretto.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt> </dl>             | Il formato XML non è corretto.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ NOXMLOPENTAG**</dt> </dl>              | Il formato XML non è corretto.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ XMLNOTFOUND**</dt> </dl>               | Impossibile trovare un tag XML obbligatorio.<br/>                                 |
| <dl> <dt>**Errori del dispositivo**</dt> </dl>            | Qualsiasi numero di errori del dispositivo.<br/>                                  |
| <dl> <dt>**Errori del client DRM**</dt> </dl>        | Qualsiasi numero di errori interni del client DRM.<br/>                     |
| <dl> <dt>**DISPOSITIVO NS \_ E \_ NON DISPOSITIVO \_ \_ \_ WMDRM**</dt> </dl> | Il dispositivo specificato non è un Windows compatibile con Media DRM.<br/> |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, l'applicazione deve chiamare [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) per verificare che tutti i componenti DRM del dispositivo siano aggiornati. Questo metodo può essere chiamato solo in un dispositivo che supporta Windows Media DRM 10 per dispositivi portatili.

I dati recuperati *pbstrMeterData* devono essere inviati all'URL specificato da *pbstrMeterURL*. Assicurarsi di codificare con URL i dati recuperati in modo che non siano modificati durante il trasferimento.

Per [altre informazioni, vedere Gestione del contenuto](handling-protected-content-in-the-application.md) protetto nell'applicazione.

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

// Any updates have been performed. Now get the metering information from the device.
CComBSTR meterCert(METERCERT);
CComBSTR URL;
CComBSTR rawdata;
CComBSTR data;
hr = pDRM->GenerateMeterChallenge(pDevice, meterCert, &URL, &rawdata);
if (hr == S_OK)
    ..... Send to URL...
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

[**Interfaccia IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**Interfaccia IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





