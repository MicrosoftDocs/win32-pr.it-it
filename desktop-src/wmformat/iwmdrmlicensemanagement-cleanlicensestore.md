---
title: Metodo IWMDRMLicenseManagement CleanLicenseStore (wmdrmsdk. h)
description: Il metodo CleanLicenseStore rimuove le licenze inutilizzabili dall'archivio licenze temporaneo e deframmenta l'archivio licenze locale per migliorare le prestazioni.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Metodo CleanLicenseStore Windows Media Format
- Metodo CleanLicenseStore Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo CleanLicenseStore
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CleanLicenseStore
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9327fd836cf742f5495c29767be93d914c0f187
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325564"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a>Metodo IWMDRMLicenseManagement:: CleanLicenseStore

Il metodo **CleanLicenseStore** rimuove le licenze inutilizzabili dall'archivio licenze temporaneo e deframmenta l'archivio licenze locale per migliorare le prestazioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flag che specificano le opzioni di pulizia dell'archivio licenze da usare. Impostare su una delle costanti nella tabella seguente.



| Costante                            | Descrizione                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_sincronizzazione dell' \_ \_ archivio licenze clean WMDRM \_  | L'operazione di pulizia verrà eseguita in modo sincrono. Questo metodo non verrà restituito fino al completamento dell'operazione.                                                              |
| WMDRM \_ Clean \_ License \_ Store \_ asincrono | L'operazione di pulizia verrà eseguita in modo asincrono. Questo metodo restituirà immediatamente. Al termine dell'operazione, verrà inviato l'evento multimediale MELicenseStoreCleaned. |



 

</dd> <dt>

*ppunkCancelationCookie* \[ out\]
</dt> <dd>

Puntatore che riceve un puntatore all'interfaccia **IUnknown** di un oggetto che identifica la chiamata asincrona. Questo puntatore di interfaccia può essere utilizzato per annullare la chiamata asincrona chiamando il metodo [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                            | Descrizione                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Il metodo è riuscito.<br/>                                       |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | Nessun archivio licenze temporaneo nel computer client.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene eseguito in modo asincrono. Viene restituito immediatamente dopo la chiamata di e quindi genera un evento **MEWMDRMLicenseStoreCleaned** al termine dell'elaborazione.

Per ulteriori informazioni sull'utilizzo dei metodi asincroni delle API estese del client Windows Media DRM, vedere [utilizzo del modello di eventi Media Foundation](using-the-media-foundation-model.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





