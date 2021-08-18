---
title: Uso di Microsoft Locator
description: Microsoft Locator è il servizio dei nomi predefinito. La libreria di runtime RPC la usa per trovare i programmi server nei sistemi host del server.
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- REMOTE Procedure Call RPC , attività, con Microsoft Locator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64a5c54c09ee344ffdba46f9f44a546ab866557bc861b206868ad6d3992896b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010739"
---
# <a name="using-microsoft-locator"></a>Uso di Microsoft Locator

Microsoft Locator è il servizio dei nomi predefinito. La libreria di runtime RPC la usa per trovare i programmi server nei sistemi host del server.

**Nota**  Il localizzatore RPC Microsoft non è supportato in Windows Vista e nei sistemi operativi successivi.

Prima di Windows 2000, Microsoft Locator non forniva voci di servizio dei nomi permanenti. Tutte le voci nel servizio dei nomi sono state archiviate in una cache di memoria nel computer host del programma server. Il localizzatore ha usato un meccanismo di trasmissione per individuare la posizione dei server come richiesto dai client. Ogni volta che il sistema host viene arrestato, tutte le voci del servizio dei nomi sono state perse.

A partire dal rilascio di Windows 2000, Microsoft Locator supporta ora le voci del servizio dei nomi permanenti. A tale scopo, il sistema usa un servizio directory distribuito per archiviare le voci del servizio dei nomi. Questo meccanismo presenta diversi vantaggi:

-   **Persistenza.** I programmi server non sono più necessari per esportare le informazioni di associazione nel servizio dei nomi a ogni avvio. Il servizio dei nomi archivia ora le informazioni fino a quando il programma server nell'amministratore di rete non le rimuove in modo esplicito.
-   **Efficienza.** Eliminando la maggior parte delle trasmissioni per le voci del servizio dei nomi, il localizzatore riduce il traffico di rete. Trova anche le voci del servizio dei nomi più rapidamente.
-   **Interoperabilità tra domini.** I client sono ora in grado di effettuare richieste di servizio dei nomi in più domini.

Le versioni correnti di Microsoft Locator sono compatibili con le versioni precedenti. Ad esempio, un sistema host server che esegue il localizzatore fornito con Windows 2000 può funzionare correttamente in una rete che contiene sistemi host server che eseguono il localizzatore fornito con Windows NT 4.0.

Con il rilascio di Windows 2000, Microsoft Locator supporta ora le voci del servizio dei nomi per i gruppi di utenti. Offre anche la possibilità di creare profili utente.

Inoltre, la versione corrente di Microsoft Locator supporta l'uso di elenchi di controllo di accesso nelle voci del servizio dei nomi. Questa funzionalità migliora la sicurezza della rete.

Plug and Play supporto è ora incluso in Microsoft Locator. Pertanto, può gestire in modo trasparente gli eventi Plug and Play, ad esempio le modifiche al dominio. Per altre informazioni, vedere [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) e [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).

 

 




