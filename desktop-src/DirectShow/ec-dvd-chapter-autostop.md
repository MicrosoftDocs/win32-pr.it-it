---
description: Indica che la riproduzione di DVD è stata interrotta in seguito a una chiamata al metodo IDvdControl2::P layChaptersAutoStop.
ms.assetid: ccafaf76-ec8c-4d67-9b29-565f3ed6593b
title: EC_DVD_CHAPTER_AUTOSTOP (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: a25c4ea621875403ad47ee6815b07b84572f939e4f2a6713d47aa53ba61f983e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652675"
---
# <a name="ec_dvd_chapter_autostop"></a>EC \_ DVD \_ CHAPTER \_ AUTOSTOP

Indica che la riproduzione del DVD è stata interrotta in seguito a una chiamata al metodo [**IDvdControl2::P layChaptersAutoStop.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop)

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Zero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento viene generato nel dominio del titolo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdevcode.h (includere Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> <dt>

[Codici di notifica degli eventi DVD](dvd-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




