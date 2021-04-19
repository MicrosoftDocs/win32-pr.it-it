---
description: È stato applicato un comando di avvio del controllo di flusso.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984562fde9001de14067e5865d5583636b264852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326162"
---
# <a name="ec_stream_control_started"></a>\_controllo flusso \_ EC \_ avviato

È stato applicato un comando di avvio del controllo di flusso.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN che ha avviato il flusso.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Valore definito dall'utente.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

I filtri inviano questo evento in risposta al metodo [**IAMStreamControl:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) . Questo metodo specifica un'ora di riferimento per avviare lo streaming di un PIN. Quando il flusso inizia, il filtro Invia questo evento.

Il parametro *pSender* specifica il pin che esegue il comando di avvio. A seconda dell'implementazione, potrebbe non corrispondere al pin che ha ricevuto la chiamata [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .

Il parametro *dwCookie* viene specificato dall'applicazione nel metodo [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) . Questo parametro consente all'applicazione di tenere traccia di più chiamate al metodo.

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

 

 




