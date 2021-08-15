---
description: Ignora il numero specificato di dispositivi nella sequenza di enumerazione.
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: Metodo IEnumPortableDeviceConnectors::Skip (Devpkey.h)
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
ms.openlocfilehash: ba704a2dd232ce5c8ba08d0271e5e0a8fda72f86f9aef89d2e89b04ca9fe94b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546551"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a>Metodo IEnumPortableDeviceConnectors::Skip

Il **metodo Skip** ignora il numero specificato di dispositivi nella sequenza di enumerazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cConnectors* \[ Pollici\]
</dt> <dd>

Numero di dispositivi da ignorare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Il metodo è riuscito.<br/>                                                                                                                                                          |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Impossibile ignorare il numero specificato di dispositivi. Una possibile causa: il *parametro cConnectors* specifica più dispositivi di quelli effettivamente presenti nella sequenza di enumerazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                                                                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                                   |
| Intestazione<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Libreria<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




