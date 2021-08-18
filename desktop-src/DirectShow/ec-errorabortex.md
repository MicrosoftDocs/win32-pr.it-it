---
description: "EC_ERRORABORTEX: un'operazione è stata interrotta a causa di un errore."
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: EC_ERRORABORTEX (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18f0cb010e6ebf94f69cd8bbebfc7cdeea16d1d085069ad2f12fedb6fbf4a266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015979"
---
# <a name="ec_errorabortex"></a>ERRORE \_ ECABORTEX

Un'operazione è stata interrotta a causa di un errore.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**(HRESULT)** Codice di errore dell'operazione non riuscita.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**(BSTR)** Stringa che contiene informazioni aggiuntive sull'errore.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Il filtro [Windows origine multimediale](windows-media-source-filter.md) legacy invia questo evento. I nuovi filtri non devono inviare questo evento.

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

 

 




