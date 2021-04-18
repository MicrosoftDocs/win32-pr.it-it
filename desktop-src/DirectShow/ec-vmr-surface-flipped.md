---
description: Inviato quando il relatore dell'allocatore VMR-7 ha chiamato il metodo di capovolgimento DirectDraw sulla superficie visualizzata. In questo modo, VMR mantiene la tabella DirectXVA delle superfici sincronizzate con la catena di capovolgimento di DirectDraw.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feafaa58f0cacdafde04591d494dbb9a9eb258e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329480"
---
# <a name="ec_vmr_surface_flipped"></a>\_superficie VMR \_ EC \_ capovolta

Inviato quando il relatore dell'allocatore VMR-7 ha chiamato il metodo di capovolgimento DirectDraw sulla superficie visualizzata. In questo modo, VMR mantiene la tabella DirectXVA delle superfici sincronizzate con la catena di capovolgimento di DirectDraw.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Codice di stato restituito dal metodo di capovolgimento DirectDraw.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Allocator-Presenter personalizzato per VMR-7 deve inviare questo evento. Questo evento non viene inviato alle applicazioni e non viene usato con Allocator-Presenter per VMR-9.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




