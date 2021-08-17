---
title: Metodo IAMWMBufferPass SetNotify
description: Il metodo SetNotify viene usato dalle applicazioni per fornire al filtro WM ASF Writer o WM ASF Reader un puntatore all'interfaccia IAMWMBufferPassCallback dell'applicazione.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- Metodo SetNotify windows Media Format
- Metodo SetNotify windows Media Format , interfaccia IAMWMBufferPass
- Metodo SetNotify dell'interfaccia IAMWMBufferPass windows Media Format
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47e189a2654ed4c760fdfcd6ced5506cc90d5e7cc989a7f79979e6d95b0bbfb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847607"
---
# <a name="iamwmbufferpasssetnotify-method"></a>Metodo IAMWMBufferPass::SetNotify

Il **metodo SetNotify** viene usato dalle applicazioni per fornire al filtro WM ASF Writer o [WM ASF Reader](wm-asf-reader-filter.md) un puntatore all'interfaccia [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCallback* \[ Pollici\]
</dt> <dd>

Puntatore all'interfaccia **IAMWMBufferPassCallback dell'applicazione.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Chiamare questo metodo prima di inserire il grafico del filtro nello stato di esecuzione.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 