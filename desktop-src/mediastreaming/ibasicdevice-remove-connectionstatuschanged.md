---
title: Metodo remove_ConnectionStatusChanged IBasicDevice
description: Annulla la registrazione di un gestore eventi per l'evento ConnectionStatusChanged. | Metodo remove_ConnectionStatusChanged IBasicDevice
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- API di streaming multimediale per il metodo remove_ConnectionStatusChanged
- API di streaming multimediale del metodo remove_ConnectionStatusChanged, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c2bfa2886774ad637e66385a057c9d4e21efe0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321557"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a>Metodo IBasicDevice:: Remove \_ ConnectionStatusChanged

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

Riferimento a un token ottenuto dal metodo [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) quando è stato registrato il gestore eventi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





