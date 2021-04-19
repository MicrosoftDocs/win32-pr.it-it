---
description: Segnala che il numero di pulsanti di menu DVD è stato modificato o che la selezione del pulsante è cambiata.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331109"
---
# <a name="ec_dvd_button_change"></a>\_ \_ modifica pulsante DVD \_ EC

Segnala che il numero di pulsanti di menu DVD è stato modificato o che la selezione del pulsante è cambiata.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore **DWORD** che indica il numero di pulsanti disponibili.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valore **DWORD** che indica il numero di pulsante attualmente selezionato. Il pulsante selezionato numero zero implica che non è selezionato alcun pulsante.

</dd> </dl>

## <a name="remarks"></a>Commenti

I numeri dei pulsanti sono compresi tra 1 e 36.

Il pulsante attualmente selezionato può essere modificato automaticamente con un comando di navigazione creato sul disco e tramite il controllo delle applicazioni tramite l'interfaccia [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .

Questo evento può segnalare qualsiasi numero di pulsanti disponibili. Questi numeri non sempre corrispondono ai numeri dei pulsanti usati per [**IDVDControl2:: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) perché tale metodo può attivare solo un subset di pulsanti.

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

 

 




