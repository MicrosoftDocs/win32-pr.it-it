---
description: Questo argomento definisce le impostazioni locali \_ IDEFAULT \* costanti usate da NLS.
ms.assetid: 4fa8b5f3-8c01-44fb-b6fd-8dbf38e3d361
title: Costanti LOCALE_IDEFAULT *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9c440c27a2fe551eae7d03d66cc43b500e8f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305639"
---
# <a name="locale_idefault-constants"></a>Costanti IDEFAULT delle impostazioni locali \_ \*

Questo argomento definisce le impostazioni locali \_ IDEFAULT \* costanti usate da NLS.



| Valore                          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| impostazioni locali \_ IDEFAULTANSICODEPAGE   | Tabella codici ANSI utilizzata dalle impostazioni locali per le applicazioni che non supportano Unicode. Il numero massimo di caratteri consentiti per questa stringa è sei, incluso un carattere di terminazione null. Se non è disponibile alcuna tabella codici ANSI, per le impostazioni locali è possibile utilizzare solo Unicode. In questo caso, il valore è CP \_ ACP (0). Le impostazioni locali di questo tipo non possono essere impostate come impostazioni locali del sistema. Le applicazioni che non supportano Unicode non funzionano correttamente con le impostazioni locali contrassegnate come "solo Unicode". Per un elenco delle tabelle codici ANSI e altre, vedere [identificatori della tabella codici](code-page-identifiers.md). |
| impostazioni locali \_ IDEFAULTCODEPAGE       | Tabella codici OEM (Original Equipment Manufacturer) associata al paese/area geografica. La tabella codici OEM viene utilizzata per la conversione da applicazioni in modalità testo basate su MS-DOS. Se le impostazioni locali non utilizzano una tabella codici OEM, il valore è CP \_ OEMCP (1). Il numero massimo di caratteri consentiti per questa stringa è sei, incluso un carattere di terminazione null. Per un elenco delle tabelle codici OEM e altre, vedere [identificatori della tabella codici](code-page-identifiers.md).                                                                                                               |
| impostazioni locali \_ IDEFAULTCOUNTRY        | Obsoleta. Non usare. Questo valore è stato specificato in modo che le impostazioni locali parzialmente specificate possano essere completate con i valori predefiniti. Le impostazioni locali parzialmente specificate sono ora deprecate.                                                                                                                                                                                                                                                                                                                                                                                               |
| impostazioni locali \_ IDEFAULTEBCDICCODEPAGE | **Windows 2000:** Tabella codici Extended Binary Coded Decimal Interchange Code (EBCDIC) predefinita associata alle impostazioni locali. Il numero massimo di caratteri consentiti per questa stringa è sei, incluso un carattere di terminazione null. Per un elenco di codici EBCDIC e altre tabelle codici, vedere [identificatori della tabella codici](code-page-identifiers.md).                                                                                                                                                                                                                                     |
| impostazioni locali \_ IDEFAULTLANGUAGE       | Obsoleta. Non usare. Questo valore è stato specificato in modo che le impostazioni locali parzialmente specificate possano essere completate con i valori predefiniti. Le impostazioni locali parzialmente specificate sono ora deprecate.                                                                                                                                                                                                                                                                                                                                                                                               |
| impostazioni locali \_ IDEFAULTMACCODEPAGE    | Tabella codici Macintosh predefinita associata alle impostazioni locali. Il numero massimo di caratteri consentiti per questa stringa è sei, incluso un carattere di terminazione null. Se le impostazioni locali non utilizzano una tabella codici Macintosh, il valore è CP \_ MACCP (2). Per un elenco di Macintosh (MAC) e altre tabelle codici, vedere [identificatori della tabella codici](code-page-identifiers.md).                                                                                                                                                                                                              |



 

 

 



