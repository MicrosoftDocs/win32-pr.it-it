---
title: Metodo IMediaRendererActionInformation IsPauseAvailable
description: Recupera un valore che indica se la dmr accetta attualmente il metodo PauseAsync.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- Metodo IsPauseAvailable API Streaming multimediale
- Metodo IsPauseAvailable API Streaming multimediale, interfaccia IMediaRendererActionInformation
- Metodo IsPauseAvailable dell'interfaccia IMediaRendererActionInformation
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fad69863306a8a937771f16c2ab9a83a2622c571d2cd5ee5658a279bf7564132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870848"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a>Metodo IMediaRendererActionInformation::IsPauseAvailable

Recupera un valore che indica se la dmr accetta attualmente il [**metodo PauseAsync.**](imediarenderer-pauseasync.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Valore booleano true **se** la dmr accetta attualmente il metodo [**PauseAsync**](imediarenderer-pauseasync.md) e **False** in caso contrario.

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

 

