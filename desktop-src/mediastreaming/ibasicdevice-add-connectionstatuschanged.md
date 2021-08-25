---
title: Metodo add_ConnectionStatusChanged IBasicDevice
description: Registra un gestore eventi per l'evento ConnectionStatusChanged. | Metodo add_ConnectionStatusChanged IBasicDevice
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- add_ConnectionStatusChanged'API Streaming multimediale
- add_ConnectionStatusChanged metodo Media Streaming API , interfaccia IBasicDevice
- Interfaccia IBasicDevice API Streaming multimediale, add_ConnectionStatusChanged metodo
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e90ea1f90ccd5b1e141b0e4071213abfe6f4a05a85d3c0d4ced505e1b0f164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952661"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a>Metodo IBasicDevice::add \_ ConnectionStatusChanged

Registra un gestore eventi per [**l'evento ConnectionStatusChanged.**](connectionstatuschanged.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*gestore* \[ Pollici\]
</dt> <dd>

Funzione [**del gestore dell'evento ConnectionStatusHandler.**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))

</dd> <dt>

*token* \[ out, retval\]
</dt> <dd>

Riferimento a un token che può essere usato per annullare la registrazione del gestore eventi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Per annullare la registrazione del gestore eventi registrato da questo metodo, passare il *valore del token* al metodo remove [**\_ ConnectionStatusChanged.**](ibasicdevice-remove-connectionstatuschanged.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

