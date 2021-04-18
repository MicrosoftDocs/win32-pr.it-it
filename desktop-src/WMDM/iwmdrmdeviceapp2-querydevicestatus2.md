---
title: Metodo IWMDRMDeviceApp2 QueryDeviceStatus2 (WMDRMDeviceApp. h)
description: Il metodo QueryDeviceStatus2 esegue una query su un dispositivo per uno stato o una funzionalità DRM specifica.
ms.assetid: f7e95fb7-5929-4a70-8580-a443e152e6d1
keywords:
- Metodo QueryDeviceStatus2 Windows Media Gestione dispositivi
- Metodo QueryDeviceStatus2 Windows Media Gestione dispositivi, interfaccia IWMDRMDeviceApp2
- Interfaccia IWMDRMDeviceApp2 Windows Media Gestione dispositivi, metodo QueryDeviceStatus2
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2.QueryDeviceStatus2
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d1f03f8d1e63086bb260c9854c7dcf3e88514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329207"
---
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a>Metodo IWMDRMDeviceApp2:: QueryDeviceStatus2

Il metodo **QueryDeviceStatus2** esegue una query su un dispositivo per uno stato o una funzionalità DRM specifica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryDeviceStatus2(
  [in]  IWMDMDevice *pDevice,
  [in]  DWORD       dwFlags,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Puntatore a un oggetto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Uno o più dei seguenti valori **DWORD** che specificano le funzionalità da richiedere, combinati con un **or** bit per bit.



| Flag                              | Descrizione                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| \_ \_ INDIVSTATUS client query \_ WMDRM | Eseguire una query per verificare se i componenti DRM del computer devono essere personalizzati.       |
| \_CLOCKSTATUS del \_ dispositivo di query WMDRM \_ | Eseguire una query per verificare se è necessario aggiungere o aggiornare il clock sicuro del dispositivo.        |
| il dispositivo di query WMDRM è stato \_ \_ \_ revocato   | Eseguire una query sull'eventuale revoca del dispositivo.                                         |
| \_ISWMDRM del \_ dispositivo di query WMDRM \_     | Eseguire una query per verificare se il dispositivo supporta Windows Media DRM 10 per i dispositivi portatili. |



 

</dd> <dt>

*pdwStatus* \[ out\]
</dt> <dd>

Zero o più dei seguenti valori **DWORD** che specificano lo stato del dispositivo richiesto, combinati con un **or** bit per bit.



| Stato                      | Descrizione                                              |
|-----------------------------|----------------------------------------------------------|
| \_ISWMDRM del dispositivo WMDRM \_      | Il dispositivo supporta Windows Media DRM.                   |
| \_NEEDCLOCK del dispositivo WMDRM \_    | Il dispositivo non ha un clock protetto.                 |
| il dispositivo WMDRM è stato \_ \_ revocato      | Il dispositivo è stato revocato.                             |
| \_NEEDINDIV client \_ WMDRM    | I componenti DRM del computer devono essere personalizzati. |
| \_REFRESHCLOCK del dispositivo WMDRM \_ | È necessario aggiornare il clock.                         |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                              | Descrizione                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                     | Il metodo è riuscito.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | Uno o più argomenti non sono validi.<br/>                           |
| <dl> <dt>**\_ \_ \_ certificato non valido per NS E DRM \_**</dt> </dl>          | Il certificato del dispositivo recuperato dal dispositivo non è valido.<br/> |
| <dl> <dt>**NS \_ E \_ DRM \_ non riescono \_ a \_ ottenere il \_ certificato del dispositivo \_**</dt> </dl> | Non è stato possibile recuperare il certificato del dispositivo dal dispositivo.<br/>     |



 

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato prima di eseguire qualsiasi azione limitata sul contenuto DRM, ad esempio il trasferimento di contenuto DRM al dispositivo o l'acquisizione di informazioni di misurazione. Se i valori recuperati *da pdwStatus* indicano che è necessario eseguire un'azione, ad esempio l'individualizzazione per il desktop o l'acquisizione di un clock per il dispositivo, l'applicazione deve [**chiamare IWMDRMDeviceApp:: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passare il valore *pdwStatus* recuperato da questa funzione al parametro *dwFlags* in **AcquireDeviceData**. Se viene restituito zero, il dispositivo non supporta Windows Media DRM 10 per i dispositivi portatili e non è necessario eseguire alcuna azione. Per ulteriori informazioni, vedere [gestione del contenuto protetto nell'applicazione](handling-protected-content-in-the-application.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDRMDeviceApp. h (richiede anche Wmdrmdeviceapp \_ i. c, compilato da WMDRMDeviceApp. idl)</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Gestione del contenuto protetto nell'applicazione**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[**Interfaccia IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 





