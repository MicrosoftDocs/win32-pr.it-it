---
description: Le dimensioni del video nativo sono state modificate.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da9fc430b8d36a61b90f567f082c7224765a702549d050f11555c8e55c387a86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792381"
---
# <a name="ec_video_size_changed"></a>DIMENSIONI \_ VIDEO \_ EC \_ MODIFICATE

Le dimensioni del video nativo sono state modificate.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Word di ordine basso specifica la nuova larghezza, in pixel. word di alto livello specifica la nuova altezza, in pixel.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

I renderer video possono inviare questo evento se rilevano una modifica nelle dimensioni del video nativo.

[Video Mixing Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7) e [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9) inviano questo evento in modalità finestra, ma non in modalità senza finestra o senza rendering. Per altre informazioni sulla modalità finestra nella macchina virtuale, vedere [Rendering video](video-rendering.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




