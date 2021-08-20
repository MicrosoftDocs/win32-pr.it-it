---
title: Metodo GetMuteOperation.GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da GetMuteAsync.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- Metodo GetResults API Streaming multimediale
- Metodo GetResults API Streaming multimediale, interfaccia GetMuteOperation
- Interfaccia GetMuteOperation API Streaming multimediale, metodo GetResults
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37b8356a677f5e752fdf4e4ec658cc4077a17fa76b6181097d5753d898eef89e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972410"
---
# <a name="getmuteoperationgetresults-method"></a>Metodo GetMuteOperation.GetResults

Restituisce i risultati dell'operazione asincrona avviata [**da GetMuteAsync.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Valore mute. Il valore true indica che l'audio è attualmente disattivato. Il valore false indica che l'audio non è disattivato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Il **metodo GetResults** viene in genere chiamato dal gestore eventi registrato impostando la [**proprietà Completed.**](getmuteoperation-completed.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetMuteOperation**](getmuteoperation.md)
</dt> </dl>

 

