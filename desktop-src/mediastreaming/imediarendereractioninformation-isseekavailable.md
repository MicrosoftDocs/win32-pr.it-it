---
title: Metodo IMediaRendererActionInformation IsSeekAvailable
description: Recupera un valore che indica se la dmr sta attualmente accettando il metodo SeekAsync.
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- Metodo IsSeekAvailable API Streaming multimediale
- Metodo IsSeekAvailable API Streaming multimediale, interfaccia IMediaRendererActionInformation
- Metodo IsSeekAvailable dell'interfaccia IMediaRendererActionInformation
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32b5c7eef78dad4ebfeeebb40c323d7b13e540033eb54852f7da41942f5ec83e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735514"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a>Metodo IMediaRendererActionInformation::IsSeekAvailable

Recupera un valore che indica se la dmr sta attualmente accettando il [**metodo SeekAsync.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Valore booleano True **se** la dmr accetta attualmente il metodo [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) e **False** in caso contrario.

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

 

