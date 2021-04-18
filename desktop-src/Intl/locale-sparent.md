---
description: impostazioni locali \_ SPARENT
ms.assetid: 3fa0bc36-7577-4b5a-b557-8ac42e8594a8
title: LOCALE_SPARENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35a774c6a7f8eea631a2d6579b97058b30acdfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316275"
---
# <a name="locale_sparent"></a>impostazioni locali \_ SPARENT

**Windows Vista e versioni successive:** Impostazioni locali di fallback, usate dal caricatore di risorse. Il numero massimo di caratteri consentiti per questa stringa è 85, incluso un carattere di terminazione null.

Le impostazioni locali hanno una gerarchia in cui l'elemento padre di un'impostazione locale specifica è un'impostazione locale non associata ad alcun paese. Le impostazioni locali specifiche sono associate a una lingua e a un paese, mentre le impostazioni locali non associate ad alcun paese sono associate a una lingua. Le impostazioni locali padre vengono usate per decidere il primo fallback da provare quando una risorsa per le impostazioni locali specifiche non è disponibile. Ad esempio, le impostazioni locali padre per "en-US" (0x0409) sono "en" (ad esempio 0x0009). Quando una risorsa non è disponibile per le impostazioni locali "en-US" specifiche, il caricatore di risorse esegue il fallback per usare la risorsa disponibile per le impostazioni locali "en" neutre. Per ulteriori informazioni sulla strategia di fallback del caricatore di risorse, vedere [gestione della lingua dell'interfaccia utente](user-interface-language-management.md) .

Questo modello è coerente per le impostazioni locali predefinite. Tuttavia, le impostazioni locali padre non sono determinate da alcuna manipolazione del nome delle impostazioni locali. Ovvero, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) e [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) non analizzano una stringa, ad esempio "en-US", per ottenere il valore "en". Ma esaminano i dati delle impostazioni locali archiviati. Per le impostazioni locali predefinite, il valore segue il modello previsto, in cui l'elemento padre di un'impostazione locale specifica corrisponde alle impostazioni locali neutre corrispondenti e l'elemento padre di impostazioni locali non associate ad alcun paese è costituito dalle impostazioni locali invariabili. Sebbene sia consigliabile che le impostazioni locali personalizzate seguano una strategia simile per la definizione delle impostazioni locali padre, questo non viene applicato. L'applicazione che implementa le impostazioni locali personalizzate può specificare un elemento padre meno appropriato.

> [!Note]  
> Poiché nessuna delle funzioni descritte nella [chiamata delle funzioni "nome delle impostazioni locali"](calling-the--locale-name--functions.md) accetta impostazioni locali neutre come input, i \_ dati SPARENT delle impostazioni locali sono di uso molto limitato. In particolare, né [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) né [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) accettano impostazioni locali neutre come input.

 

 

 



