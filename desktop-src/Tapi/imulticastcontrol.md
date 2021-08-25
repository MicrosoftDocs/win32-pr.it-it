---
description: L'interfaccia IMulticastControl viene implementata da IPConf MSP e disponibile solo per gli oggetti chiamata multicast.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Interfaccia IMulticastControl (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7469ca26a49bc25b36ae87727a1fdcf324bcf54e8a253805ed56f252c7f062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905951"
---
# <a name="imulticastcontrol-interface"></a>Interfaccia IMulticastControl

\[**IMulticastControl** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

**L'interfaccia IMulticastControl** viene implementata da IPConf MSP e disponibile solo per gli oggetti chiamata multicast. Questa interfaccia espone metodi che consentono la creazione e la manipolazione di terminali in grado di comunicare tra client H323 e SDP. **L'interfaccia IMulticastControl** controlla la modalità loopback multicast.

Nella modalità MM NO LOOPBACK il loopback multicast è disabilitato, ovvero due applicazioni nello stesso computer che si uniscono allo stesso gruppo multicast otterranno i pacchetti \_ \_ reciproci. Questa modalità consente di ottenere prestazioni ottimali se nel computer è sempre presente una sola applicazione che si unisce al gruppo multicast. Mm \_ NO \_ LOOPBACK è la modalità predefinita.

La modalità \_ LOOPBACK MM FULL \_ è buona solo per i test. Anche tutti i pacchetti inviati vengono trasmessi a ciclo continuo. Può essere usato per verificare se i dispositivi funzionano.

La modalità \_ \_ LOOPBACK SELETTIVA MM viene usata per consentire a più applicazioni in un computer di aggiungersi allo stesso gruppo multicast. I pacchetti vengono inviati a ciclo continuo dallo stack e ogni sessione RTP è responsabile del filtraggio dei pacchetti indesiderati.

## <a name="members"></a>Membri

**L'interfaccia IMulticastControl** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMulticastControl** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IMulticastControl** include questi metodi.



| Metodo                                                          | Descrizione                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [**get \_ LoopbackMode**](imulticastcontrol-get-loopbackmode.md) | Ottiene la modalità loopback multicast.<br/> |
| [**put \_ LoopbackMode**](imulticastcontrol-put-loopbackmode.md) | Imposta la modalità di loopback multicast.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> </dl>

 

