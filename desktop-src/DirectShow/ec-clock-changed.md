---
description: L'orologio di riferimento è stato modificato.
ms.assetid: f6de9e74-85fa-4f36-9d7d-3d95f2dbf873
title: EC_CLOCK_CHANGED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760c947c74a88f9c37ba75ffb55c49e5581c370ef4cc153aee8ebf377bf29246
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965961"
---
# <a name="ec_clock_changed"></a>EC \_ CLOCK \_ MODIFICATO

L'orologio di riferimento è stato modificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Zero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Il gestore del grafico filtri invia questo evento quando viene chiamato il metodo [**IMediaFilter::SetSyncSource.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource)

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

 

 




