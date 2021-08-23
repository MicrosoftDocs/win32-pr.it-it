---
title: Metodo IsAudioSupported di IMediaRenderer
description: Recupera un valore che indica se la dmr è in grado di riprodurre contenuto audio.
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- Metodo IsAudioSupported API Streaming multimediale
- Metodo IsAudioSupported API Streaming multimediale, interfaccia IMediaRenderer
- Interfaccia IMediaRenderer API Streaming multimediale , metodo IsAudioSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5abe42e65e451464a5f7f3a4d59679db62c3634e95e89e5e275919dd0ece869e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777011"
---
# <a name="imediarendererisaudiosupported-method"></a>Metodo IMediaRenderer::IsAudioSupported

Recupera un valore che indica se la dmr è in grado di riprodurre contenuto audio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Valore booleano True **se** la dmr è in grado di riprodurre contenuto audio e **False** in caso contrario.

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

 

 





