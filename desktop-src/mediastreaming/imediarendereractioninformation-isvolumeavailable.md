---
title: Metodo IMediaRendererActionInformation IsVolumeAvailable
description: Recupera un valore che indica se ricevitore è in grado di regolare il livello del volume audio.
ms.assetid: 6DFDC37A-3304-4CDB-9928-C113D2F64ED0
keywords:
- API di streaming multimediale del metodo IsVolumeAvailable
- API di streaming multimediale del metodo IsVolumeAvailable, interfaccia IMediaRendererActionInformation
- API di streaming multimediale dell'interfaccia IMediaRendererActionInformation, metodo IsVolumeAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsVolumeAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb8dc60c25cf3ec12e0ebeaa863e239c287d7c46
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117619"
---
# <a name="imediarendereractioninformationisvolumeavailable-method"></a>Metodo IMediaRendererActionInformation:: IsVolumeAvailable

Recupera un valore che indica se ricevitore è in grado di regolare il livello del volume audio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsVolumeAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Valore booleano che è **true** se ricevitore è in grado di regolare il livello del volume audio e **false** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

