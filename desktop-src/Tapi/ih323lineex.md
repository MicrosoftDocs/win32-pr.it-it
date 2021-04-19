---
description: L'interfaccia IH323LineEx viene implementata da H323 MSP ed è disponibile solo per gli oggetti Address H. 323. Questa interfaccia espone i metodi che consentono la creazione e la manipolazione di terminali che possono comunicare tra client H323 e SDP.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: Interfaccia IH323LineEx (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41888b16f645a3af1eefd9df61623cb28684bfdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329951"
---
# <a name="ih323lineex-interface"></a>Interfaccia IH323LineEx

\[**IH323LineEx** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **IH323LineEx** viene implementata da [H323 msp](h323-msp.md) ed è disponibile solo per gli oggetti Address H. 323. Questa interfaccia espone i metodi che consentono la creazione e la manipolazione di terminali che possono comunicare tra client H323 e SDP.

> [!Note]  
> Tutti i metodi in questa interfaccia devono essere chiamati solo dopo la registrazione per le chiamate in ingresso su questo indirizzo.

 

## <a name="members"></a>Membri

L'interfaccia **IH323LineEx** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IH323LineEx** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IH323LineEx** dispone di questi metodi.



| Metodo                                                                                 | Descrizione                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**Alias**](ih323lineex-setalias.md)                                               | Configura un alias H. 323 predefinito per l'indirizzo.<br/>             |
| [**SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md) | Configura la ponderazione delle preferenze per le funzionalità predefinite.<br/> |
| [**SetExternalT120Address**](ih323lineex-setexternalt120address.md)                   | Configura un indirizzo T. 120 esterno per lo scambio di dati.<br/>       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MSP H323](h323-msp.md)
</dt> </dl>

 

