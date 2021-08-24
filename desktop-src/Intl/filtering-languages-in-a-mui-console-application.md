---
description: Un'applicazione console MUI può supportare impostazioni di sistema o impostazioni specifiche dell'applicazione per le lingue dell'interfaccia utente. In questo argomento viene illustrato il filtro delle lingue per questo tipo di applicazione.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtro delle lingue in un'applicazione console MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcdd8fc0f7f63b5771f5b75b86ce5e76ab2420d407832d77b731ad952174cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041321"
---
# <a name="filtering-languages-in-a-mui-console-application"></a>Filtro delle lingue in un'applicazione console MUI

Un'applicazione console MUI può supportare impostazioni di sistema o impostazioni specifiche dell'applicazione per le lingue dell'interfaccia utente. In questo argomento viene illustrato il filtro delle lingue per questo tipo di applicazione.

## <a name="limit-the-languages-to-display"></a>Limitare le lingue da visualizzare

A differenza di una finestra grafica, la console Windows non può visualizzare script [complessi,](uniscribe-glossary.md)ad esempio arabo, ebraico, persiano, hindi, Urdu, thai e molti altri. Pertanto, molte lingue dell'interfaccia utente non possono essere visualizzate dalla console in alcuna circostanza.

La console di può visualizzare solo i caratteri della singola [tabella codici OEM](code-pages.md) associata alla lingua corrente per le applicazioni non Unicode. Per ogni tabella codici OEM, la console usa un tipo di carattere specifico e ciò potrebbe non fornire copertura completa per tale tabella codici.

Queste limitazioni relative alla console riducono il numero di lingue dell'interfaccia utente che la console può visualizzare in un computer specifico. Ad esempio, se la lingua corrente per le applicazioni non Unicode è il giapponese e l'utente tenta di visualizzare il testo in tedesco nella console, i caratteri con umlaut non vengono visualizzati correttamente. Se la lingua corrente per le applicazioni non Unicode è il tedesco e l'utente vuole visualizzare il testo giapponese nella console, i risultati sono molto peggiori, rendendo il testo quasi incomprensibile.

> [!Note]  
> Quando si fornisce il supporto della console per le applicazioni MUI, tenere presente che la console fornisce solo supporto limitato per gli editor dei [metodi di input.](input-method-manager.md)

 

## <a name="set-the-language-for-console-output"></a>Impostare la lingua per l'output della console

In Windows Vista e versioni successive, un'applicazione console imposta la lingua per supportare la visualizzazione della console chiamando [**SetThreadPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) In questa chiamata, l'applicazione passa MUI CONSOLE FILTER nel \_ \_ parametro *dwFlags* e **NULL** per *pwszLanguagesBuffer*. In alternativa, chiamare [**SetThreadUILanguage con**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) un identificatore di lingua 0. Questa impostazione fa in modo che la funzione seleziona la lingua che meglio supporta la visualizzazione della console.

In Windows XP, l'applicazione può impostare solo la lingua per l'output della console chiamando [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) con un identificatore di lingua 0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione delle preferenze di lingua dell'applicazione](setting-application-language-preferences.md)
</dt> </dl>

 

 
