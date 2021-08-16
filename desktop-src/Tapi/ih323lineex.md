---
description: L'interfaccia IH323LineEx viene implementata da H323 MSP ed è disponibile solo per gli oggetti indirizzo H.323. Questa interfaccia espone metodi che consentono la creazione e la manipolazione di terminali in grado di comunicare tra client H323 e SDP.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: Interfaccia IH323LineEx (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 856deae92568acd2eb9f9394e949dc2d5ea6a4bbde9c2c28f0b998c99098eef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013111"
---
# <a name="ih323lineex-interface"></a>Interfaccia IH323LineEx

\[**IH323LineEx** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

**L'interfaccia IH323LineEx** viene implementata da [H323 MSP](h323-msp.md) ed è disponibile solo per gli oggetti indirizzo H.323. Questa interfaccia espone metodi che consentono la creazione e la manipolazione di terminali in grado di comunicare tra client H323 e SDP.

> [!Note]  
> Tutti i metodi in questa interfaccia devono essere chiamati solo dopo la registrazione per le chiamate in ingresso su questo indirizzo.

 

## <a name="members"></a>Membri

**L'interfaccia IH323LineEx** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IH323LineEx** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IH323LineEx.**



| Metodo                                                                                 | Descrizione                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**SetAlias**](ih323lineex-setalias.md)                                               | Configura un alias H.323 predefinito per l'indirizzo.<br/>             |
| [**SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md) | Configura la ponderazione delle preferenze per le funzionalità predefinite.<br/> |
| [**SetExternalT120Address**](ih323lineex-setexternalt120address.md)                   | Configura un indirizzo T.120 esterno per lo scambio di dati.<br/>       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[H323 MSP](h323-msp.md)
</dt> </dl>

 

