---
title: Metodo IMediaRendererActionInformation PlaySpeeds
description: Recupera l'elenco completo dei valori PlaySpeed accettati dalla dmr.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- Metodo PlaySpeeds API Streaming multimediale
- Metodo PlaySpeeds API Streaming multimediale, interfaccia IMediaRendererActionInformation
- Interfaccia IMediaRendererActionInformation API Streaming multimediale, metodo PlaySpeeds
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 573fe9da4e71f9c16a9850da352e866ddbb0f77abc8c30861f2aa29647065fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972200"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a>Metodo IMediaRendererActionInformation::P laySpeeds

Recupera l'elenco completo [**dei valori PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) accettati dalla dmr.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un vettore di [**strutture PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) che specifica l'elenco completo dei valori **PlaySpeed** accettati dalla dmr.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

