---
description: Si è verificato un errore del dispositivo in un filtro di acquisizione audio.
ms.assetid: 13f8641b-7881-4f1c-816c-77c140e48ed4
title: EC_SNDDEV_IN_ERROR (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bfc65b751010288ed37fc1596e020887e6ea901c451dcdac729fe05ea33f93a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102811"
---
# <a name="ec_snddev_in_error"></a>EC \_ SNDDEV \_ IN \_ ERRORE

Si è verificato un errore del dispositivo in un filtro di acquisizione audio.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore DWORD del [**tipo enumerato SNDDEV \_ ERR,**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) che indica come è stato eseguito l'accesso al dispositivo quando si è verificato l'errore.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valore DWORD che indica l'errore restituito dalla chiamata del dispositivo audio.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Nessuno.

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

 

 




