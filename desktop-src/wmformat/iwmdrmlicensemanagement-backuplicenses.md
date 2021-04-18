---
title: Metodo IWMDRMLicenseManagement BackupLicenses (wmdrmsdk. h)
description: Il metodo BackupLicenses crea una copia di backup delle licenze nell'archivio licenze locale.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- Metodo BackupLicenses Windows Media Format
- Metodo BackupLicenses Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo BackupLicenses
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
ms.openlocfilehash: 61c7f676b532353c839a428571f6d28540851bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327265"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a>Metodo IWMDRMLicenseManagement:: BackupLicenses

Il metodo **BackupLicenses** crea una copia di backup delle licenze nell'archivio licenze locale.

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

*bstrBackupDirectory* \[ in\]
</dt> <dd>

Percorso UNC della posizione in cui verrà eseguito il backup delle licenze.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flag che specificano le opzioni di backup da utilizzare. L'unico flag attualmente supportato è WMDRM \_ backup \_ overwrite, che configura il metodo per sovrascrivere eventuali file di backup esistenti nella directory.

</dd> <dt>

*ppunkCancelationCookie* \[ out\]
</dt> <dd>

Puntatore che riceve un puntatore all'interfaccia **IUnknown** di un oggetto che identifica la chiamata asincrona. Questo puntatore di interfaccia può essere utilizzato per annullare la chiamata asincrona chiamando il metodo [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene eseguito in modo asincrono. Viene restituito immediatamente dopo la chiamata di e quindi genera una serie di eventi **MEWMDRMLicenseBackupProgress** seguiti da un evento **MEWMDRMLicenseBackupCompleted** al termine dell'elaborazione. Il valore di ogni evento **MEWMDRMLicenseBackupProgress** ottenuto chiamando **IMFMediaEvent:: GetValue** è un puntatore **IUnknown** . È possibile chiamare il metodo **QueryInterface** dell'interfaccia **IUnknown** recuperata per ottenere un'istanza dell'interfaccia [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .

Per ulteriori informazioni sull'utilizzo dei metodi asincroni delle API estese del client Windows Media DRM, vedere [utilizzo del modello di eventi Media Foundation](using-the-media-foundation-model.md).

Non è consentito eseguire il backup di tutte le licenze. Questo metodo esegue il backup solo delle licenze che lo consentono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





