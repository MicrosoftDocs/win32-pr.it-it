---
description: Un'applicazione console MUI può supportare le impostazioni di sistema o le impostazioni specifiche dell'applicazione per le lingue dell'interfaccia utente. In questo argomento viene illustrato il filtro delle lingue per questo tipo di applicazione.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtraggio di lingue in un'applicazione console MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d484835af211f59cc559f8e1cd0dd414af13a8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882146"
---
# <a name="filtering-languages-in-a-mui-console-application"></a>Filtraggio di lingue in un'applicazione console MUI

Un'applicazione console MUI può supportare le impostazioni di sistema o le impostazioni specifiche dell'applicazione per le lingue dell'interfaccia utente. In questo argomento viene illustrato il filtro delle lingue per questo tipo di applicazione.

## <a name="limit-the-languages-to-display"></a>Limitare le lingue da visualizzare

A differenza di una finestra grafica, la console di Windows non è in grado di visualizzare [alfabeti complessi](uniscribe-glossary.md), ad esempio arabo, ebraico, persiano, Hindi, Urdu, Thai e molti altri. Pertanto, molte lingue dell'interfaccia utente non possono essere visualizzate dalla console in qualsiasi circostanza.

Nella console di è possibile visualizzare solo i caratteri della singola [tabella codici OEM](code-pages.md) associata alla lingua corrente per le applicazioni non Unicode. Per ogni tabella codici OEM, nella console viene utilizzato un particolare tipo di carattere e questo potrebbe non fornire una copertura completa per tale tabella codici.

Queste limitazioni relative alla console riducono il numero di lingue dell'interfaccia utente che possono essere visualizzate dalla console in un computer specifico. Se, ad esempio, la lingua corrente per le applicazioni non Unicode è giapponese e l'utente tenta di visualizzare il testo tedesco nella console, i caratteri con dieresi non vengono visualizzati correttamente. Se la lingua corrente per le applicazioni non Unicode è il tedesco e l'utente desidera visualizzare il testo giapponese nella console, i risultati sono molto peggiori, rendendo il testo quasi incomprensibile.

> [!Note]  
> Quando si fornisce il supporto della console per le applicazioni MUI, tenere presente che la console fornisce solo il supporto limitato per gli [Editor del metodo di input](input-method-manager.md).

 

## <a name="set-the-language-for-console-output"></a>Impostare la lingua per l'output della console

In Windows Vista e versioni successive, un'applicazione console imposta la lingua per supportare la visualizzazione della console chiamando [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). In questa chiamata, l'applicazione passa il \_ filtro della console MUI \_ nel parametro *dwFlags* e **null** per *pwszLanguagesBuffer*. In alternativa, è possibile chiamare [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) con un identificatore di lingua pari a 0. Questa impostazione fa in modo che la funzione selezioni la lingua che meglio supporta la visualizzazione della console.

In Windows XP, l'applicazione può impostare solo la lingua per l'output della console chiamando [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) con un identificatore di lingua pari a 0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione delle preferenze di lingua dell'applicazione](setting-application-language-preferences.md)
</dt> </dl>

 

 
