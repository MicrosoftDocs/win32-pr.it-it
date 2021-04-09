---
description: Questo metodo restituisce un'interfaccia che consente di accedere ai dati audio.
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: 'Metodo IAudioFrameNative:: GetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: eb61bce5132c2029b6f53fdd1159ca50984ba936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129238"
---
# <a name="iaudioframenativegetdata-method"></a>Metodo IAudioFrameNative:: GetData

Questo metodo restituisce un'interfaccia che consente di accedere ai dati audio.

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

Tipo: **REFIID**

IID dell'interfaccia da recuperare.

</dd> <dt>

*PPV* \[ out\]
</dt> <dd>

Tipo: **LPVOID \** _

Quando questo metodo viene restituito correttamente, contiene il puntatore a interfaccia richiesto nel parametro _riid *.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce \_ OK se il completamento è riuscito. Restituisce E \_ nointerface se non è possibile trovare l'interfaccia richiesta.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



