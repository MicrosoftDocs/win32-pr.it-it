---
title: Metodo IWMDRMLicenseManagement BackupLicenses (Wmdrmsdk.h)
description: Il metodo BackupLicenses crea un backup delle licenze nell'archivio licenze locale.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- Metodo BackupLicenses windows Media Format
- Metodo BackupLicenses windows Media Format , interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement windows Media Format , metodo BackupLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3905f8fd464645f7fcd22551360e6a9610913eeea7f191d7e770e24f5ea8cd49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027649"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a>Metodo IWMDRMLicenseManagement::BackupLicenses

Il **metodo BackupLicenses** crea un backup delle licenze nell'archivio licenze locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrBackupDirectory* \[ Pollici\]
</dt> <dd>

Percorso UNC del percorso in cui verrà eseguito il backup delle licenze.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Flag che specificano le opzioni di backup da usare. L'unico flag attualmente supportato è WMDRM BACKUP OVERWRITE, che configura il metodo per sovrascrivere tutti i file di \_ \_ backup esistenti nella directory.

</dd> <dt>

*ppunkCancelationCookie* \[ Cambio\]
</dt> <dd>

Puntatore che riceve un puntatore **all'interfaccia IUnknown** di un oggetto che identifica questa chiamata asincrona. Questo puntatore a interfaccia può essere usato per annullare la chiamata asincrona chiamando il metodo [**IWMDRMEventGenerator::CancelAsyncOperation.**](iwmdrmeventgenerator-cancelasyncoperation.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene eseguito in modo asincrono. Restituisce immediatamente dopo la chiamata e quindi genera una serie di eventi **MEWMDRMLicenseBackupProgress** seguiti da un evento **MEWMDRMLicenseBackupCompleted** al termine dell'elaborazione. Il valore di ogni evento **MEWMDRMLicenseBackupProgress** ottenuto chiamando **IMFMediaEvent::GetValue** è un **puntatore IUnknown.** È possibile chiamare il **metodo QueryInterface** dell'interfaccia **IUnknown** recuperata per ottenere un'istanza dell'interfaccia [**IWMDRMLicenseBackupRestoreStatus.**](iwmdrmlicensebackuprestorestatus.md)

Per altre informazioni sull'uso dei metodi asincroni delle API estese Windows Media DRM Client, vedere [Using the Media Foundation Event Model](using-the-media-foundation-model.md).

Non è consentito eseguire il backup di tutte le licenze. Questo metodo esegue solo il backup delle licenze che lo consentono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





