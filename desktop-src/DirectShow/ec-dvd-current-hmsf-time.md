---
description: Segnala l'ora corrente, in \_ formato TIMECODE DVD HMSF, \_ rispetto all'inizio del titolo. Questo evento viene attivato all'inizio di ogni VOBU, che si verifica ogni 0,4-1,0 secondi.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 52a6eb077599b4fe6dfd89267974cb71c0c5a58a65d6c52307d77eb3e98201d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965811"
---
# <a name="ec_dvd_current_hmsf_time"></a>EC \_ DVD \_ CURRENT \_ HMSF \_ TIME

Segnala l'ora corrente, in [**\_ formato \_ TIMECODE DVD HMSF,**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) rispetto all'inizio del titolo. Questo evento viene attivato all'inizio di ogni VOBU, che si verifica ogni 0,4-1,0 secondi.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore ULONG che contiene la struttura \_ TIMECODE HMSF \_ del DVD. Assegnare lParam1 a una variabile ULONG e quindi eseguire il cast di tale variabile a un DVD \_ HMSF \_ TIMECODE per accedere ai relativi valori.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valore ULONG contenente un'unione di [**DVD \_ TIMECODE \_ FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).

</dd> </dl>

## <a name="remarks"></a>Commenti

Il formato TIMECODE del DVD HMSF è progettato per sostituire il vecchio formato BCD restituito negli eventi \_ \_ EC DVD CURRENT \_ \_ \_ TIME. I timecode HMSF sono più facili da usare. Per fare in modo che lo Strumento di navigazione invii eventi \_ EC DVD \_ CURRENT \_ HMSF TIME anziché EC DVD CURRENT \_ \_ \_ \_ TIME, `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` un'applicazione deve chiamare . Quando questo flag è impostato, lo strumento di navigazione prevede anche che tutti i parametri temporali nei metodi [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) siano passati come \_ \_ TIMECODE DVD HMSF.

Questo evento viene generato nei domini dei titoli.

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

 

 




