---
description: Questo metodo restituisce un'interfaccia che fornisce l'accesso ai dati video.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: 'Metodo IVideoFrameNative:: GetData'
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
ms.openlocfilehash: c612d2d34e23b393921f83f7dbe9e189aa366b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966685"
---
# <a name="ivideoframenativegetdata-method"></a>Metodo IVideoFrameNative:: GetData

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

*riid* \[ in\]
</dt> <dd>

IID dell'interfaccia da recuperare.

</dd> <dt>

*PPV* \[ out\]
</dt> <dd>

Quando questo metodo viene restituito correttamente, contiene il puntatore a interfaccia richiesto nel parametro *riid* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se il completamento è riuscito. Restituisce E \_ nointerface se non è possibile trovare l'interfaccia richiesta.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



