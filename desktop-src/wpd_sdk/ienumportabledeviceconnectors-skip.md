---
description: Ignora il numero specificato di dispositivi nella sequenza di enumerazione.
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: 'Metodo IEnumPortableDeviceConnectors:: Skip (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Skip
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: c00daecccd12beee8e9e741c2906e47484fa6da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057890"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a>Metodo IEnumPortableDeviceConnectors:: Skip

Il metodo **Skip** ignora il numero specificato di dispositivi nella sequenza di enumerazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cConnectors* \[ in\]
</dt> <dd>

Numero di dispositivi da ignorare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Il metodo è riuscito.<br/>                                                                                                                                                          |
| <dl> <dt>**S \_ false**</dt> </dl> | Non è stato possibile ignorare il numero specificato di dispositivi. Una delle possibili cause: il parametro *cConnectors* specifica più dispositivi che rimangono effettivamente nella sequenza di enumerazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                                                                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                                   |
| Intestazione<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>PortableDeviceConnectApi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>PortableDeviceConnectApi. idl</dt> </dl>                                                                |
| Libreria<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




