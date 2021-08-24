---
description: Un nome delle impostazioni locali è basato sulle convenzioni di assegnazione di tag alla lingua di RFC 4646 (Windows Vista e versioni successive) ed è rappresentato da LOCALE \_ SNAME.
ms.assetid: 221aae7b-3a7c-4995-ae78-50d97de436d8
title: Nomi delle impostazioni locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed4c09900544e96c0f05166d1f4054972e9d8ff89fc108c185695a7506859bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147403"
---
# <a name="locale-names"></a>Nomi delle impostazioni locali

Un [nome](locales-and-languages.md) delle impostazioni locali è basato sulle convenzioni di assegnazione di tag alla lingua di RFC 4646 (Windows Vista e versioni successive) ed è rappresentato da [LOCALE \_ SNAME](locale-sname.md). In genere, viene `<language>-<REGION>` usato il modello . In questo caso, language è un codice lingua ISO 639 minuscolo. I codici ISO 639-1 vengono usati quando disponibili. In caso contrario, vengono usati i codici ISO 639-2/T. REGION specifica un identificatore di paese/area geografica ISO 3166-1 maiuscolo. Ad esempio, il nome delle impostazioni locali per l'inglese (Stati Uniti) è "en-US" e il nome delle impostazioni locali per Divehi (Tutto) è "dv-MV".

> [!Note]  
> La costante [LOCALE \_ NAME MAX \_ \_ LENGTH](locale-name-constants.md) indica la lunghezza massima di un nome di impostazioni locali. Include lo spazio per un carattere Null di terminazione.

 

Se le impostazioni locali sono neutre (nessuna area), il [valore \_ LOCALE SNAME](locale-sname.md) segue il modello `<language>` . Se si tratta di impostazioni locali neutre per le quali lo script è significativo, il modello è `<language>-<Script>` .

Se le impostazioni locali devono essere distinte da altre impostazioni locali per la stessa lingua e la stessa area usando uno script diverso, il valore LOCALE SNAME segue il modello , dove Script è un codice \_ `<language>-<Script>-<REGION>` script [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html) iniziale maiuscolo. Ad esempio, il valore LOCALE SNAME per le impostazioni locali specifiche \_ dell'Uzbeco (alfabeto latino, Uzbekistan) è "uz-Latn-UZ". Il componente script non è incluso nei casi in cui un linguaggio viene in genere scritto in un solo script.

Gli ordinamenti per le impostazioni locali vengono designati usando identificatori [di ordinamento,](sort-order-identifiers.md)ad esempio SORT \_ DEFAULT. Per distinguere due o più ordinazioni per la stessa lingua e la stessa area, il nome delle impostazioni locali segue il modello `<language>-<REGION>\_<sort order>` . Se è necessario distinguere sia lo script che l'ordinamento, il nome segue il criterio `<language>-<Script>-<REGION>\_<sort order>` . L'ordinamento predefinito non viene mai specificato in modo esplicito, ma solo l'ordinamento alternativo. Ad esempio, l'ungherese (Avaia) con SORT DEFAULT o l'equivalente numerico SORT HUNGARIAN DEFAULT è \_ \_ \_ designato come "hu-HU". L'ungherese (Repubblica) con ordinamento SORT \_ HUNGARIAN \_ TECHNICAL è designato come "hu-HU \_ technl".

Per le [impostazioni locali sostitutive,](custom-locales.md)il nome delle impostazioni locali deve corrispondere al nome delle impostazioni locali da sostituire. Per le impostazioni locali supplementari, il nome delle impostazioni locali deve seguire il modello di o , dove è una stringa `<language>-<REGION>-x-<custom>` `<language>-<Script>-<REGION>-x-<custom>` `<custom>` alfanumerica specifica delle impostazioni locali supplementari. Ad esempio, le impostazioni locali supplementari specifiche di una società denominata Fabricam potrebbero essere denominate "en-US-x-fabricam".

Un'applicazione può recuperare i nomi delle impostazioni locali correnti usando le [**funzioni GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) e [**GetUserDefaultLocaleName.**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename) Anche se ogni thread può recuperare e impostare il proprio identificatore delle impostazioni locali con [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) e impostarlo con [**SetThreadLocale,**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)non sono disponibili funzioni analoghe per ottenere e impostare le impostazioni locali in base al nome.

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

 

 



