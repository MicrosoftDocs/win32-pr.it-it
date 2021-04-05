---
title: Metodi di sicurezza
description: Microsoft RPC supporta due metodi diversi per aggiungere sicurezza all'applicazione distribuita.
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c4d052301ac1100d84cf18dc63e1540ed34b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045167"
---
# <a name="security-methods"></a>Metodi di sicurezza

Microsoft RPC supporta due metodi diversi per aggiungere sicurezza all'applicazione distribuita. Il primo metodo consiste nell'utilizzare l'interfaccia SSPI (Security Support Provider Interface), a cui è possibile accedere utilizzando le funzioni RPC. In generale, è preferibile usare questo metodo. SSPI fornisce le funzionalità di autenticazione più flessibili e indipendenti dalla rete.

Il secondo metodo consiste nell'utilizzare le funzionalità di sicurezza incorporate nei protocolli di trasporto di sistema. Il metodo di sicurezza a livello di trasporto non è il metodo preferito. L'uso di SSPI è consigliato perché funziona su tutti i trasporti, su più piattaforme e fornisce livelli elevati di sicurezza, inclusa la privacy.

In questa sezione vengono fornite panoramiche su SSPI e sulla sicurezza a livello di trasporto negli argomenti seguenti:

-   [Security Support Provider Interface (SSPI)](security-support-provider-interface-sspi-.md)
-   [Sicurezza del trasporto](transport-security.md)

 

 




