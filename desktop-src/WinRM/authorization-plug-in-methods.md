---
title: Metodi plug-in di autorizzazione
description: Tutti i punti di ingresso del plug-in di autorizzazione hanno un meccanismo di callback per segnalare l'esito positivo o negativo della chiamata. Alcuni meccanismi di callback vengono chiamati più volte fino a quando non vengono restituiti tutti i risultati.
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9253267b87a30c5cc2781440b0ecd430f244e90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298311"
---
# <a name="authorization-plug-in-methods"></a>Metodi plug-in di autorizzazione

Tutti i punti di ingresso del plug-in di autorizzazione hanno un meccanismo di callback per segnalare l'esito positivo o negativo della chiamata. Alcuni meccanismi di callback vengono chiamati più volte fino a quando non vengono restituiti tutti i risultati.

Nella tabella seguente viene fornita una panoramica dei metodi di callback di autorizzazione.



| Metodo                                                                           | Descrizione                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | Segnala un'operazione utente riuscita o non riuscita.                |
| [**WSManPluginAuthzQueryQuotaComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | Segnala i dettagli della quota rilevanti per l'utente specificato.      |
| [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | Segnala un'autorizzazione di connessione utente riuscita o non riuscita. |



 

 

 




