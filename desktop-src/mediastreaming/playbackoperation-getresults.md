---
title: Metodo PlaybackOperation.GetResults
description: Restituisce i risultati di un'operazione asincrona avviata da uno dei metodi di riproduzione di MediaRenderer.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- Metodo GetResults API Streaming multimediale
- Metodo GetResults API Streaming multimediale, interfaccia PlaybackOperation
- PlaybackOperation interface Media Streaming API , metodo GetResults
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9bd3c79164a78e7993eb8a58d0d89a64c7ceb31a0c33eaff2e9c1bc352144088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235784"
---
# <a name="playbackoperationgetresults-method"></a>Metodo PlaybackOperation.GetResults

Restituisce i risultati di un'operazione asincrona avviata da uno dei [**metodi di riproduzione di MediaRenderer.**](mediarenderer.md)

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

Risultato dell'operazione. Il valore 0 indica che l'operazione è stata completata. Altri valori sono riservati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Il **metodo GetResults** viene in genere chiamato dal gestore eventi registrato impostando la [**proprietà Completed.**](playbackoperation-completed.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PlaybackOperation**](playbackoperation.md)
</dt> </dl>

 

 





