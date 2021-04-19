---
description: Segnala che il numero del flusso di sottoimmagine corrente è stato modificato per il titolo principale.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (Dvdevcode. h)
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
ms.openlocfilehash: c30ef0b27185b5300ac5cec877ed4e4b38685c12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326637"
---
# <a name="ec_dvd_subpicture_stream_change"></a>\_ \_ Modifica flusso di sottoimmagine DVD EC \_ \_

Segnala che il numero del flusso di sottoimmagine corrente è stato modificato per il titolo principale.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore **DWORD** che indica il nuovo numero di flusso di sottoimmagine utente. I numeri di flusso di immagini secondarie sono compresi tra 0 e 31. Il flusso 0xFFFFFFFF indica che non è selezionato alcun flusso.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valore booleano che indica lo stato on/off dell'immagine.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile modificare automaticamente la sottoimmagine con un comando di navigazione creato sul disco e tramite il controllo delle applicazioni tramite [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).

Questo evento viene generato in tutti i domini.

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

 

 




