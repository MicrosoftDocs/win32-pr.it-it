---
description: impostazioni locali \_ SCONSOLEFALLBACKNAME
ms.assetid: 36465a1c-085f-4f80-ad3d-5be6eaefe943
title: LOCALE_SCONSOLEFALLBACKNAME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09536167c68a4ec9156a1558960c48778019ae97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313370"
---
# <a name="locale_sconsolefallbackname"></a>impostazioni locali \_ SCONSOLEFALLBACKNAME

**Windows Vista e versioni successive:** Impostazioni locali preferite da usare per la visualizzazione della console. Il numero massimo di caratteri consentiti per questa stringa è 85, incluso un carattere di terminazione null.

> [!Note]  
> In generale, le applicazioni non devono usare direttamente \_ i dati SCONSOLEFALLBACKNAME delle impostazioni locali. Per determinare le risorse di lingua da usare in una finestra della console, un'applicazione deve chiamare [SetThreadUILanguage](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) o [SetThreadPreferredUILanguages](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Queste funzioni usano i dati di fallback della console come fattore per la scelta di una lingua leggibile nella console, ma non è l'unico fattore determinante. In particolare, la console è limitata alla visualizzazione di caratteri da una singola tabella codici. Ad esempio, El-GR per greco (Grecia) è un linguaggio console valido, ma se la tabella codici della console corrente è Latin-1 (tabella codici 1252) la console Visualizza il testo greco principalmente come una serie di simboli non trovati.

 

Se la lingua corrispondente alle impostazioni locali è supportata nella console, il valore è identico a quello delle impostazioni locali [ \_ sName](locale-sname.md), ovvero le impostazioni locali possono essere usate per la visualizzazione della console. Tuttavia, la console non può visualizzare lingue di cui è possibile eseguire il rendering solo con [Uniscribe](uniscribe.md). Ad esempio, la console non può visualizzare l'arabo o le varie lingue indiane. Pertanto, il valore delle impostazioni locali \_ SCONSOLEFALLBACKNAME per le impostazioni locali corrispondenti a queste lingue è diverso dal valore di sName delle impostazioni locali \_ .

Per le impostazioni locali predefinite, se il valore di fallback è diverso dal valore per le impostazioni locali, viene utilizzato il valore per le impostazioni locali non associate ad alcun paese. Le impostazioni locali specifiche sono associate a una lingua e a un paese, mentre le impostazioni locali non associate ad alcun paese sono associate a una lingua. Ad esempio, ar-SA esegue il fallback a "en", non a "en-US". Questo criterio di utilizzo delle impostazioni locali neutre viene implementato in modo coerente per le impostazioni locali predefinite ed è fortemente consigliato per le impostazioni locali personalizzate. Tuttavia, i criteri non vengono applicati. Per le impostazioni locali personalizzate, l'applicazione può usare impostazioni locali specifiche anziché impostazioni locali non associate ad alcun paese come fallback.

> [!Note]  
> Nessuna delle funzioni descritte nella [chiamata delle funzioni "nome delle impostazioni locali"](calling-the--locale-name--functions.md) accetta impostazioni locali neutre come input. \_Di conseguenza, le impostazioni locali SCONSOLEFALLBACKNAME i dati hanno un uso molto limitato. In particolare, né [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) né [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) accettano impostazioni locali neutre come input.

 

 

 



