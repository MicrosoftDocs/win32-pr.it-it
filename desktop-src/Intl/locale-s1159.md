---
description: Impostazioni locali \_ S1159 e Sam locale \_
ms.assetid: dc7058af-1d5f-40a0-8d0b-17d2ff5662ce
title: LOCALE_S1159 e LOCALE_SAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b41f98ea5c07f1d88534c1e47acecfa81a4e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883697"
---
# <a name="locale_s1159-and-locale_sam"></a>Impostazioni locali \_ S1159 e Sam locale \_

Stringa per l'indicatore AM (prime 12 ore del giorno). Il numero massimo di caratteri consentiti per questa stringa, incluso un carattere di terminazione null, è diverso per le diverse versioni di Windows.

**Windows XP:** Tredici, incluso un carattere null di terminazione per [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Quindici, incluso un carattere null di terminazione per [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

**Windows Me/98/95, Windows NT 4,0, windows 2000:** Nine che include un carattere null di terminazione.

**Windows Server 2003 e versioni successive:** Quindici, incluso un carattere null di terminazione.

Windows 10 ha aggiunto il valore **locale \_ Sam** come sinonimo più leggibile per le **impostazioni locali \_ S1159**.

 

 



