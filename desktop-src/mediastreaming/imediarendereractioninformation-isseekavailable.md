---
title: Metodo IMediaRendererActionInformation IsSeekAvailable
description: Recupera un valore che indica se ricevitore sta attualmente accettando il Metodo SeekAsync.
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- API di streaming multimediale del metodo IsSeekAvailable
- API di streaming multimediale del metodo IsSeekAvailable, interfaccia IMediaRendererActionInformation
- API di streaming multimediale dell'interfaccia IMediaRendererActionInformation, metodo IsSeekAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 700afb72efbab01bbd3a8f5e15fa444eb6b06272
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872465"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a>Metodo IMediaRendererActionInformation:: IsSeekAvailable

Recupera un valore che indica se ricevitore sta attualmente accettando il metodo [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Valore booleano che è **true** se ricevitore sta attualmente accettando il metodo [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) e **false** in caso contrario.

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

 

