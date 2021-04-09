---
title: Uso di Microsoft Locator
description: Microsoft Locator è il servizio dei nomi predefinito. La libreria di runtime RPC la utilizza per trovare i programmi server nei sistemi host server.
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- RPC (Remote Procedure Call), attività, utilizzo di Microsoft Locator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236dce18b9286150581af925935222f3c9b3f862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856137"
---
# <a name="using-microsoft-locator"></a>Uso di Microsoft Locator

Microsoft Locator è il servizio dei nomi predefinito. La libreria di runtime RPC la utilizza per trovare i programmi server nei sistemi host server.

**Nota**    Microsoft RPC Locator non è supportato in Windows Vista e nei sistemi operativi successivi.

Prima di Windows 2000, Microsoft Locator non forniva voci del servizio di nome permanenti. Tutte le voci nel servizio nome sono state archiviate in una cache in memoria sul computer host del programma server. Il localizzatore ha utilizzato un meccanismo di trasmissione per individuare il percorso dei server richiesti dai client. Ogni volta che il sistema host si arresta, tutte le voci del servizio nome andranno perse.

A partire dal rilascio di Windows 2000, Microsoft Locator supporta ora le voci del servizio nome permanente. A tale scopo, il sistema usa un servizio di directory distribuito per archiviare le voci del servizio del nome. Questo meccanismo presenta diversi vantaggi:

-   **Persistenza.** I programmi server non sono più necessari per esportare le informazioni di binding nel servizio nome ogni volta che vengono avviate. Il servizio nome Archivia ora le informazioni finché il programma server nell'amministratore di rete non lo rimuove in modo esplicito.
-   **Efficienza.** Eliminando la maggior parte delle trasmissioni per le voci del servizio nomi, il localizzatore riduce il traffico di rete. Trova anche le voci del servizio nome più rapidamente.
-   **Interoperabilità tra domini.** I client sono ora in grado di effettuare richieste di servizio con nome tra più domini.

Le versioni correnti di Microsoft Locator sono compatibili con le versioni precedenti. Ad esempio, un sistema host server che esegue il localizzatore fornito con Windows 2000 può funzionare correttamente in una rete che contiene i sistemi host server che eseguono il localizzatore fornito con Windows NT 4,0.

Con il rilascio di Windows 2000, Microsoft Locator ora supporta le voci del servizio di denominazione per i gruppi di utenti. Offre inoltre la possibilità di creare profili utente.

Inoltre, la versione corrente di Microsoft Locator supporta l'utilizzo degli elenchi di controllo di accesso nelle voci del servizio di denominazione. Questa funzionalità migliora la sicurezza della rete.

Il supporto Plug and Play è ora incluso in Microsoft Locator. Pertanto, può gestire in modo trasparente Plug and Play eventi come le modifiche al dominio. Per ulteriori informazioni, vedere [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) e [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).

 

 




