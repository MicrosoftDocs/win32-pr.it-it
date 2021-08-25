---
description: È stato eseguito un comando di arresto del controllo di flusso.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69884ecc573b2bb775092529cb81e1b33a1514d4799af9f55c7bcebb5ebd2b24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928421"
---
# <a name="ec_stream_control_stopped"></a>CONTROLLO \_ DEL FLUSSO EC \_ \_ ARRESTATO

È stato eseguito un comando di arresto del controllo di flusso.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin che ha arrestato il flusso.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Valore definito dall'utente.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

I filtri inviano questo evento in risposta al [**metodo IAMStreamControl::StopAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) Il **metodo StopAt** specifica un tempo di riferimento per l'arresto dello streaming di un pin. Quando lo streaming si arresta, il filtro invia questo evento.

Il *parametro pSender* specifica il pin che esegue il comando stop. A seconda dell'implementazione, potrebbe non essere il pin che ha ricevuto la [**chiamata StopAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat)

Il *parametro dwCookie* viene specificato dall'applicazione nel [**metodo StopAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) Questo parametro consente all'applicazione di tenere traccia di più chiamate al metodo .

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

 

 




