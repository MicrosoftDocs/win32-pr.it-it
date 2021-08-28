---
description: Segnala che il numero di flusso dell'immagine secondaria corrente è stato modificato per il titolo principale.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 21549ec6427b82c6d229d2e3962689bc8879815429f3a68fd32d54283c30d6a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639771"
---
# <a name="ec_dvd_subpicture_stream_change"></a>EC \_ DVD \_ SUBPICTURE \_ STREAM \_ CHANGE

Segnala che il numero di flusso dell'immagine secondaria corrente è stato modificato per il titolo principale.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**Valore DWORD** che indica il nuovo numero di flusso dell'immagine secondaria dell'utente. I numeri di flusso delle immagini secondarie sono da 0 a 31. Flusso 0xFFFFFFFF indica che non è selezionato alcun flusso.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valore booleano che indica lo stato di on/off dell'immagine secondaria.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'immagine secondaria può cambiare automaticamente con un comando di navigazione creato su disco e tramite il controllo dell'applicazione [**usando IDvdControl2.**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)

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

 

 




