---
description: Inviato quando l'allocatore presenter di VMR-7 ha chiamato il metodo Flip DirectDraw sulla superficie visualizzata. Ciò consente al VMR di mantenere la tabella directXVA delle superfici sincronizzata con la catena di capovolgimento di DirectDraw.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c352af01ee31728b41aa276d14ca64b7c3fa6770bb4c9328a8c4ee5e91bb07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043351"
---
# <a name="ec_vmr_surface_flipped"></a>SUPERFICIE \_ VMR \_ EC \_ CAPOVOLTA

Inviato quando l'allocatore presenter di VMR-7 ha chiamato il metodo Flip DirectDraw sulla superficie visualizzata. Ciò consente al VMR di mantenere la tabella directXVA delle superfici sincronizzata con la catena di capovolgimento di DirectDraw.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Codice di stato restituito dal metodo DirectDraw Flip.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli allocator-presenter personalizzati per VMR-7 devono inviare questo evento. Questo evento non viene inoltrato alle applicazioni e non viene usato con allocator-presenter per vmr-9.

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

 

 




