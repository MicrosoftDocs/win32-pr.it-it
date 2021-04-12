---
description: L'elenco seguente contiene i membri CMSPCAllBase.
ms.assetid: a3193639-e0c4-4851-a879-551eca8023f9
title: Membri di CMSPCallBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ddae67d85a64a5a443727b3950054957c7f24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231688"
---
# <a name="cmspcallbase-members"></a>Membri di CMSPCallBase



| Tipo di membro                   | Nome             | Descrizione                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IUnknown                      | \*\_pFTM m        | Puntatore al marshaller a thread libero.                                                                                                                                                                                                                                                                                                          |
| CMSPAddress\*                 | \*\_pMSPAddress m | Puntatore all'oggetto indirizzo MSP. Viene usato per ottenere i terminali predefiniti se l'applicazione non seleziona alcuna. Contiene anche un refcount (tramite [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), non AddRef), in modo che l'indirizzo aggregato non venga tolto mentre la chiamata è ancora attiva, ma l'indirizzo di TAPI 3 non è AddRef'ed. |
| \_handle msp                   | \*\_htCall m      | Handle per chiamare TAPI3's. Utilizzato per attivare gli eventi di chiamata.                                                                                                                                                                                                                                                                                             |
| DWORD                         | \_dwMediaType m   | Maschera di maschera dei tipi di supporto in questa chiamata.                                                                                                                                                                                                                                                                                                          |
| CMSPArray <ITStream \*> | \_flussi m       | Elenco di oggetti Stream nella chiamata.                                                                                                                                                                                                                                                                                                           |
| CMSPCritSection               | \_blocco m          | Blocco che protegge gli elenchi di flussi.                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 



