---
title: Metodo IMediaRendererActionInformation IsVolumeAvailable
description: Recupera un valore che indica se la dmr è in grado di regolare il livello del volume audio.
ms.assetid: 6DFDC37A-3304-4CDB-9928-C113D2F64ED0
keywords:
- Metodo IsVolumeAvailable API Streaming multimediale
- Metodo IsVolumeAvailable API Streaming multimediale, interfaccia IMediaRendererActionInformation
- Interfaccia IMediaRendererActionInformation API Streaming multimediale , metodo IsVolumeAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsVolumeAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce36a9151998a5f7b0a7785aebc1795bd29d31ff47cfdd2368978ad040f3597c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972210"
---
# <a name="imediarendereractioninformationisvolumeavailable-method"></a>Metodo IMediaRendererActionInformation::IsVolumeAvailable

Recupera un valore che indica se la dmr è in grado di regolare il livello del volume audio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsVolumeAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Valore booleano True **se** la dmr è in grado di regolare il livello del volume audio e **False** in caso contrario.

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

 

