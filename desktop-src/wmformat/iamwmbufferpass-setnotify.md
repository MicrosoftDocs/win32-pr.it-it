---
title: Metodo IAMWMBufferPass senotify
description: Il metodo senotify viene usato dalle applicazioni per fornire il filtro WM ASF Writer o WM ASF Reader con un puntatore all'interfaccia IAMWMBufferPassCallback dell'applicazione.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- Metodo senotify-formato Windows Media
- Metodo senotify, formato Windows Media, interfaccia IAMWMBufferPass
- Interfaccia IAMWMBufferPass Windows Media Format, metodo senotify
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9739952792fcfa49da1b5656db513c3af41a419c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399558"
---
# <a name="iamwmbufferpasssetnotify-method"></a>Metodo IAMWMBufferPass:: senotify

Il metodo **senotify** viene usato dalle applicazioni per fornire il filtro WM ASF Writer o [WM ASF Reader](wm-asf-reader-filter.md) con un puntatore all'interfaccia [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCallback* \[ in\]
</dt> <dd>

Puntatore all'interfaccia **IAMWMBufferPassCallback** dell'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Chiamare questo metodo prima di inserire il grafico del filtro nello stato di esecuzione.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 