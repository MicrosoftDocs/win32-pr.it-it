---
title: Metodo IWMDRMDeviceApp ProcessMeterResponse (WMDRMDeviceApp. h)
description: Il metodo ProcessMeterResponse Reimposta alcuni o tutti i conteggi di misurazione in un dispositivo, dopo che i dati del dispositivo sono stati inviati ed elaborati dal server.
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- Metodo ProcessMeterResponse Windows Media Gestione dispositivi
- Metodo ProcessMeterResponse Windows Media Gestione dispositivi, interfaccia IWMDRMDeviceApp
- Interfaccia IWMDRMDeviceApp Windows Media Gestione dispositivi, metodo ProcessMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.ProcessMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b57312dc2f401207e41f38f5bf75cddf69a13b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327878"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a>IWMDRMDeviceApp::P metodo rocessMeterResponse

Il metodo **ProcessMeterResponse** Reimposta alcuni o tutti i conteggi di misurazione in un dispositivo, dopo che i dati del dispositivo sono stati inviati ed elaborati dal server.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ProcessMeterResponse(
  [in]  IWMDMDevice *pDevice,
  [in]  BYTE        *pbResponse,
  [in]  DWORD       cbResponse,
  [out] DWORD       *pdwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Puntatore a un oggetto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*pbResponse* \[ in\]
</dt> <dd>

Risposta ricevuta da un server di controllo, dopo l'invio dei dati generati con [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).

</dd> <dt>

*cbResponse* \[ in\]
</dt> <dd>

Dimensioni di *pbResponse* in byte.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

**Valore DWORD** della tabella seguente che indica se nel dispositivo sono presenti più dati di misurazione che devono essere elaborati.



| Flag                            | Descrizione                                     |
|---------------------------------|-------------------------------------------------|
| \_risposta contatore \_ WMDRM \_ tutti     | Tutti i dati di misurazione sono stati elaborati.           |
| \_risposta contatore \_ WMDRM \_ parziale | È necessario elaborare dati di misurazione aggiuntivi. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                      | Descrizione                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                             | Il metodo è riuscito.<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | Uno o più argomenti non sono validi.<br/>                               |
| <dl> <dt>**Errori dal dispositivo**</dt> </dl>            | Qualsiasi numero di errori del dispositivo.<br/>                                  |
| <dl> <dt>**Errori dal client DRM**</dt> </dl>        | Uno qualsiasi dei numerosi errori interni del client DRM.<br/>                     |
| <dl> <dt>**dispositivo NS \_ E \_ dispositivo \_ non \_ WMDRM \_**</dt> </dl> | Il dispositivo specificato non è un dispositivo compatibile con Windows Media DRM.<br/> |



 

## <a name="remarks"></a>Commenti

Altre informazioni sulla misurazione, inclusi esempi di codice, sono disponibili nel white paper relativo all' [uso di contenuti multimediali digitali con Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) sul sito Web MSDN.

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

[**Interfaccia IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

