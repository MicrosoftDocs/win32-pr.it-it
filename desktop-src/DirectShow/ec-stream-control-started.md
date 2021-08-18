---
description: È stato eseguito un comando di avvio del controllo di flusso.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73af8d39c3dae0447600a23dcb00483f4e0da6b81bc7ba6ab4a7e8b5f7afa42d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997891"
---
# <a name="ec_stream_control_started"></a>CONTROLLO \_ DEL FLUSSO EC \_ \_ AVVIATO

È stato eseguito un comando di avvio del controllo di flusso.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin che ha avviato il flusso.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Valore definito dall'utente.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

I filtri inviano questo evento in risposta al [**metodo IAMStreamControl::StartAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) Questo metodo specifica un tempo di riferimento per l'inizio dello streaming di un pin. Quando lo streaming inizia, il filtro invia questo evento.

Il *parametro pSender* specifica il pin che esegue il comando start. A seconda dell'implementazione, potrebbe non essere il pin che ha ricevuto la [**chiamata StartAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat)

Il *parametro dwCookie* viene specificato dall'applicazione nel [**metodo StartAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) Questo parametro consente all'applicazione di tenere traccia di più chiamate al metodo .

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

 

 




