---
title: Metodo GetMuteOperation. GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da GetMuteAsync.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- API di streaming multimediale metodo GetResults
- API di streaming multimediale del metodo GetResults, interfaccia GetMuteOperation
- API di streaming multimediale dell'interfaccia GetMuteOperation, metodo GetResults
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33c43dc7fee228b1808ff4f607ee6a72faf1e770
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117623"
---
# <a name="getmuteoperationgetresults-method"></a>Metodo GetMuteOperation. GetResults

Restituisce i risultati dell'operazione asincrona avviata da [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out, retval\]
</dt> <dd>

Valore di silenziamento. Il valore true indica che l'audio è attualmente disattivato. Il valore false indica che l'audio non è disattivato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Il metodo **GetResults** viene in genere chiamato dal gestore eventi registrato impostando la proprietà [**Completed**](getmuteoperation-completed.md) .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetMuteOperation**](getmuteoperation.md)
</dt> </dl>

 

