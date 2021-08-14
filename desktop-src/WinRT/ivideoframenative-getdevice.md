---
description: Questo metodo restituisce un dispositivo associato ai dati video.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: Metodo IVideoFrameNative::GetDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: 7f204cc0d44690a2b80c8642d590ef38510cebedbc00332720ec51529fe34ad2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323110"
---
# <a name="ivideoframenativegetdevice-method"></a>Metodo IVideoFrameNative::GetDevice

Questo metodo restituisce un dispositivo associato ai dati video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* \[ Pollici\]
</dt> <dd>

IID del dispositivo da recuperare.

</dd> <dt>

*ppv* \[ Cambio\]
</dt> <dd>

Quando questo metodo viene restituito correttamente, contiene il puntatore di dispositivo richiesto nel *parametro riid.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK al completamento dell'operazione.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



