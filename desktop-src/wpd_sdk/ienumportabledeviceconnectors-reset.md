---
description: Riporta all'inizio la sequenza di enumerazione.
ms.assetid: 1df1ff95-06ae-4e5e-8064-17f832c5f0b3
title: 'Metodo IEnumPortableDeviceConnectors:: Reset (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Reset
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 3a6846ea928afb6cd52f20098cd100b94b3a564e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319089"
---
# <a name="ienumportabledeviceconnectorsreset-method"></a>Metodo IEnumPortableDeviceConnectors:: Reset

Il metodo **Reset** Reimposta l'inizio della sequenza di enumerazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

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

 

 




