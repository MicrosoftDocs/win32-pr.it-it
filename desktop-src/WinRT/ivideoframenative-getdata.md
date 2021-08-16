---
description: Questo metodo restituisce un'interfaccia che fornisce l'accesso ai dati video.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: Metodo IVideoFrameNative::GetData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: 832b2e300887699b926362ce9cbfc6f334c181805bacb3546532920c684251d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993771"
---
# <a name="ivideoframenativegetdata-method"></a>Metodo IVideoFrameNative::GetData

Questo metodo restituisce un'interfaccia che fornisce l'accesso ai dati video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* \[ Pollici\]
</dt> <dd>

IID dell'interfaccia da recuperare.

</dd> <dt>

*ppv* \[ Cambio\]
</dt> <dd>

Quando questo metodo viene restituito correttamente, contiene il puntatore a interfaccia richiesto nel *parametro riid.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK al completamento corretto. Restituisce E NOINTERFACE se non è possibile \_ trovare l'interfaccia richiesta.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



