---
title: Le chiamate remote al protocollo RPC SAM sono limitate solo agli amministratori locali
description: Il protocollo RPC SAM è limitato. Ciò significa che solo i membri del gruppo Administrator locale possono effettuare chiamate remote ai metodi in questo protocollo. Il comportamento del controller di dominio di Active Directory non è interessato.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee009e3f346c7e7a179a324ec68834999acd711934ab5c64a3cae1845372dbdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211336"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a>Le chiamate remote al protocollo RPC SAM sono limitate solo agli amministratori locali

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Il protocollo RPC SAM è limitato. Ciò significa che solo i membri del gruppo Administrator locale possono effettuare chiamate remote ai metodi in questo protocollo. Il comportamento del controller di dominio di Active Directory non è interessato.

## <a name="mitigations"></a>Soluzioni di prevenzione

Assicurarsi che gli utenti giuste siano impostati come amministratori nel PC. L'ACL usato per il controllo di accesso è configurabile tramite Criteri di gruppo.

 

 




