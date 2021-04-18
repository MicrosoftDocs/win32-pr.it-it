---
description: L'interfaccia IMulticastControl viene implementata da IPConf MSP ed è disponibile solo per gli oggetti chiamata multicast.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Interfaccia IMulticastControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98ad006ea41034d6d4da32359d1ecbcdd250ab6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331603"
---
# <a name="imulticastcontrol-interface"></a>Interfaccia IMulticastControl

\[**IMulticastControl** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **IMulticastControl** viene implementata da IPConf MSP ed è disponibile solo per gli oggetti chiamata multicast. Questa interfaccia espone i metodi che consentono la creazione e la manipolazione di terminali che possono comunicare tra client H323 e SDP. L'interfaccia **IMulticastControl** controlla la modalità loopback multicast.

In modalità di \_ \_ loopback senza loopback, il loopback multicast è disabilitato, ovvero due applicazioni nello stesso computer che si uniscono allo stesso gruppo multicast otterranno i pacchetti dell'altro. Questa modalità offre le prestazioni migliori se è presente sempre una sola applicazione che partecipa al gruppo multicast nel computer. MM \_ \_ la modalità di loopback non è la modalità predefinita.

La \_ \_ modalità loopback completa mm è efficace solo per i test. Viene anche eseguito il loop di tutti i pacchetti inviati. Questa operazione può essere usata per verificare se i dispositivi sono in funzione.

La \_ modalità loopback selettivo mm \_ viene utilizzata per consentire a più applicazioni in un computer di partecipare allo stesso gruppo multicast. I pacchetti vengono riprodotti in ciclo dallo stack e ogni sessione RTP è responsabile del filtraggio dei pacchetti indesiderati.

## <a name="members"></a>Membri

L'interfaccia **IMulticastControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMulticastControl** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IMulticastControl** dispone di questi metodi.



| Metodo                                                          | Descrizione                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [**ottenere \_ LoopbackMode**](imulticastcontrol-get-loopbackmode.md) | Ottiene la modalità di loopback multicast.<br/> |
| [**Inserisci \_ LoopbackMode**](imulticastcontrol-put-loopbackmode.md) | Imposta la modalità loopback multicast.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MSP IPConf](ipconf-msp.md)
</dt> </dl>

 

