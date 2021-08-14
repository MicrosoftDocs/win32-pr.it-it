---
title: Metodo IMediaRenderer ActionInformation
description: Recupera informazioni sui metodi che possono essere attualmente richiamati nella dmr.
ms.assetid: 7681FF92-DD13-4BBC-B860-E2BDFDA74FB9
keywords:
- Metodo ActionInformation API Streaming multimediale
- Metodo ActionInformation API Streaming multimediale, interfaccia IMediaRenderer
- Interfaccia IMediaRenderer API Streaming multimediale, metodo ActionInformation
topic_type:
- apiref
api_name:
- IMediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3caf251c080f218b99861d4a81920cd5c95c1f0e53bc6b006c84536f33f7f29c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735524"
---
# <a name="imediarendereractioninformation-method"></a>Metodo IMediaRenderer::ActionInformation

Recupera informazioni sui metodi che possono essere attualmente richiamati nella dmr.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un riferimento a [**un'interfaccia IMediaRendererActionInformation.**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

