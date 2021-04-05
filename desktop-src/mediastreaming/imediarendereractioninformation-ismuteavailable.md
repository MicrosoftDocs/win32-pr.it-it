---
title: Metodo IMediaRendererActionInformation IsMuteAvailable
description: Recupera un valore che indica se ricevitore è in grado di tacitare l'audio.
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- API di streaming multimediale del metodo IsMuteAvailable
- API di streaming multimediale del metodo IsMuteAvailable, interfaccia IMediaRendererActionInformation
- API di streaming multimediale dell'interfaccia IMediaRendererActionInformation, metodo IsMuteAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96751a7f2f1aedcd9e29be981ffadf6c43bf4008
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046631"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a>Metodo IMediaRendererActionInformation:: IsMuteAvailable

Recupera un valore che indica se ricevitore è in grado di tacitare l'audio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Valore booleano che è **true** se ricevitore è in grado di disattivare l'audio e **false** in caso contrario.

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

 

