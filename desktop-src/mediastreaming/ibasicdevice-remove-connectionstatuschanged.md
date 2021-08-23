---
title: Metodo remove_ConnectionStatusChanged IBasicDevice
description: Annulla la registrazione di un gestore eventi per l'evento ConnectionStatusChanged. | Metodo remove_ConnectionStatusChanged IBasicDevice
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- remove_ConnectionStatusChanged api Streaming multimediale
- remove_ConnectionStatusChanged metodo Media Streaming API , interfaccia IBasicDevice
- Interfaccia IBasicDevice API Streaming multimediale, remove_ConnectionStatusChanged metodo
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35b2f08b6df25f57d77f5c3677a4c6499370d9472202b6808073c5a75d1e2c34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599801"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a>Metodo IBasicDevice::remove \_ ConnectionStatusChanged

Annulla la registrazione di un gestore eventi per [**l'evento ConnectionStatusChanged.**](connectionstatuschanged.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*token* \[ Pollici\]
</dt> <dd>

Riferimento a un token ottenuto dal metodo [**add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) quando è stato registrato il gestore eventi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





