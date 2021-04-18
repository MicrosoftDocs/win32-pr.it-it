---
title: Metodo IWMDRMDeviceApp SynchronizeLicenses (WMDRMDeviceApp. h)
description: Il metodo SynchronizeLicenses aggiorna le licenze in un dispositivo quando sono vicine alla scadenza.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- Metodo SynchronizeLicenses Windows Media Gestione dispositivi
- Metodo SynchronizeLicenses Windows Media Gestione dispositivi, interfaccia IWMDRMDeviceApp
- Interfaccia IWMDRMDeviceApp Windows Media Gestione dispositivi, metodo SynchronizeLicenses
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.SynchronizeLicenses
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08f3457fec55a0eb519419feddf4594a2cbfac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329208"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a>Metodo IWMDRMDeviceApp:: SynchronizeLicenses

Il metodo **SynchronizeLicenses** aggiorna le licenze in un dispositivo quando sono vicine alla scadenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SynchronizeLicenses(
  [in] IWMDMDevice    *pDevice,
  [in] IWMDMProgress3 *pProgressCallback,
  [in] DWORD          cMinCountThreshold,
  [in] DWORD          cMinHoursThreshold
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Puntatore a un oggetto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*pProgressCallback* \[ in\]
</dt> <dd>

Callback di stato che riceverà lo stato di tutti i passaggi che potrebbero essere necessari per eseguire. Il passaggio viene identificato dal parametro *eventId* del metodo [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) chiamato.

</dd> <dt>

*cMinCountThreshold* \[ in\]
</dt> <dd>

Numero minimo di Play rimanenti facoltativo in una licenza del dispositivo.

</dd> <dt>

*cMinHoursThreshold* \[ in\]
</dt> <dd>

Numero minimo di ore rimanenti facoltative per una licenza del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                         | Descrizione                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                | Il metodo è riuscito.<br/>                                                                                                                            |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                   | Uno o più argomenti non sono validi.<br/>                                                                                                             |
| <dl> <dt>**DRM \_ E \_ INVALIDXMLTAG**</dt> </dl>                | Il formato XML non è corretto.<br/>                                                                                                                        |
| <dl> <dt>**DRM \_ E \_ NOTIMPL**</dt> </dl>                      | Questa funzionalità non è attualmente implementata. (SyncLicenses w/ *PDEVICE* = null)<br/>                                                               |
| <dl> <dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt> </dl>                | Il formato dell'XML di licenza non è corretto.<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ NOXMLOPENTAG**</dt> </dl>                 | Il formato dell'XML di licenza non è corretto.<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ OutOfMemory**</dt> </dl>                  | Memoria insufficiente.<br/>                                                                                                                                   |
| <dl> <dt>**DRM \_ E \_ XMLNOTFOUND**</dt> </dl>                  | Impossibile trovare un tag XML necessario nella licenza.<br/>                                                                                                |
| <dl> <dt>**dispositivo NS \_ E \_ dispositivo \_ non \_ WMDRM \_**</dt> </dl>    | Il dispositivo specificato non è un dispositivo compatibile con DRM di Windows Media.<br/>                                                                               |
| <dl> <dt>**NS \_ E \_ DRM \_ necessitano di un' \_ individualizzazione**</dt> </dl> | Per eseguire questa funzione, il DRM richiede un black box individualizzato. In altre parole, Windows Media Format SDK richiede un aggiornamento della sicurezza.<br/> |



 

## <a name="remarks"></a>Commenti

Questa chiamata può essere eseguita solo su un dispositivo che supporta Windows Media DRM 10 per i dispositivi portatili. È necessario specificare almeno un parametro di soglia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDRMDeviceApp. h (richiede anche Wmdrmdeviceapp \_ i. c, compilato da WMDRMDeviceApp. idl)</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Gestione del contenuto protetto nell'applicazione**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaccia IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**Interfaccia IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





