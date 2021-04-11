---
title: Metodo BasicDevice.remove_ConnectionStatusChanged
description: Annulla la registrazione di un gestore eventi per l'evento ConnectionStatusChanged. | Metodo BasicDevice.remove_ConnectionStatusChanged
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- API di streaming multimediale per il metodo remove_ConnectionStatusChanged
- API di streaming multimediale del metodo remove_ConnectionStatusChanged, interfaccia BasicDevice
- API di streaming multimediale dell'interfaccia BasicDevice, metodo remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdd39309774a61c4fd115ff09e16428101439a0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234804"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a>BasicDevice. Remove, \_ Metodo ConnectionStatusChanged

Annulla la registrazione di un gestore eventi per l'evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*token* \[ in\]
</dt> <dd>

Riferimento a un token ottenuto dal metodo [**Add \_ ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) quando è stato registrato il gestore eventi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

