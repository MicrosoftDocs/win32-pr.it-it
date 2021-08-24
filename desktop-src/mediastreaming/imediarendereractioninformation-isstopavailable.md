---
title: Metodo IMediaRendererActionInformation IsStopAvailable
description: Recupera un valore che indica se la dmr accetta attualmente il metodo StopAsync.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- Metodo IsStopAvailable API Streaming multimediale
- Metodo IsStopAvailable API Streaming multimediale, interfaccia IMediaRendererActionInformation
- Metodo IsStopAvailable dell'interfaccia IMediaRendererActionInformation
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c177c46c62309525d9362f985075cec293105a80678b3b857eafa0524179d17e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712891"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a>Metodo IMediaRendererActionInformation::IsStopAvailable

Recupera un valore che indica se la dmr accetta attualmente il [**metodo StopAsync.**](imediarenderer-stopasync.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Valore booleano che è **True** se la dmr accetta attualmente il metodo [**StopAsync**](imediarenderer-stopasync.md) e **False** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

