---
description: Un filtro richiede il riavvio del grafo.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fae3426048229c19b1d35a061d67d3d1d0a3149a8f820e891987c88405b76f7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820143"
---
# <a name="ec_need_restart"></a>EC \_ NEED \_ RESTART

Un filtro richiede il riavvio del grafo.

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

Il gestore del grafico del filtro sospende e riavvia il grafico. Non passa l'evento all'applicazione.

## <a name="remarks"></a>Commenti

Se un filtro rifiuta un campione nel mezzo di un flusso, il pin upstream interromperà la distribuzione dei campioni. Il filtro può riavviare il flusso inviando questo evento. Ad esempio, il renderer audio potrebbe perdere l'accesso al dispositivo audio, perché una finestra video ha perso lo stato attivo. A questo punto, il renderer audio inizia a rifiutare i campioni. Quando recupera l'accesso al dispositivo audio, invia questo evento per riavviare il flusso audio.

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

 

 




