---
title: BasicDevice.add_ConnectionStatusChanged metodo
description: Registra un gestore eventi per l'evento ConnectionStatusChanged. | BasicDevice.add_ConnectionStatusChanged metodo
ms.assetid: FFAA0981-508C-4300-9CA9-24C6AFC1183D
keywords:
- add_ConnectionStatusChanged metodo MEDIA Streaming API
- add_ConnectionStatusChanged metodo Media Streaming API , Interfaccia BasicDevice
- Interfaccia BasicDevice API Streaming multimediale, add_ConnectionStatusChanged metodo
topic_type:
- apiref
api_name:
- BasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a416770a0ea3a4d317a2308fc9f5c9d940e89900aabbc7651ceb93b789454338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462261"
---
# <a name="basicdeviceadd_connectionstatuschanged-method"></a>Metodo BasicDevice.add \_ ConnectionStatusChanged

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

Funzione [**del gestore eventi ConnectionStatusHandler.**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))

</dd> <dt>

*token* \[ out, retval\]
</dt> <dd>

Riferimento a un token che può essere usato per annullare la registrazione del gestore eventi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Per annullare la registrazione del gestore eventi registrato da questo metodo, passare il *valore del token* al metodo remove [**\_ ConnectionStatusChanged.**](basicdevice-remove-connectionstatuschanged.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

