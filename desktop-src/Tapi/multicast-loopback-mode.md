---
description: L' \_ \_ enumerazione modalità loopback multicast descrive la modalità loopback multicast.
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: Enumerazione MULTICAST_LOOPBACK_MODE (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a15505efcd1a9e399866b104da0582ccf846689
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333967"
---
# <a name="multicast_loopback_mode-enumeration"></a>\_ \_ Enumerazione modalità loopback multicast

\[**Multicast \_ La \_ modalità loopback** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L' **enumerazione \_ \_ modalità loopback multicast** descrive la modalità loopback multicast.

## <a name="syntax"></a>Sintassi


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ nessun \_ loopback**
</dt> <dd>

Il loopback multicast è disabilitato. Ciò significa che due applicazioni nello stesso computer che si uniscono allo stesso gruppo multicast possono ottenere i pacchetti dell'altro.

</dd> <dt>

<span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**\_loopback completo di mm \_**
</dt> <dd>

Viene anche eseguito il loop di tutti i pacchetti inviati. Questa modalità è utile solo per i test.

</dd> <dt>

<span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**\_loopback selettivo mm \_**
</dt> <dd>

Il loopback selettivo è abilitato. Ciò significa che più applicazioni in un computer possono partecipare allo stesso gruppo multicast senza confusione. I pacchetti vengono riprodotti in ciclo dallo stack e ogni sessione RTP è responsabile del filtraggio dei pacchetti indesiderati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMulticastControl:: Get \_ LoopbackMode**](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[**IMulticastControl::p UT \_ LoopbackMode**](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 




