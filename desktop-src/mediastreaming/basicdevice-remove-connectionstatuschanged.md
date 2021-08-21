---
title: BasicDevice.remove_ConnectionStatusChanged metodo
description: Annulla la registrazione di un gestore eventi per l'evento ConnectionStatusChanged. | BasicDevice.remove_ConnectionStatusChanged metodo
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- remove_ConnectionStatusChanged'API Streaming multimediale
- remove_ConnectionStatusChanged metodo Media Streaming API , interfaccia BasicDevice
- BasicDevice interface Media Streaming API , remove_ConnectionStatusChanged metodo
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89057195c23aa917c7338a8abb740817bb6af7896261cf1d31bcb37d5d5d5ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972500"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a>Metodo BasicDevice.remove \_ ConnectionStatusChanged

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

Riferimento a un token ottenuto dal metodo [**add \_ ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) quando è stato registrato il gestore eventi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

