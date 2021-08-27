---
title: Metodo IWMDRMLicenseManagement MonitorLicenseAcquisition (Wmdrmsdk.h)
description: Il metodo MonitorLicenseAcquisition avvia il monitoraggio per un processo di acquisizione delle licenze.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- Metodo MonitorLicenseAcquisition windows Media Format
- Metodo MonitorLicenseAcquisition windows Media Format , interfaccia IWMDRMLicenseManagement
- Metodo MonitorLicenseAcquisition dell'interfaccia IWMDRMLicenseManagement di Windows Media Format
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ab3188425decca614ae104989fdc2f07930ac0de463e492be630a3fb54556e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027579"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a>Metodo IWMDRMLicenseManagement::MonitorLicenseAcquisition

Il **metodo MonitorLicenseAcquisition** avvia il monitoraggio per un processo di acquisizione delle licenze.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrKID* \[ Pollici\]
</dt> <dd>

ID chiave (KID) della licenza acquisita.

</dd> <dt>

*bstrHeader* \[ Pollici\]
</dt> <dd>

Intestazione di contenuto usata nella chiamata al [**metodo AcquireLicense.**](iwmdrmlicensemanagement-acquirelicense.md)

</dd> <dt>

*bstrActions* \[ Pollici\]
</dt> <dd>

Stringa contenente le azioni richieste nella chiamata al **metodo AcquireLicense.**

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

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





