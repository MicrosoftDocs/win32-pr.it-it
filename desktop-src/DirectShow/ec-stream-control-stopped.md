---
description: È stato applicato un comando di interruzione del controllo del flusso.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c5488ba400d90623955c3e9adcba0dde07e04a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327115"
---
# <a name="ec_stream_control_stopped"></a>\_controllo flusso \_ EC \_ arrestato

È stato applicato un comando di interruzione del controllo del flusso.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN che ha interrotto il flusso.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Valore definito dall'utente.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

I filtri inviano questo evento in risposta al metodo [**IAMStreamControl:: STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) . Il metodo **STOPAT** specifica un'ora di riferimento per l'arresto del flusso da parte di un PIN. Quando il flusso si interrompe, il filtro Invia questo evento.

Il parametro *pSender* specifica il pin che esegue il comando stop. A seconda dell'implementazione, potrebbe non corrispondere al pin che ha ricevuto la chiamata [**STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .

Il parametro *dwCookie* viene specificato dall'applicazione nel metodo [**STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) . Questo parametro consente all'applicazione di tenere traccia di più chiamate al metodo.

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

 

 




