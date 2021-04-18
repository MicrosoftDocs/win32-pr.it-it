---
title: Metodo IWMDRMDevice SetMeterResponse
description: Il metodo SetMeterResponse imposta la risposta di misurazione.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Metodo SetMeterResponse Windows Media Gestione dispositivi
- Metodo SetMeterResponse Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo SetMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed70b158215eb831296ad083af8cd2c001cb38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327395"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a>Metodo IWMDRMDevice:: SetMeterResponse

Il metodo **SetMeterResponse** imposta la risposta di misurazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMeterResponse(
  [in]  BYTE  *pbMeterResponse,
  [in]  DWORD cbMeterResponse,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbMeterResponse* \[ in\]
</dt> <dd>

Risposta di misurazione da impostare.

</dd> <dt>

*cbMeterResponse* \[ in\]
</dt> <dd>

Dimensioni in byte della risposta di misurazione.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Flag di risposta. Questo valore deve essere uno dei flag seguenti.



| Flag                            | Descrizione              |
|---------------------------------|--------------------------|
| \_risposta contatore \_ WMDRM \_ tutti     | Tutte le risposte del contatore.     |
| \_risposta contatore \_ WMDRM \_ parziale | Risposte parziali del contatore. |



 

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

 

 





