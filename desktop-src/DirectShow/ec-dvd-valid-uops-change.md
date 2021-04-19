---
description: Segnala che il set disponibile di metodi dell'interfaccia IDvdControl2 è stato modificato.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (Dvdevcode. h)
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
ms.openlocfilehash: 26ab0674b504fac3fe374247f47ca20496b22ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326629"
---
# <a name="ec_dvd_valid_uops_change"></a>\_ \_ \_ modifica UOPs valida DVD \_ EC

Segnala che il set disponibile di metodi dell'interfaccia [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) è stato modificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore **DWORD** che contiene una combinazione di zero o più flag dall'enumerazione [**valida \_ del \_ flag UOP**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) . I bit indicano quali comandi di [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) sono stati disabilitati in modo esplicito dal disco DVD.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento indica solo le operazioni che vengono disabilitate in modo esplicito dal contenuto del disco DVD. Non garantisce che sia valido chiamare metodi che non sono disabilitati. Se, ad esempio, non è presente alcun pulsante, il metodo [**IDVDControl2:: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) non funzionerà, anche se il metodo non è disabilitato in modo esplicito.

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

 

 




