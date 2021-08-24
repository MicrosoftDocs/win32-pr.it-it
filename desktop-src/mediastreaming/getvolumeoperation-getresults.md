---
title: Metodo GetVolumeOperation.GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da GetVolumeAsync.
ms.assetid: 71DC4D76-4CC2-4D40-960F-AF56E1F33557
keywords:
- Metodo GetResults API Streaming multimediale
- Metodo GetResults API Streaming multimediale, interfaccia GetVolumeOperation
- Interfaccia GetVolumeOperation API Streaming multimediale, metodo GetResults
topic_type:
- apiref
api_name:
- GetVolumeOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e58188a0d8b0d2ed13a9cb7d7486f440f4a1303ca32208371690965f976339d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011851"
---
# <a name="getvolumeoperationgetresults-method"></a>Metodo GetVolumeOperation.GetResults

Restituisce i risultati dell'operazione asincrona avviata [**da GetVolumeAsync.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Volume. Valore compreso tra 0 e 100. 0 indica il volume minimo e 100 indica il volume massimo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Il **metodo GetResults** viene in genere chiamato dal gestore eventi registrato impostando la [**proprietà Completed.**](getvolumeoperation-completed.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetVolumeOperation**](getvolumeoperation.md)
</dt> </dl>

 

