---
description: Un provider di rete è una DLL che consente al sistema operativo Windows di interagire con altri tipi di reti, ad esempio Novell. Si tratta di un client del driver WNet di Windows.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: API provider di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315864"
---
# <a name="network-provider-api"></a>API provider di rete

Un provider di rete è una DLL che consente al sistema operativo Windows di interagire con altri tipi di reti, ad esempio Novell. Si tratta di un client del driver WNet di Windows. Un provider di rete implementa azioni specifiche della rete, ad esempio la creazione di una connessione, ed espone un'interfaccia comune a Windows. Questa interfaccia è chiamata API del provider di rete ed è costituita da funzioni implementate dal provider di rete. È possibile creare una DLL del provider di rete per supportare nuovi protocolli di rete.

Poiché ogni rete espone un'interfaccia comune tramite il provider, Windows può interagire con diversi tipi di reti senza conoscere i dettagli di implementazione specifici della rete.

Il [*router multi-provider*](../secgloss/m-gly.md) (MPR) gestisce la comunicazione con tutti i diversi provider di rete del sistema e presenta una rete integrata all'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider di rete](network-providers.md)
</dt> <dt>

[Gestione credenziali](credential-manager.md)
</dt> <dt>

[Router per più provider](multiple-provider-router.md)
</dt> <dt>

[Funzioni implementate dai provider di rete](functions-implemented-by-network-providers.md)
</dt> <dt>

[API di gestione delle credenziali](credential-management-api.md)
</dt> <dt>

[API di notifica della connessione](connection-notification-api.md)
</dt> </dl>

 

 
