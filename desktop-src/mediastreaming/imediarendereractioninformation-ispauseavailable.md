---
title: Metodo IMediaRendererActionInformation IsPauseAvailable
description: Recupera un valore che indica se ricevitore sta attualmente accettando il metodo PauseAsync.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- API di streaming multimediale del metodo IsPauseAvailable
- API di streaming multimediale del metodo IsPauseAvailable, interfaccia IMediaRendererActionInformation
- API di streaming multimediale dell'interfaccia IMediaRendererActionInformation, metodo IsPauseAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9eb0b750f5a04528aef830d87376c276bdaf6674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872466"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a>Metodo IMediaRendererActionInformation:: IsPauseAvailable

Recupera un valore che indica se ricevitore sta attualmente accettando il metodo [**PauseAsync**](imediarenderer-pauseasync.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Valore booleano che è **true** se ricevitore sta attualmente accettando il metodo [**PauseAsync**](imediarenderer-pauseasync.md) e **false** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

