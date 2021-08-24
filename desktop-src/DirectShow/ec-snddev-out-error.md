---
description: Si è verificato un errore del dispositivo in un filtro del renderer audio.
ms.assetid: 60e36476-f553-468d-a28d-351fdf4a02f1
title: EC_SNDDEV_OUT_ERROR (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefe6dbe57b26bf167a7fbc668010930bacffc321d42d2847ae6776696e009fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792411"
---
# <a name="ec_snddev_out_error"></a>ERRORE \_ EC SNDDEV \_ \_ OUT

Si è verificato un errore del dispositivo in un filtro del renderer audio.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore DWORD del tipo [**enumerato SNDDEV \_ ERR,**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) che indica la modalità di accesso al dispositivo quando si è verificato l'errore.

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

 

 




