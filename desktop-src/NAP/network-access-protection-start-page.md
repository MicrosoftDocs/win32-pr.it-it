---
title: Protezione accesso alla rete
description: Nota La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10 Protezione accesso alla rete è un set di componenti del sistema operativo che forniscono una piattaforma per l'accesso protetto alle reti private.
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Protezione accesso alla rete
- Protezione accesso alla rete, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1e5b5121566c3626ee7a9f2ba5d85efc1bf6cff17b412cd99874ae9b346780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939129"
---
# <a name="network-access-protection"></a>Protezione accesso alla rete

## <a name="purpose"></a>Scopo

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Protezione accesso alla rete è un set di componenti del sistema operativo che forniscono una piattaforma per l'accesso protetto alle reti private. La piattaforma protezione accesso alla rete offre un modo integrato per valutare lo stato di integrità del sistema di un client di rete che sta tentando di connettersi o comunicare in una rete e di limitare l'accesso del client di rete fino a quando non sono stati soddisfatti i requisiti dei criteri di integrità.

Protezione accesso alla rete è una piattaforma estendibile che fornisce un'infrastruttura e un set di API per l'aggiunta di componenti che archiviano, segnalano, convalidano e correggino lo stato di integrità del sistema di un computer. Di per sé, la piattaforma Protezione accesso alla rete non fornisce componenti per accumulare e valutare gli attributi dello stato di integrità di un computer. Altri componenti, noti come agenti di integrità del sistema e validator dell'integrità del sistema, forniscono la convalida dei criteri di rete e la conformità ai criteri di rete.

## <a name="where-applicable"></a>Se applicabile

Protezione accesso alla rete è progettato per essere estendibile. Può interagire con qualsiasi software del fornitore che fornisce SHA e SHV o che riconosce il set di API pubblicato. Protezione accesso alla rete offre una soluzione per gli scenari comuni seguenti:

-   Controllare l'integrità e lo stato dei portatili in roaming.
-   Verificare l'integrità dei computer desktop.
-   Verificare la conformità e l'integrità dei computer negli uffici remoti.
-   Determinare l'integrità dei portatili in visita.
-   Verificare la conformità e l'integrità dei computer domestici non gestiti.

## <a name="developer-audience"></a>Sviluppatori

L'API protezione accesso alla rete è progettata per gli sviluppatori C/C++. Per i metodi di imposizione di Protezione accesso alla rete, i programmatori devono avere familiarità con i protocolli e le tecnologie di rete, ad esempio RADIUS (Remote Authentication Dial-in User Service), Dynamic Host Configuration Protocol (DHCP), reti private virtuali (VPN), lo standard IEEE 802.1X per l'accesso cablato e wireless e internet protocol security (IPsec).

## <a name="run-time-requirements"></a>Requisiti di runtime

La piattaforma Protezione accesso alla rete richiede server dell'infrastruttura di Protezione accesso alla rete che eseguono Windows Server 2008 o versione successiva e client protezione accesso alla rete che eseguono Windows XP con Service Pack 3 (SP3), Windows Vista o sistemi operativi successivi. Per informazioni specifiche sui sistemi operativi che supportano un particolare elemento di programmazione, vedere le sezioni Requisiti delle API di Protezione accesso alla rete nella documentazione di riferimento di Protezione accesso alla rete.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                         | Descrizione                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [Informazioni su Protezione accesso alla rete](about-nap.md)<br/>         | Informazioni generali sull'API di Protezione accesso alla rete.<br/>                                     |
| [Uso di Protezione accesso alla rete](using-nap.md)<br/>         | Esempi di utilizzo per l'API protezione accesso alla rete.<br/>                                            |
| [Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)<br/> | Documentazione per interfacce, strutture e altri elementi di codice di Protezione accesso alla rete.<br/> |



 

 

 





