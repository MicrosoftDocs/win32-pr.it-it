---
description: Segnala l'ora corrente, in \_ \_ formato di timecode HMSF DVD, rispetto all'inizio del titolo. Questo evento viene generato all'inizio di ogni VOBU, che si verifica ogni 0,4 e 1,0 secondi.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (Dvdevcode. h)
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
ms.openlocfilehash: 36306b95682e62ffebf8fb819dcc4b7c5185493c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325186"
---
# <a name="ec_dvd_current_hmsf_time"></a>\_ \_ \_ ora HMSF corrente del DVD EC \_

Segnala l'ora corrente, in formato di [**\_ \_ timecode HMSF DVD**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) , rispetto all'inizio del titolo. Questo evento viene generato all'inizio di ogni VOBU, che si verifica ogni 0,4 e 1,0 secondi.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore ULONG che contiene la struttura del \_ timecode HMSF DVD \_ . Assegnare lParam1 a una variabile ULONG, quindi eseguire il cast della variabile in \_ un \_ timecode DVD HMSF per accedere ai valori.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valore ULONG contenente un'Unione di [**flag del \_ timecode \_ del DVD**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).

</dd> </dl>

## <a name="remarks"></a>Commenti

Il \_ formato del timecode DVD HMSF \_ è destinato a sostituire il vecchio formato BCD restituito negli eventi dell' \_ ora corrente del DVD EC \_ \_ . I timecode HMSF sono più facili da usare. Per fare in modo che lo strumento di navigazione invii gli \_ \_ eventi del \_ tempo HMSF corrente del DVD EC \_ anziché \_ gli eventi dell'ora corrente del DVD EC \_ \_ , un'applicazione deve chiamare `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` . Quando questo flag è impostato, lo strumento di spostamento prevede anche che tutti i parametri di tempo nei metodi [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) vengano passati come \_ timecode HMSF del DVD \_ .

Questo evento viene generato nei domini del titolo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdevcode. h (include dshow. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> <dt>

[Codici di notifica degli eventi DVD](dvd-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




