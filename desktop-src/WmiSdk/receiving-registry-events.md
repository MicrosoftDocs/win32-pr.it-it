---
description: Il provider del Registro di sistema tenta di inviare una notifica per ogni evento che si verifica.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Ricezione di eventi del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6f3c8f39be30beeb64e7c8d8ff7f1bacfba8a47b7f4bd0c70e7cf638bf726e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817457"
---
# <a name="receiving-registry-events"></a>Ricezione di eventi del Registro di sistema

Il provider del Registro di sistema tenta di inviare una notifica per ogni evento che si verifica. Tuttavia, il provider del Registro di sistema non garantisce che il consumer riceverà uno o tutti gli eventi. L'eccezione è che il provider del Registro di sistema garantisce che un consumer riceva una notifica per ogni registrazione dell'evento.

Si supponga, ad esempio, che un consumer si registri per due eventi di modifica dell'albero, richiedendo una notifica [**per le istanze di RegistryTreeChangeEvent.**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) Ogni registrazione ha lo stesso valore Hive (sottoalbero), ma un valore RootPath diverso. Se le chiavi in entrambi i percorsi cambiano più volte, il provider del Registro di sistema garantisce che il consumer riceverà una notifica per ogni percorso. A seconda del tempo di risposta del Registro di sistema e del provider del Registro di sistema, il consumer può ricevere tutte le notifiche quante sono le occorrenze di eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione per gli eventi del Registro di sistema](registering-for-system-registry-events.md)
</dt> </dl>

 

 
