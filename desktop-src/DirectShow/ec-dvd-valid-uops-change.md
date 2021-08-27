---
description: Segnala che il set disponibile di metodi di interfaccia IDvdControl2 è stato modificato.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: fafdbb5443a32a8029ad73d92a2b23c5f05c96d5dfc32375fd05e6d4502484a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051811"
---
# <a name="ec_dvd_valid_uops_change"></a>EC \_ DVD \_ VALID \_ UOPS \_ CHANGE

Segnala che il set disponibile di [**metodi di interfaccia IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) è stato modificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**Valore DWORD** che contiene una combinazione di zero o più flag [**dell'enumerazione VALID \_ UOP \_ FLAG.**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) I bit indicano quali [**comandi IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) sono stati disabilitati in modo esplicito dal disco DVD.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento indica solo le operazioni disabilitate in modo esplicito dal contenuto del disco DVD. Non garantisce che sia valido chiamare metodi che non sono disabilitati. Ad esempio, se non sono presenti pulsanti, il [**metodo IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) non funzionerà, anche se il metodo non è disabilitato in modo esplicito.

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

 

 




