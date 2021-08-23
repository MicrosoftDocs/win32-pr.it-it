---
description: Specifica il timestamp per il passaggio dell'intervallo più recente.
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: EC_SCRUB_TIME (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d4d3cc09d286f6955dda30aeb77288b75e90e8c66777a5f9f16246507f64b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686091"
---
# <a name="ec_scrub_time"></a>EC \_ SCRUB \_ TIME

Specifica il timestamp per il passaggio dell'intervallo più recente.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) 32 bit inferiori del timestamp.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) 32 bit superiori del timestamp.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Il presentatore del filtro [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) invia questo messaggio all'EVR quando completa un passaggio del fotogramma.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> </dl>

 

 




