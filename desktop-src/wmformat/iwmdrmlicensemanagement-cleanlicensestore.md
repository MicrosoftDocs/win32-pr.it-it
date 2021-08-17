---
title: Metodo IWMDRMLicenseManagement CleanLicenseStore (Wmdrmsdk.h)
description: Il metodo CleanLicenseStore rimuove le licenze inutilizzabili dall'archivio licenze temporaneo e deframmenta l'archivio licenze locale per migliorare le prestazioni.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Metodo CleanLicenseStore windows Media Format
- Metodo CleanLicenseStore windows Media Format , interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement windows Media Format , metodo CleanLicenseStore
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
ms.openlocfilehash: 6010313efaca6855c403f9ee698284ff4aebb2e0ab8a5e08e5862a5890224a1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846954"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a>Metodo IWMDRMLicenseManagement::CleanLicenseStore

Il **metodo CleanLicenseStore** rimuove le licenze inutilizzabili dall'archivio licenze temporaneo e deframmenta l'archivio licenze locale per migliorare le prestazioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Flag che specificano le opzioni di pulizia dell'archivio licenze da usare. Impostare su una delle costanti nella tabella seguente.



| Costante                            | Descrizione                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SINCRONIZZAZIONE \_ \_ DELL'ARCHIVIO LICENZE PULITA \_ \_ WMDRM  | L'operazione di pulizia verrà eseguita in modo sincrono. Questo metodo non verrà restituito fino al completamento dell'operazione.                                                              |
| WMDRM \_ CLEAN \_ LICENSE \_ STORE \_ ASYNC | L'operazione di pulizia verrà eseguita in modo asincrono. Questo metodo restituirà immediatamente . Al termine dell'operazione, verrà inviato l'evento multimediale MELicenseStoreCleaned. |



 

</dd> <dt>

*ppunkCancelationCookie* \[ Cambio\]
</dt> <dd>

Puntatore che riceve un puntatore **all'interfaccia IUnknown** di un oggetto che identifica questa chiamata asincrona. Questo puntatore a interfaccia può essere usato per annullare la chiamata asincrona chiamando il [**metodo IWMDRMEventGenerator::CancelAsyncOperation.**](iwmdrmeventgenerator-cancelasyncoperation.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                            | Descrizione                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Il metodo è riuscito.<br/>                                       |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | Nel computer client non è presente alcun archivio licenze temporaneo.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene eseguito in modo asincrono. Restituisce immediatamente dopo essere stato chiamato e quindi genera un **evento MEWMDRMLicenseStoreCleaned** al termine dell'elaborazione.

Per altre informazioni sull'uso dei metodi asincroni delle API estese del client DRM di Windows, vedere [Using the Media Foundation Event Model](using-the-media-foundation-model.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





