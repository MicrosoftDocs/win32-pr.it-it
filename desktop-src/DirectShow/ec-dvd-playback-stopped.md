---
description: Indica che la riproduzione di DVD è stata arrestata. Questo evento viene inviato quando un titolo o un capitolo viene completato e lo strumento di navigazione DVD non trova altre istruzioni di diramazione per la riproduzione successiva. L'evento non viene inviato quando l'applicazione arresta la riproduzione.
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: EC_DVD_PLAYBACK_STOPPED (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_STOPPED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 7a5f0b1b66e9d78309e33981910da467757a2b606b967cee5b78e86c4cc0049b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820457"
---
# <a name="ec_dvd_playback_stopped"></a>RIPRODUZIONE \_ DI DVD EC \_ \_ ARRESTATA

Indica che la riproduzione di DVD è stata arrestata. Questo evento viene inviato quando un titolo o un capitolo viene completato e lo strumento di navigazione [DVD](dvd-navigator-filter.md) non trova altre istruzioni di diramazione per la riproduzione successiva. L'evento non viene inviato quando l'applicazione arresta la riproduzione.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Membro dell'enumerazione [**DVD \_ PB \_ STOPPED,**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) che indica il motivo per cui la riproduzione è stata arrestata.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento viene generato in tutti i domini.

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

 

 




