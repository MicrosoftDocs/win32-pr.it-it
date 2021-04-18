---
title: Metodo IMediaRenderer IsAudioSupported
description: Recupera un valore che indica se ricevitore è in grado di riprodurre contenuto audio.
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- API di streaming multimediale del metodo IsAudioSupported
- API di streaming multimediale del metodo IsAudioSupported, interfaccia IMediaRenderer
- API di streaming multimediale dell'interfaccia IMediaRenderer, metodo IsAudioSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7670d0a2818cf5518bee0b2586531caeea20fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299023"
---
# <a name="imediarendererisaudiosupported-method"></a>Metodo IMediaRenderer:: IsAudioSupported

Recupera un valore che indica se ricevitore è in grado di riprodurre contenuto audio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Valore booleano che è **true** se ricevitore è in grado di riprodurre contenuto audio e **false** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





