---
description: Si è verificato un errore del dispositivo in un filtro di acquisizione audio.
ms.assetid: 13f8641b-7881-4f1c-816c-77c140e48ed4
title: EC_SNDDEV_IN_ERROR (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f9b95055483b1bda812179f1a1bf132d12de7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332054"
---
# <a name="ec_snddev_in_error"></a>EC \_ SNDDEV \_ in \_ errore

Si è verificato un errore del dispositivo in un filtro di acquisizione audio.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore DWORD dal tipo enumerato [**SNDDEV \_ Err**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) , che indica il modo in cui è stato eseguito l'accesso al dispositivo quando si è verificato l'errore.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valore DWORD che indica l'errore restituito dalla chiamata al dispositivo audio.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Nessuna.

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

 

 




