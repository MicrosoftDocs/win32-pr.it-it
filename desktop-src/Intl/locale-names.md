---
description: Un nome delle impostazioni locali è basato sulle convenzioni di codifica della lingua RFC 4646 (Windows Vista e versioni successive) ed è rappresentato dalle impostazioni locali \_ sname.
ms.assetid: 221aae7b-3a7c-4995-ae78-50d97de436d8
title: Nomi delle impostazioni locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9808db94615cba4416c12995b9c969eaaf5a3fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314807"
---
# <a name="locale-names"></a>Nomi delle impostazioni locali

Un nome delle [impostazioni locali](locales-and-languages.md) è basato sulle convenzioni di codifica della lingua RFC 4646 (Windows Vista e versioni successive) ed è rappresentato dalle [impostazioni locali \_ sName](locale-sname.md). In genere `<language>-<REGION>` viene usato il modello. In questo caso il linguaggio è un codice lingua ISO 639 minuscolo. I codici da ISO 639-1 vengono usati quando disponibili. In caso contrario, vengono usati i codici di ISO 639-2/T. REGION specifica un identificatore di paese/area geografica ISO 3166-1 maiuscolo. Ad esempio, il nome delle impostazioni locali per la lingua inglese (Stati Uniti) è "en-US" e il nome delle impostazioni locali per Divehi (Maldive) è "DV-MV".

> [!Note]  
> Il [nome delle impostazioni locali della costante \_ \_ Max \_ length](locale-name-constants.md) indica la lunghezza massima del nome delle impostazioni locali. Include lo spazio per un carattere null di terminazione.

 

Se le impostazioni locali sono impostazioni locali non associate ad alcun paese (nessuna area), il valore delle [impostazioni locali \_ sName](locale-sname.md) segue il modello `<language>` . Se si tratta di impostazioni locali non associate ad alcun paese per cui lo script è significativo, il modello è `<language>-<Script>` .

Se le impostazioni locali devono essere distinte dalle altre impostazioni locali per la stessa lingua e area usando uno script diverso, il valore delle impostazioni locali \_ sName segue il modello `<language>-<Script>-<REGION>` , dove script è un codice di script [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html) maiuscolo. Ad esempio, il valore delle impostazioni locali \_ sName per le impostazioni locali specifiche Uzbeco (alfabeto latino, Uzbekistan) è "UZ-Latn-uz". Il componente script non è incluso nei casi in cui un linguaggio viene comunemente scritto in un solo script.

Gli ordinamenti per le impostazioni locali vengono designati utilizzando gli [identificatori](sort-order-identifiers.md)di ordinamento, ad esempio, ordinamento \_ predefinito. Per distinguere due o più ordinamenti per la stessa lingua e per la stessa area, il nome delle impostazioni locali segue il modello `<language>-<REGION>\_<sort order>` . Se è necessario distinguere sia script che ordinamento, il nome segue il modello `<language>-<Script>-<REGION>\_<sort order>` . L'ordinamento predefinito non viene mai specificato in modo esplicito, bensì solo l'ordinamento alternativo. Ad esempio, ungherese (Ungheria) con \_ il valore predefinito di ordinamento o il valore predefinito ungherese di ordinamento numerico equivalente \_ \_ viene designato come "hu-HU". Ungherese (Ungheria) con ordinamento in base ai dati \_ tecnici ungheresi \_ è designato come "HU-HU \_ technl".

Per le [impostazioni locali sostitutive](custom-locales.md), il nome delle impostazioni locali deve corrispondere al nome delle impostazioni locali da sostituire. Per le impostazioni locali aggiuntive, il nome delle impostazioni locali deve seguire il modello di `<language>-<REGION>-x-<custom>` o `<language>-<Script>-<REGION>-x-<custom>` , dove `<custom>` è una stringa alfanumerica specifica delle impostazioni locali aggiuntive. Ad esempio, le impostazioni locali supplementari specifiche di una società denominata fabricat potrebbero essere denominate "en-US-x-fabricat".

Un'applicazione può recuperare i nomi delle impostazioni locali correnti usando le funzioni [**GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) e [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename) . Mentre ogni thread può recuperare e impostare il proprio identificatore delle impostazioni locali con [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) e impostarlo con [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale), non sono disponibili funzioni analoghe per ottenere e impostare le impostazioni locali in base al nome.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni locali e lingue](locales-and-languages.md)
</dt> <dt>

[Impostazioni locali personalizzate](custom-locales.md)
</dt> <dt>

[Identificatori delle impostazioni locali](locale-identifiers.md)
</dt> <dt>

[Identificatori di ordinamento](sort-order-identifiers.md)
</dt> </dl>

 

 



