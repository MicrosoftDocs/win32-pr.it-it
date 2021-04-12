---
title: Metodo IMsRdpDeviceCollection2 RedirectNow
description: Impone il reindirizzamento o la rimozione dei dispositivi selezionati o deselezionati dalla raccolta.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RedirectNow
- Metodo RedirectNow Servizi Desktop remoto, interfaccia IMsRdpDeviceCollection2
- Interfaccia IMsRdpDeviceCollection2 Servizi Desktop remoto, metodo RedirectNow
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893d1e26f504d5aeb45f795ea7425eeefc3a6232
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963773"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a>Metodo IMsRdpDeviceCollection2:: RedirectNow

Impone il reindirizzamento o la rimozione dei dispositivi selezionati o deselezionati dalla raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tipo* \[ di in\]
</dt> <dd>

Tipo: **[ **RedirectDeviceType**](redirectdevicetype.md)**

Valore dell'enumerazione [**RedirectDeviceType**](redirectdevicetype.md) che specifica il tipo di dispositivo da reindirizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RedirectDeviceType**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





