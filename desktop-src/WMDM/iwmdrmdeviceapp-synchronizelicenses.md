---
title: Metodo SynchronizeLicenses IWMDRMDeviceApp (WMDRMDeviceApp.h)
description: Il metodo SynchronizeLicenses aggiorna le licenze in un dispositivo quando stanno per scadere.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- Metodo SynchronizeLicenses in Gestione dispositivi multimediali di Windows
- Metodo SynchronizeLicenses windows Media Device Manager, interfaccia IWMDRMDeviceApp
- Interfaccia IWMDRMDeviceApp windows Media Device Manager, metodo SynchronizeLicenses
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
ms.openlocfilehash: 91ec48743bf52d990c64ce1aecf30897a7ee2f51664e88695a181f9d4f758140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031741"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a>Metodo IWMDRMDeviceApp::SynchronizeLicenses

Il **metodo SynchronizeLicenses** aggiorna le licenze in un dispositivo quando stanno per scadere.

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

*pDevice* \[ Pollici\]
</dt> <dd>

Puntatore a [**un oggetto IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)

</dd> <dt>

*pProgressCallback* \[ Pollici\]
</dt> <dd>

Callback di stato che riceverà lo stato di avanzamento di tutti i passaggi che potrebbe essere necessario eseguire. Il passaggio è identificato dal *parametro EventId* del metodo [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) chiamato.

</dd> <dt>

*cMinCountThreshold* \[ Pollici\]
</dt> <dd>

Numero minimo di riproduzione rimanente facoltativo per una licenza del dispositivo.

</dd> <dt>

*cMinHoursThreshold* \[ Pollici\]
</dt> <dd>

Numero minimo facoltativo di ore rimanenti per una licenza del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                         | Descrizione                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                | Il metodo è riuscito.<br/>                                                                                                                            |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                   | Uno o più argomenti non sono validi.<br/>                                                                                                             |
| <dl> <dt>**DRM \_ E \_ INVALIDXMLTAG**</dt> </dl>                | Il formato XML non è corretto.<br/>                                                                                                                        |
| <dl> <dt>**DRM \_ E \_ NOTIMPL**</dt> </dl>                      | Questa funzionalità non è attualmente implementata. (SyncLicenses w/ *pDevice* =NULL)<br/>                                                               |
| <dl> <dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt> </dl>                | Il formato XML della licenza non è corretto.<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ NOXMLOPENTAG**</dt> </dl>                 | Il formato XML della licenza non è corretto.<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ OUTOFMEMORY**</dt> </dl>                  | Memoria insufficiente.<br/>                                                                                                                                   |
| <dl> <dt>**DRM \_ E \_ XMLNOTFOUND**</dt> </dl>                  | Impossibile trovare un tag XML obbligatorio nella licenza.<br/>                                                                                                |
| <dl> <dt>**DISPOSITIVO NS \_ E \_ NON DISPOSITIVO \_ \_ \_ WMDRM**</dt> </dl>    | Il dispositivo specificato non è un Windows compatibile con Media DRM.<br/>                                                                               |
| <dl> <dt>**NS \_ E \_ DRM RICHIEDE \_ \_ L'INDIVIDUALIZZAZIONE**</dt> </dl> | Il DRM richiede un black box per eseguire questa funzione. In altre parole, l'SDK Windows Media Format richiede un aggiornamento della sicurezza.<br/> |



 

## <a name="remarks"></a>Commenti

Questa chiamata può essere effettuata solo in un dispositivo che supporta Windows Media DRM 10 per dispositivi portatili. È necessario specificare almeno un parametro threshold.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDRMDeviceApp.h (richiede anche Wmdrmdeviceapp \_ i.c, compilato da WMDRMDeviceApp.idl)</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Gestione del contenuto protetto nell'applicazione**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaccia IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**Interfaccia IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





