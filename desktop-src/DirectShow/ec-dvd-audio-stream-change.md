---
description: Segnala che il numero del flusso audio corrente è stato modificato per il titolo principale del DVD.
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: EC_DVD_AUDIO_STREAM_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_AUDIO_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2ad6015ef132a98d02dc207cb9d43b6324ea3a05c541f43e295e75d13b5bb7ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998131"
---
# <a name="ec_dvd_audio_stream_change"></a>MODIFICA DEL \_ FLUSSO AUDIO DI EC \_ DVD \_ \_

Segnala che il numero del flusso audio corrente è stato modificato per il titolo principale del DVD.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**Valore DWORD** che indica il nuovo numero di flusso audio dell'utente. I numeri di flusso audio sono da 0 a 7. La 0xFFFFFFFF di flusso indica che non è selezionato alcun flusso.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il flusso audio corrente può cambiare automaticamente con un comando di navigazione creato sul disco e tramite il controllo dell'applicazione tramite [**l'interfaccia IDvdControl2.**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)

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

 

 




