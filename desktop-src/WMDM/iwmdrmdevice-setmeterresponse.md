---
title: Metodo IWMDRMDevice SetMeterResponse
description: Il metodo SetMeterResponse imposta la risposta di misurazione.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Metodo SetMeterResponse in Gestione dispositivi multimediali di Windows
- Metodo SetMeterResponse windows Media Device Manager, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice windows Media Device Manager, metodo SetMeterResponse
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
ms.openlocfilehash: b05941619d30ea067dc594e05b7b427ec5d825ef3e0c3c441cdfb3c723e94d4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619571"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a>Metodo IWMDRMDevice::SetMeterResponse

Il **metodo SetMeterResponse** imposta la risposta di misurazione.

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

*pbMeterResponse* \[ Pollici\]
</dt> <dd>

Risposta di misurazione da impostare.

</dd> <dt>

*cbMeterResponse* \[ Pollici\]
</dt> <dd>

Dimensioni della risposta di misurazione, in byte.

</dd> <dt>

*pdwFlags* \[ Cambio\]
</dt> <dd>

Flag di risposta. Questo valore deve essere uno dei flag seguenti.



| Flag                            | Descrizione              |
|---------------------------------|--------------------------|
| RISPOSTA DEL CONTATORE WMDRM \_ \_ \_ ALL     | Tutte le risposte del contatore.     |
| RISPOSTA DEL CONTATORE WMDRM \_ \_ \_ PARZIALE | Risposte parziali del contatore. |



 

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

 

 





