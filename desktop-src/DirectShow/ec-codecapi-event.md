---
description: "L' \\_ evento di evento CODEcapite EC \\_ viene inviato da un codificatore per segnalare un evento di codifica. Il client esegue la registrazione per l'evento del codificatore chiamando il metodo ICodecAPI:: RegisterForEvent."
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c24ece20a0c729b251c56b50b5b44fc9f7fa98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328463"
---
# <a name="ec_codecapi_event"></a>\_evento CODEcapite EC \_

L' \_ evento di evento CODEcapite EC \_ viene inviato da un codificatore per segnalare un evento di codifica. Il client esegue la registrazione per l'evento del codificatore chiamando il metodo [**ICodecAPI:: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Dati utente. Il valore di questo parametro è il puntatore specificato dal chiamante nel parametro *UserData* del metodo [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Puntatore ai dati dell'evento. Questi dati vengono allocati dal codificatore e devono essere liberati dall'applicazione mediante la funzione **CoTaskMemFree** . Il blocco di dati inizia con una struttura [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) ; eseguire il cast del parametro *lParam2* a un puntatore a questa struttura.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Nessuna azione predefinita.

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

 

 




