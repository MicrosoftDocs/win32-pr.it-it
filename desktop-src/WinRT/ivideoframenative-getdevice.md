---
description: Questo metodo restituisce un dispositivo associato ai dati video.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: 'Metodo IVideoFrameNative:: GetDevice'
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
ms.openlocfilehash: d012ae79b1cb2c83e916dc74113cc3d0560da4c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401657"
---
# <a name="ivideoframenativegetdevice-method"></a>Metodo IVideoFrameNative:: GetDevice

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

*riid* \[ in\]
</dt> <dd>

IID del dispositivo da recuperare.

</dd> <dt>

*PPV* \[ out\]
</dt> <dd>

Quando questo metodo viene restituito correttamente, contiene il puntatore del dispositivo richiesto nel parametro *riid* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se il completamento è riuscito.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



