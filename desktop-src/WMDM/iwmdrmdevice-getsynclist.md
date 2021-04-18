---
title: IWMDRMDevice metodo getsyncs
description: Il metodo getsyncname recupera l'elenco di sincronizzazione delle licenze nel dispositivo. La sincronizzazione delle licenze consente al computer host di trasferire le licenze aggiornate a un dispositivo in base ai criteri specificati.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Metodo getsyncname Windows Media Gestione dispositivi
- Metodo getsyncname Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo getsyncname
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
ms.openlocfilehash: 381d410bd938cb90855b182e62354d48e72f16d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327402"
---
# <a name="iwmdrmdevicegetsynclist-method"></a>Metodo IWMDRMDevice:: getsyncname

Il metodo **Getsyncname** recupera l'elenco di sincronizzazione delle licenze nel dispositivo. La sincronizzazione delle licenze consente al computer host di trasferire le licenze aggiornate a un dispositivo in base ai criteri specificati.

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

*cMinCountThreshold* \[ in\]
</dt> <dd>

Soglia numero minimo.

</dd> <dt>

*cMinHoursThreshold* \[ in\]
</dt> <dd>

Soglia ore minime.

</dd> <dt>

*ppbSyncList* \[ out\]
</dt> <dd>

Elenco di sincronizzazione delle licenze recuperato.

</dd> <dt>

*pcbSyncList* \[ out\]
</dt> <dd>

Dimensioni in byte dell'elenco di sincronizzazione delle licenze.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





