---
title: Metodo IWMDRMLicenseManagement RestoreLicenses (Wmdrmsdk.h)
description: Il metodo RestoreLicenses ripristina le licenze da un backup delle licenze creato chiamando il metodo BackupLicenses.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Metodo RestoreLicenses windows Media Format
- Metodo RestoreLicenses windows Media Format , interfaccia IWMDRMLicenseManagement
- IWMDRMLicenseManagement interface windows Media Format , RestoreLicenses method
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.RestoreLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a35fdd33df2387bb59dfac64f554dd8b5953fa3015afec6ca643725b9bd58f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846939"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a>Metodo IWMDRMLicenseManagement::RestoreLicenses

Il **metodo RestoreLicenses** ripristina le licenze da un backup delle licenze creato chiamando il [**metodo BackupLicenses.**](iwmdrmlicensemanagement-backuplicenses.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT RestoreLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrBackupDirectory* \[ Pollici\]
</dt> <dd>

Percorso UNC del percorso da cui verranno ripristinate le licenze.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Flag che specificano le opzioni di ripristino da usare. L'unico flag attualmente supportato è WMDRM RESTORE INDIVIDUALIZE, che configura il metodo per eseguire l'individualizzazione come parte \_ \_ del ripristino, se necessario.

</dd> <dt>

*ppunkCancelationCookie* \[ Cambio\]
</dt> <dd>

Puntatore che riceve un puntatore **all'interfaccia IUnknown** di un oggetto che identifica questa chiamata asincrona. Questo puntatore a interfaccia può essere usato per annullare la chiamata asincrona chiamando il [**metodo IWMDRMEventGenerator::CancelAsyncOperation.**](iwmdrmeventgenerator-cancelasyncoperation.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene eseguito in modo asincrono. Restituisce immediatamente dopo la chiamata e quindi genera una serie di eventi **MEWMDRMLicenseRestoreProgress** seguiti da un evento **MEWMDRMLicenseRestoreCompleted** al termine dell'elaborazione. Il valore di ogni evento **MEWMDRMLicenseRestoreProgress** ottenuto chiamando **IMFMediaEvent::GetValue** è un **puntatore IUnknown.** È possibile chiamare il **metodo QueryInterface** dell'interfaccia **IUnknown** recuperata per ottenere un'istanza dell'interfaccia [**IWMDRMLicenseBackupRestoreStatus.**](iwmdrmlicensebackuprestorestatus.md)

Per altre informazioni sull'uso dei metodi asincroni delle API estese Windows Media DRM Client, vedere [Using the Media Foundation Event Model](using-the-media-foundation-model.md).

Il backup può essere eseguito dal computer locale o da un computer diverso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





