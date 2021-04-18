---
description: S2359 delle impostazioni locali \_ e \_ SPM locale
ms.assetid: 8a97073e-84f6-47d9-98fb-65760e8a6cd8
title: LOCALE_S2359 e LOCALE_SPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca0c22d541102fcdf0826778de591dc4100dda55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315483"
---
# <a name="locale_s2359-and-locale_spm"></a>S2359 delle impostazioni locali \_ e \_ SPM locale

Stringa per l'indicatore PM (seconda 12 ore del giorno). Il numero massimo di caratteri consentiti per questa stringa è diverso per le diverse versioni di Windows.

**Windows XP:** Tredici, incluso un carattere null di terminazione per [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Quindici, incluso un carattere null di terminazione per [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

**Windows Me/98/95, Windows NT 4,0, windows 2000:** Nine che include un carattere null di terminazione.

**Windows Server 2003 e versioni successive:** Quindici, incluso un carattere null di terminazione.

Windows 10 ha aggiunto il valore delle **impostazioni locali \_ SPM** come sinonimo più leggibile per le **impostazioni locali \_ S2359**.

 

 



