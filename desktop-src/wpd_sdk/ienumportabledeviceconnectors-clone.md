---
description: Crea una copia dell'interfaccia IEnumPortableDeviceConnectors corrente.
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
title: 'Metodo IEnumPortableDeviceConnectors:: Clone (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Clone
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 0e5273f1c400732c94c7c63918787f5e130a854d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348566"
---
# <a name="ienumportabledeviceconnectorsclone-method"></a>Metodo IEnumPortableDeviceConnectors:: Clone

Il metodo **Clone** crea una copia dell'interfaccia [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
  [out] IEnumPortableDeviceConnectors **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Indirizzo di un puntatore a un'interfaccia [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) . L'applicazione chiamante deve rilasciare questa interfaccia quando viene eseguita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                                                                             |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                              |
| Intestazione<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>PortableDeviceConnectApi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>PortableDeviceConnectApi. idl</dt> </dl>                                                                |
| Libreria<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




