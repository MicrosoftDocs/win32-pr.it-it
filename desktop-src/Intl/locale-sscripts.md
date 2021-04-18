---
description: impostazioni locali \_ SSCRIPTS
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307850"
---
# <a name="locale_sscripts"></a>impostazioni locali \_ SSCRIPTS

**Windows Vista e versioni successive:** Stringa che rappresenta un elenco di script, utilizzando la notazione di 4 caratteri utilizzata in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html). Ogni nome di script è costituito da quattro caratteri latini e l'elenco viene disposto in ordine alfabetico con ogni nome, incluso l'ultimo, seguito da un punto e virgola.

È possibile chiamare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con *LCType* impostato su locale \_ SSCRIPTS come parte di una strategia per attenuare i problemi di sicurezza correlati ai nomi di dominio internazionali (IDN). Di seguito sono riportati alcuni valori di esempio:



| Locale                  | Nome delle impostazioni locali/lingua | Valore                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| Inglese (Stati Uniti) | it-IT                | Latn                                                                                                  |
| Hindi (India)           | hi-IN                | Deva                                                                                                  |
| Giapponese (Giappone)        | ja-JP                | **Windows 7 e versioni successive:** Hani Hira Jpan; Kana<br/> **Windows Vista:** Hani Hira Kana<br/> |



 

Un valore di script composto non include lo script latino, a meno che non si tratti di una parte essenziale del sistema di scrittura usato per le impostazioni locali specifiche. I caratteri latini vengono spesso utilizzati nel contesto delle impostazioni locali per le quali non sono nativi, ad esempio per un nome aziendale esterno. Nell'esempio precedente per hindi in India, l'unico valore di script è "Deva" (per "devangal"), anche se i caratteri latini possono essere visualizzati anche in testo Hindi. La funzione [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) ha un flag speciale per risolvere questo caso.

 

 




