---
description: Segnala che il numero di pulsanti del menu DVD è stato modificato o che la selezione del pulsante è stata modificata.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (Dvdevcode.h)
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
ms.openlocfilehash: 61e74a967df18d5ba105eda1609a72c0db9770868bbd967c7a90f5e920dc954d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652747"
---
# <a name="ec_dvd_button_change"></a>EC \_ DVD \_ BUTTON \_ CHANGE

Segnala che il numero di pulsanti del menu DVD è stato modificato o che la selezione del pulsante è stata modificata.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**Valore DWORD** che indica il numero di pulsanti disponibili.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**Valore DWORD** che indica il numero di pulsante attualmente selezionato. Il numero zero del pulsante selezionato implica che non è selezionato alcun pulsante.

</dd> </dl>

## <a name="remarks"></a>Commenti

I numeri dei pulsanti sono compreso tra 1 e 36.

Il pulsante attualmente selezionato può cambiare automaticamente con un comando di navigazione creato sul disco e tramite il controllo dell'applicazione tramite [**l'interfaccia IDvdControl2.**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)

Questo evento può segnalare uno qualsiasi dei numeri di pulsante disponibili. Questi numeri non corrispondono sempre ai numeri di pulsante usati per [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) perché tale metodo può attivare solo un subset di pulsanti.

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

 

 




