---
description: SSCRIPT \_ DELLE IMPOSTAZIONI LOCALI
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aede4d6d1843fd32bdd17ae3a275a364c3a2d4f0bd282302f49d7b4a3b0dd1ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105851"
---
# <a name="locale_sscripts"></a>SSCRIPT \_ DELLE IMPOSTAZIONI LOCALI

**Windows Vista e versioni successive:** Stringa che rappresenta un elenco di script, utilizzando la notazione a 4 caratteri usata in [ISO 15924.](https://www.unicode.org/iso15924/iso15924-codes.html) Ogni nome di script è costituito da quattro caratteri latini e l'elenco viene disposto in ordine alfabetico con ogni nome, incluso l'ultimo, seguito da un punto e virgola.

È possibile chiamare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con *LCType* impostato su LOCALE SSCRIPTS come parte di una strategia per attenuare i problemi di sicurezza correlati ai nomi \_ IDN (Internationalized Domain Names). Ecco alcuni valori di esempio:



| Locale                  | Nome delle impostazioni locali/della lingua | Valore                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| Inglese (Stati Uniti) | it-IT                | Latn;                                                                                                  |
| Hindi (India)           | hi-IN                | Deva;                                                                                                  |
| Giapponese (Giappone)        | ja-JP                | **Windows 7 e versioni successive:** Hani; Hira; Jpan; Kana;<br/> **Windows Vista:** Hani; Hira; Kana;<br/> |



 

Un valore di script composto non include lo script latino a meno che non sia una parte essenziale del sistema di scrittura usato per le impostazioni locali specifiche. I caratteri latini vengono spesso usati nel contesto delle impostazioni locali per cui non sono nativi, ad esempio per un nome di azienda esterna. Nell'esempio precedente per l'hindi in India, l'unico valore dello script è "Deva" (per "Devanagari"), anche se i caratteri latini possono essere visualizzati anche nel testo in hindi. La [funzione VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) ha un flag speciale per risolvere questo caso.

 

 




