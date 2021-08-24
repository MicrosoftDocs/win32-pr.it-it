---
title: Metodo IWMDRMDevice CleanDataStore
description: Il metodo CleanDataStore avvia il processo di pulizia dell'archivio dati DRM nel dispositivo.
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- Metodo CleanDataStore windows Media Device Manager
- Metodo CleanDataStore windows Media Device Manager, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice windows Media Device Manager, metodo CleanDataStore
topic_type:
- apiref
api_name:
- IWMDRMDevice.CleanDataStore
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9decc999d1ecb6c97359d1c4c169b84e7f67da88f5fa25bfe2cb17b2c31f9fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766641"
---
# <a name="iwmdrmdevicecleandatastore-method"></a>Metodo IWMDRMDevice::CleanDataStore

Il **metodo CleanDataStore** avvia il processo di pulizia dell'archivio dati DRM nel dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CleanDataStore(
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Flag per i criteri di pulizia dell'archivio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





