---
description: LOCALE \_ SPARENT
ms.assetid: 3fa0bc36-7577-4b5a-b557-8ac42e8594a8
title: LOCALE_SPARENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11383e6fcdd216a1837d9f2f31e70a26821d394c3c56ea614b1df197bbe35c76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105921"
---
# <a name="locale_sparent"></a>LOCALE \_ SPARENT

**Windows Vista e versioni successive:** Impostazioni locali di fallback, usate dal caricatore di risorse. Il numero massimo di caratteri consentiti per questa stringa è 85, incluso un carattere Null di terminazione.

Le impostazioni locali hanno una gerarchia in cui l'elemento padre di impostazioni locali specifiche è un'impostazione locale neutra. Le impostazioni locali specifiche sono associate sia a una lingua che a un paese, mentre le impostazioni locali non associate ad alcun paese sono associate a una lingua. Le impostazioni locali padre vengono usate per decidere il primo fallback da eseguire quando non è disponibile una risorsa per impostazioni locali specifiche. Ad esempio, le impostazioni locali padre per "en-US" (0x0409) sono "en" (0x0009). Quando una risorsa non è disponibile per le impostazioni locali "en-US" specifiche, il caricatore di risorse esegue il falls back per usare la risorsa disponibile per le impostazioni locali "en" neutre. Vedere [Interfaccia utente Language Management per](user-interface-language-management.md) altri dettagli sulla strategia di fallback del caricatore di risorse.

Questo modello è coerente per le impostazioni locali predefinite. Tuttavia, le impostazioni locali padre non sono determinate da alcuna modifica del nome delle impostazioni locali. In altri [**casi, GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) e [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) non analizzano una stringa come "en-US" per ottenere il valore "en". Vengono invece a esaminare i dati delle impostazioni locali archiviati. Per le impostazioni locali predefinite, il valore segue il modello previsto, in cui l'elemento padre di impostazioni locali specifiche corrisponde alle impostazioni locali neutre corrispondenti e l'elemento padre delle impostazioni locali neutre è quello invariante. Sebbene sia consigliabile che le impostazioni locali personalizzate seguano una strategia simile in termini di definizione delle impostazioni locali padre, questa operazione non viene applicata. L'applicazione che implementa impostazioni locali personalizzate può specificare un elemento padre meno appropriato.

> [!Note]  
> Poiché nessuna delle funzioni descritte in Chiamata delle funzioni ["Nome](calling-the--locale-name--functions.md) delle impostazioni locali" accetta impostazioni locali neutre come input, questi dati LOCALE SPARENT sono \_ di uso molto limitato. In particolare, [**né GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) né [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) accettano impostazioni locali neutre come input.

 

 

 



