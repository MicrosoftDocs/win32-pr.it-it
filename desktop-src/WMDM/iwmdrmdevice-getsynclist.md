---
title: Metodo GetSyncList IWMDRMDevice
description: Il metodo GetSyncList recupera l'elenco di sincronizzazione delle licenze nel dispositivo. La sincronizzazione delle licenze consente al computer host di trasferire le licenze aggiornate a un dispositivo in base ai criteri specificati.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Metodo GetSyncList windows Media Device Manager
- Metodo GetSyncList windows Media Device Manager , interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice windows Media Device Manager, metodo GetSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6424daa720f9987228175a7698a29f7056e5d4b4d174d1d635bbcd1ed7f8382
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619581"
---
# <a name="iwmdrmdevicegetsynclist-method"></a>Metodo IWMDRMDevice::GetSyncList

Il **metodo GetSyncList** recupera l'elenco di sincronizzazione delle licenze nel dispositivo. La sincronizzazione delle licenze consente al computer host di trasferire le licenze aggiornate a un dispositivo in base ai criteri specificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cMinCountThreshold* \[ Pollici\]
</dt> <dd>

Soglia minima di conteggio.

</dd> <dt>

*cMinHoursThreshold* \[ Pollici\]
</dt> <dd>

Soglia minima ore.

</dd> <dt>

*ppbSyncList* \[ Cambio\]
</dt> <dd>

Recupero dell'elenco di sincronizzazione delle licenze.

</dd> <dt>

*pcbSyncList* \[ Cambio\]
</dt> <dd>

Dimensioni dell'elenco di sincronizzazione delle licenze, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



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

 

 





