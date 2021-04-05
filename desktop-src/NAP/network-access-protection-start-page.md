---
title: Protezione accesso alla rete
description: Nota la piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10, protezione accesso alla rete (NAP) è un set di componenti del sistema operativo che forniscono una piattaforma per l'accesso protetto alle reti private.
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Protezione accesso alla rete
- Protezione accesso alla rete, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b99348428a867be5bf846fd40b030b844460cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709802"
---
# <a name="network-access-protection"></a>Protezione accesso alla rete

## <a name="purpose"></a>Scopo

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Protezione accesso alla rete (NAP) è un set di componenti del sistema operativo che forniscono una piattaforma per l'accesso protetto alle reti private. La piattaforma NAP fornisce un modo integrato per valutare lo stato di integrità del sistema di un client di rete che tenta di connettersi a una rete o di comunicare in una rete e di limitare l'accesso del client di rete fino a quando non sono stati soddisfatti i requisiti dei criteri di integrità.

NAP è una piattaforma estendibile che fornisce un'infrastruttura e un set di API per l'aggiunta di componenti che archiviano, segnalano, convalidano e correggono lo stato di integrità del sistema di un computer. La piattaforma NAP non fornisce componenti per accumulare e valutare gli attributi dello stato di integrità di un computer. Altri componenti, noti come System Health Agent (SHAs) e convalida integrità sistema (SHV), forniscono la convalida dei criteri di rete e la conformità dei criteri di rete.

## <a name="where-applicable"></a>Se applicabile

NAP è progettato per essere estendibile. Può interagire con qualsiasi software fornitore che fornisce SHAs e SHV o che riconosce il set di API pubblicate. NAP consente di fornire una soluzione per gli scenari comuni seguenti:

-   Controllare l'integrità e lo stato dei computer portatili mobili.
-   Verificare l'integrità dei computer desktop.
-   Verificare la conformità e l'integrità dei computer in uffici remoti.
-   Determinare l'integrità dei portatili in visita.
-   Verificare la conformità e l'integrità dei computer domestici non gestiti.

## <a name="developer-audience"></a>Sviluppatori

L'API NAP è progettata per gli sviluppatori C/C++. Per i metodi di imposizione di protezione accesso alla rete, i programmatori devono conoscere i protocolli e le tecnologie di rete, ad esempio Remote Authentication Dial-in User Service (RADIUS), Dynamic Host Configuration Protocol (DHCP), reti private virtuali (VPN), lo standard IEEE 802.1 X per l'accesso cablato e wireless e l'Internet Protocol Security (IPsec).

## <a name="run-time-requirements"></a>Requisiti di runtime

La piattaforma NAP richiede server di infrastruttura NAP che eseguono Windows Server 2008 o versioni successive e client NAP che eseguono Windows XP con Service Pack 3 (SP3), Windows Vista o sistemi operativi successivi. Per informazioni specifiche sui sistemi operativi che supportano un particolare elemento di programmazione, vedere le sezioni requisiti delle API NAP nella documentazione di riferimento per NAP.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                         | Descrizione                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [Informazioni su NAP](about-nap.md)<br/>         | Informazioni generali sull'API NAP.<br/>                                     |
| [Uso di Protezione accesso alla rete](using-nap.md)<br/>         | Esempi di utilizzo per l'API NAP.<br/>                                            |
| [Riferimento NAP](nap-reference.md)<br/> | Documentazione per le interfacce NAP, le strutture e altri elementi di codice.<br/> |



 

 

 





