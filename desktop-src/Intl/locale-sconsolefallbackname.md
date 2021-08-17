---
description: IMPOSTAZIONI \_ LOCALI SCONSOLEFALLBACKNAME
ms.assetid: 36465a1c-085f-4f80-ad3d-5be6eaefe943
title: LOCALE_SCONSOLEFALLBACKNAME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4234ea00516f777b4f70adc6127fd7dcf089d687b16ce68df8fbb210057b469b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948496"
---
# <a name="locale_sconsolefallbackname"></a>IMPOSTAZIONI \_ LOCALI SCONSOLEFALLBACKNAME

**Windows Vista e versioni successive:** Impostazioni locali preferite da usare per la visualizzazione della console. Il numero massimo di caratteri consentiti per questa stringa è 85, incluso un carattere Null di terminazione.

> [!Note]  
> In generale, le applicazioni non devono usare direttamente i dati \_ LOCALE SCONSOLEFALLBACKNAME. Per determinare le risorse di lingua da usare in una finestra della console, un'applicazione deve chiamare [SetThreadUILanguage](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) o [SetThreadPreferredUILanguages](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Queste funzioni usano i dati di fallback della console come fattore nella scelta di un linguaggio leggibile nella console, ma non è l'unico determinante. In particolare, la console è limitata alla visualizzazione di caratteri da una singola tabella codici. Ad esempio, el-GR per greco (Grecia) è una lingua della console valida, ma se la tabella codici della console corrente è Latin-1 (tabella codici 1252) la console visualizza il testo greco principalmente come una serie di simboli non trovati da caratteri.

 

Se la lingua corrispondente a queste impostazioni locali è supportata nella console, il valore è uguale a quello di [LOCALE \_ SNAME,](locale-sname.md)vale a dire che le impostazioni locali possono essere usate per la visualizzazione della console. Tuttavia, la console non può visualizzare le lingue di cui è possibile eseguire il rendering solo [con Uniscribe.](uniscribe.md) Ad esempio, la console non può visualizzare l'arabo o le varie lingue indic. Pertanto, il valore LOCALE SCONSOLEFALLBACKNAME per le impostazioni locali corrispondenti a queste lingue è diverso dal valore \_ di LOCALE \_ SNAME.

Per le impostazioni locali predefinite, se il valore di fallback è diverso da quello delle impostazioni locali, viene usato il valore per le impostazioni locali neutre. Le impostazioni locali specifiche sono associate sia a una lingua che a un paese/area geografica, mentre le impostazioni locali neutre sono associate a una lingua, ma non sono associate ad alcun paese o area geografica. Ar-SA, ad esempio, torna a "en", non a "en-US". Questo criterio di uso delle impostazioni locali neutre viene implementato in modo coerente per le impostazioni locali predefinite ed è fortemente consigliato per le impostazioni locali personalizzate. Tuttavia, i criteri non vengono applicati. Per le impostazioni locali personalizzate, l'applicazione può usare impostazioni locali specifiche anziché impostazioni locali neutre come fallback.

> [!Note]  
> Nessuna delle funzioni descritte in [Chiamata delle funzioni "Nome impostazioni locali"](calling-the--locale-name--functions.md) accetta impostazioni locali neutre come input. I dati \_ LOCALE SCONSOLEFALLBACKNAME hanno quindi un uso molto limitato. In particolare, [**né GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) né [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) accetta impostazioni locali neutre come input.

 

 

 



