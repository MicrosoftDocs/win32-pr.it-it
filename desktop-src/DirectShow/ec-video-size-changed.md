---
description: Le dimensioni del video nativo sono state modificate.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328334"
---
# <a name="ec_video_size_changed"></a>\_dimensioni del video EC \_ \_ modificate

Le dimensioni del video nativo sono state modificate.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) WORD di ordine inferiore specifica la nuova larghezza, in pixel; WORD di ordine superiore specifica la nuova altezza, in pixel.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

I renderer video possono inviare questo evento se rilevano una modifica nelle dimensioni del video nativo.

Il [video di mixaggio 7](video-mixing-renderer-filter-7.md) (VMR-7) e il [renderer video mixing 9](video-mixing-renderer-filter-9.md) (VMR-9) inviano questo evento in modalità finestra, ma non in modalità senza finestra o in modalità di rendering. Per ulteriori informazioni sulla modalità finestra in VMR, vedere rendering del [video](video-rendering.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




