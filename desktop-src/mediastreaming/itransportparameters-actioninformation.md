---
title: Metodo ITransportParameters ActionInformation
description: Ottiene un'interfaccia IMediaRendererActionInformation che fornisce informazioni sui metodi che possono essere attualmente richiamati in ricevitore.
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- API di streaming multimediale del metodo ActionInformation
- API di streaming multimediale del metodo ActionInformation, interfaccia ITransportParameters
- API di streaming multimediale dell'interfaccia ITransportParameters, metodo ActionInformation
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b194da50e71402b6af69eb4cc9d67902e8ae89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046644"
---
# <a name="itransportparametersactioninformation-method"></a>Metodo ITransportParameters:: ActionInformation

Ottiene un'interfaccia [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) che fornisce informazioni sui metodi che possono essere attualmente richiamati in ricevitore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out, retval\]
</dt> <dd>

Riceve un riferimento a un'interfaccia [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

