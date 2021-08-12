---
title: Metodo ITransportParameters ActionInformation
description: Ottiene un'interfaccia IMediaRendererActionInformation che fornisce informazioni sui metodi che possono essere attualmente richiamati nella dmr.
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- Metodo ActionInformation API Streaming multimediale
- Metodo ActionInformation API Streaming multimediale, interfaccia ITransportParameters
- Interfaccia ITransportParameters API Streaming multimediale, metodo ActionInformation
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 551612fcaffb9379823efea15f29ed9feba1ff3d0c5af6e7271b61ad9d6036f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235856"
---
# <a name="itransportparametersactioninformation-method"></a>Metodo ITransportParameters::ActionInformation

Ottiene [**un'interfaccia IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) che fornisce informazioni sui metodi che possono essere attualmente richiamati nella dmr.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ out, retval\]
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

[**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

