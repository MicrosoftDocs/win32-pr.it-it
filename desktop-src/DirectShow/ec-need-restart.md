---
description: Un filtro richiede che il grafico venga riavviato.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651ae51b8dd8969a95b4f5e9d5093ec2e879f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324168"
---
# <a name="ec_need_restart"></a>EC \_ necessario \_ riavvio

Un filtro richiede che il grafico venga riavviato.

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

Il gestore del grafico del filtro sospende e riavvia il grafo. L'evento non viene passato all'applicazione.

## <a name="remarks"></a>Commenti

Se un filtro rifiuta un campione al centro di un flusso, il pin upstream interrompe la distribuzione degli esempi. Il filtro può riavviare il flusso inviando questo evento. Ad esempio, il renderer audio potrebbe perdere l'accesso al dispositivo audio, perché una finestra video ha perso lo stato attivo. A questo punto, il renderer audio inizia a rifiutare gli esempi. Quando viene riacquisito l'accesso al dispositivo audio, questo evento viene inviato per riavviare il flusso audio.

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

 

 




