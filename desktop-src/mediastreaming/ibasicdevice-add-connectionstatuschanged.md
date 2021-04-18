---
title: Metodo add_ConnectionStatusChanged IBasicDevice
description: Registra un gestore eventi per l'evento ConnectionStatusChanged. | Metodo add_ConnectionStatusChanged IBasicDevice
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- API di streaming multimediale per il metodo add_ConnectionStatusChanged
- API di streaming multimediale del metodo add_ConnectionStatusChanged, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0028e6f3dad1670974178b0f07a59f74dffdc06f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321763"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a>Metodo IBasicDevice:: Add \_ ConnectionStatusChanged

Registra un gestore eventi per l'evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*gestore* \[ di in\]
</dt> <dd>

Funzione del gestore eventi [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .

</dd> <dt>

*token* \[ out, retval\]
</dt> <dd>

Riferimento a un token che può essere utilizzato per annullare la registrazione del gestore eventi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Per annullare la registrazione del gestore eventi registrato da questo metodo, passare il valore del *token* al metodo [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

