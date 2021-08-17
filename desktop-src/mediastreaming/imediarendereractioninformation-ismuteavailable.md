---
title: Metodo IMediaRendererActionInformation IsMuteAvailable
description: Recupera un valore che indica se la dmr è in grado di muto l'audio.
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- Metodo IsMuteAvailable API Streaming multimediale
- Metodo IsMuteAvailable API Streaming multimediale, interfaccia IMediaRendererActionInformation
- Interfaccia IMediaRendererActionInformation API Streaming multimediale , metodo IsMuteAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 331e2831ff18656f23a3d7067b8ab472835bf4a25760f6e86a92302621048a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871068"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a>Metodo IMediaRendererActionInformation::IsMuteAvailable

Recupera un valore che indica se la dmr è in grado di muto l'audio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Valore booleano True **se** la dmr è in grado di muto l'audio e **False** in caso contrario.

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

 

