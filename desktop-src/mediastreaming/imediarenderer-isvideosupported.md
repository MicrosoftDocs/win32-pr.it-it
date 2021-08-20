---
title: Metodo IMediaRenderer IsVideoSupported
description: Recupera un valore che indica se la dmr è in grado di riprodurre contenuto video.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- Metodo IsVideoSupported API Streaming multimediale
- Metodo IsVideoSupported API Streaming multimediale, interfaccia IMediaRenderer
- Interfaccia IMediaRenderer API Streaming multimediale , metodo IsVideoSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c1f6fa149c6c5025d3fd2c785dc2f4a8451fabed3906b559674d8038662c21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972310"
---
# <a name="imediarendererisvideosupported-method"></a>Metodo IMediaRenderer::IsVideoSupported

Recupera un valore che indica se la dmr è in grado di riprodurre contenuto video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Valore booleano True **se** la dmr è in grado di riprodurre contenuto video e **False** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





