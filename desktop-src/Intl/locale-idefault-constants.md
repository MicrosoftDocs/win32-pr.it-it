---
description: Questo argomento definisce le costanti \_ LOCALE IDEFAULT \* usate da NLS.
ms.assetid: 4fa8b5f3-8c01-44fb-b6fd-8dbf38e3d361
title: LOCALE_IDEFAULT* Costanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0524ea64d9924439e14ae6cb3cf16fed8a5f97ffb1e95d5f7fea98d5b6c61329
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106781"
---
# <a name="locale_idefault-constants"></a>Costanti IDEFAULT delle impostazioni \_ \* locali

Questo argomento definisce le costanti \_ LOCALE IDEFAULT \* usate da NLS.



| Valore                          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMPOSTAZIONI \_ LOCALI IDEFAULTANSICODEPAGE   | Tabella codici ANSI usata dalle impostazioni locali per le applicazioni che non supportano Unicode. Il numero massimo di caratteri consentiti per questa stringa è sei, incluso un carattere Null di terminazione. Se non è disponibile alcuna tabella codici ANSI, è possibile usare solo Unicode per le impostazioni locali. In questo caso, il valore è CP \_ ACP (0). Tali impostazioni locali non possono essere impostate come impostazioni locali del sistema. Le applicazioni che non supportano Unicode non funzionano correttamente con le impostazioni locali contrassegnate come "Solo Unicode". Per un elenco di ANSI e altre code pages, vedere [Identificatori di tabella codici](code-page-identifiers.md). |
| IMPOSTAZIONI \_ LOCALI IDEFAULTCODEPAGE       | Tabella codici OEM (Original Equipment Manufacturer) associata al paese o all'area geografica. La tabella codici OEM viene usata per la conversione da applicazioni in modalità testo basate su MS-DOS. Se le impostazioni locali non usano una tabella codici OEM, il valore è CP \_ OEMCP (1). Il numero massimo di caratteri consentiti per questa stringa è sei, incluso un carattere Null di terminazione. Per un elenco di OEM e altre code pages, vedere [Identificatori di tabella codici](code-page-identifiers.md).                                                                                                               |
| IMPOSTAZIONI \_ LOCALI IDEFAULTCOUNTRY        | Obsoleta. Non usare. Questo valore è stato fornito in modo che le impostazioni locali parzialmente specificate possono essere completate con i valori predefiniti. Le impostazioni locali parzialmente specificate sono ora deprecate.                                                                                                                                                                                                                                                                                                                                                                                               |
| IMPOSTAZIONI \_ LOCALI IDEFAULTEBCDICCODEPAGE | **Windows 2000:** Tabella Extended Binary Coded Decimal Interchange Code predefinita (EBCDIC) associata alle impostazioni locali. Il numero massimo di caratteri consentiti per questa stringa è sei, incluso un carattere Null di terminazione. Per un elenco di EBCDIC e altre code pages, vedere [Identificatori di tabella codici](code-page-identifiers.md).                                                                                                                                                                                                                                     |
| IMPOSTAZIONI \_ LOCALI IDEFAULTLANGUAGE       | Obsoleta. Non usare. Questo valore è stato fornito in modo che le impostazioni locali parzialmente specificate possono essere completate con i valori predefiniti. Le impostazioni locali parzialmente specificate sono ora deprecate.                                                                                                                                                                                                                                                                                                                                                                                               |
| IMPOSTAZIONI \_ LOCALI IDEFAULTMACCODEPAGE    | Tabella codici Macintosh predefinita associata alle impostazioni locali. Il numero massimo di caratteri consentiti per questa stringa è sei, incluso un carattere Null di terminazione. Se le impostazioni locali non usano una tabella codici Macintosh, il valore è CP \_ MACCP (2). Per un elenco di Macintosh (MAC) e altre code pages, vedere [Identificatori di tabella codici](code-page-identifiers.md).                                                                                                                                                                                                              |



 

 

 



