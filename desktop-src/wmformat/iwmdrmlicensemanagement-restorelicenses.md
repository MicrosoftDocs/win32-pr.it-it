---
title: Metodo IWMDRMLicenseManagement RestoreLicenses (wmdrmsdk. h)
description: Il metodo RestoreLicenses Ripristina le licenze da un backup delle licenze creato chiamando il metodo BackupLicenses.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Metodo RestoreLicenses Windows Media Format
- Metodo RestoreLicenses Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo RestoreLicenses
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
ms.openlocfilehash: fb07f3989ff19faa723e4b1d1cd50dc4e269f219
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327464"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a>Metodo IWMDRMLicenseManagement:: RestoreLicenses

Il metodo **RestoreLicenses** Ripristina le licenze da un backup delle licenze creato chiamando il metodo [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) .

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

*bstrBackupDirectory* \[ in\]
</dt> <dd>

Percorso UNC della posizione da cui verranno ripristinate le licenze.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flag che specificano le opzioni di ripristino da utilizzare. L'unico flag attualmente supportato è WMDRM \_ Restore \_ individualizzato, che configura il metodo per eseguire l'individualizzazione come parte del ripristino, se necessario.

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

Questo metodo viene eseguito in modo asincrono. Viene restituito immediatamente dopo la chiamata di e quindi genera una serie di eventi **MEWMDRMLicenseRestoreProgress** seguiti da un evento **MEWMDRMLicenseRestoreCompleted** al termine dell'elaborazione. Il valore di ogni evento **MEWMDRMLicenseRestoreProgress** ottenuto chiamando **IMFMediaEvent:: GetValue** è un puntatore **IUnknown** . È possibile chiamare il metodo **QueryInterface** dell'interfaccia **IUnknown** recuperata per ottenere un'istanza dell'interfaccia [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .

Per ulteriori informazioni sull'utilizzo dei metodi asincroni delle API estese del client Windows Media DRM, vedere [utilizzo del modello di eventi Media Foundation](using-the-media-foundation-model.md).

Il backup può provenire dal computer locale o da un computer diverso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





