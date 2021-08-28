---
title: Metodo IMediaRendererActionInformation IsSetNextSourceAvailable
description: Recupera un valore che indica se la dmr sta attualmente accettando il metodo SetNextSourceFromUriAsync, il metodo SetNextSourceFromStreamAsync o il metodo SetNextSourceFromMediaSourceAsync.
ms.assetid: 7588E992-4070-4E0F-8C4B-7DFC097A5076
keywords:
- Metodo IsSetNextSourceAvailable API Streaming multimediale
- Metodo IsSetNextSourceAvailable API Streaming multimediale, interfaccia IMediaRendererActionInformation
- Metodo IsSetNextSourceAvailable dell'interfaccia IMediaRendererActionInformation
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSetNextSourceAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee18eadbc535dd2cd4b48ec6f77adb1d3dec2f5a0c1f5065cee009e27635eda9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092301"
---
# <a name="imediarendereractioninformationissetnextsourceavailable-method"></a>Metodo IMediaRendererActionInformation::IsSetNextSourceAvailable

Recupera un valore che indica se la dmr sta attualmente accettando il [**metodo SetNextSourceFromUriAsync,**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) [**il metodo SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) o [**il metodo SetNextSourceFromMediaSourceAsync.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsSetNextSourceAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Valore booleano **True** se la DMR accetta attualmente il metodo [**SetNextSourceFromUriAsync,**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) [**il metodo SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) o [**il metodo SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) e **False** in caso contrario.

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

 

