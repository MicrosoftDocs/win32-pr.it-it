---
description: Il provider del registro di sistema tenta di inviare una notifica per ogni evento che si verifica.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Ricezione degli eventi del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f0da8c039f83e3d4eb1f51d6b6707d0edd6b3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049761"
---
# <a name="receiving-registry-events"></a>Ricezione degli eventi del registro di sistema

Il provider del registro di sistema tenta di inviare una notifica per ogni evento che si verifica. Tuttavia, il provider del registro di sistema non garantisce che il consumer riceverà uno o tutti gli eventi. L'eccezione è che il provider del registro di sistema garantisce che un consumer riceva una notifica per ogni registrazione degli eventi.

Si supponga, ad esempio, che un consumer registri per due eventi di modifica della struttura ad albero, richiedendo notifiche per le istanze [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) . Ogni registrazione ha lo stesso valore hive (sottoalbero), ma un valore RootPath diverso. Se le chiavi di entrambi i percorsi cambiano più volte, il provider del registro di sistema garantisce che il consumer riceva una notifica per ogni percorso. A seconda del tempo di risposta del registro di sistema e del provider del registro di sistema, il consumer può ricevere il numero di notifiche che si sono verificate in presenza di eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione per eventi registro di sistema](registering-for-system-registry-events.md)
</dt> </dl>

 

 
