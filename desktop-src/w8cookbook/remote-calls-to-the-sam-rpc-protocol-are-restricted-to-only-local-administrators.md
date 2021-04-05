---
title: Le chiamate remote al protocollo RPC SAM sono limitate solo agli amministratori locali
description: Il protocollo RPC SAM viene limitato. Ciò significa che solo i membri del gruppo Administrators locale possono effettuare chiamate remote ai metodi in questo protocollo. Active Directory comportamento del controller di dominio non è interessato.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 669c20503551b0a380372524b898559dff472f2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116933"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a>Le chiamate remote al protocollo RPC SAM sono limitate solo agli amministratori locali

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Il protocollo RPC SAM viene limitato. Ciò significa che solo i membri del gruppo Administrators locale possono effettuare chiamate remote ai metodi in questo protocollo. Active Directory comportamento del controller di dominio non è interessato.

## <a name="mitigations"></a>Soluzioni di prevenzione

Assicurarsi che gli utenti corretti siano impostati come amministratori nel computer. L'ACL usato per il controllo di accesso è configurabile tramite criteri di gruppo.

 

 




