---
description: Richiede un nuovo esempio di input dal filtro Enhanced Video Renderer (EVR).
ms.assetid: f1bf32ba-ecb7-435f-aefc-f60fdd355620
title: EC_SAMPLE_NEEDED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0058f8d0b7f8404a59f8c7e4fc5a4029c5ebaf4bc4f5c1b2678b1ed8c0f4f90c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686121"
---
# <a name="ec_sample_needed"></a>EC \_ SAMPLE \_ NEEDED

Richiede un nuovo esempio di input dal filtro [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR).

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificatore del flusso di input che richiede un nuovo input.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Il mixer per il filtro EVR invia questo messaggio quando è necessario un nuovo esempio di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> </dl>

 

 




