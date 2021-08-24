---
description: Uniscribe salva mapping da Unicode a glifo (cmap), larghezze dei glifi e tabelle di data shaping dello script OpenType.
ms.assetid: c06c0eaf-41cb-4fd1-9750-a78355217f12
title: Caching (internazionalizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a01d8444fa222c2b6f6c7b03d0e1be70c1e04b1509ab020b8769d87b2b5cbc0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500831"
---
# <a name="caching-internationalization"></a>Caching (internazionalizzazione)

Uniscribe salva mapping da Unicode a glifo (cmap), larghezze dei glifi e tabelle di data shaping dello script OpenType. Un handle per le tabelle per un tipo di carattere specifico di una determinata dimensione è detto "cache di script". Molte funzioni Uniscribe chiamano sia per un parametro di handle del contesto di dispositivo che per un puntatore a una [**struttura \_ SCRIPT CACHE.**](script-cache.md) Queste funzioni ricercano prima di tutto informazioni tramite la cache degli script, usando il contesto di dispositivo solo quando le tabelle necessarie non sono già memorizzate nella cache. Quando si chiama [**la funzione ScriptShape,**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)o [**ScriptTextOut,**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) l'applicazione deve passare un puntatore a una **struttura SCRIPT \_ CACHE.** L'handle deve essere inizializzato su **NULL prima** della prima volta che l'applicazione lo passa a una funzione Uniscribe. L'applicazione non deve mai passare lo stesso handle per tipi di carattere o dimensioni diverse.

Un'applicazione può liberare una cache di script in qualsiasi momento. Uniscribe mantiene i conteggi dei riferimenti nelle cache dei tipi di carattere e shaper, libera i dati dei tipi di carattere solo quando vengono liberate tutte le dimensioni del tipo di carattere e libera i dati dello shaper solo quando vengono liberati tutti i tipi di carattere supportati dal shaper. Quando l'applicazione viene completata con uno stile, deve chiamare la [**funzione ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache) per liberare la cache degli script per lo stile.

Per [**ScriptShape e**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace), è valido per l'applicazione passare un contesto di dispositivo Null. Nella maggior parte dei casi la chiamata avrà esito positivo, in quanto le tabelle obbligatorie sono già memorizzate nella cache. Se il shaping o il posizionamento richiede l'accesso a un contesto di dispositivo, **ScriptShape** o **ScriptPlace** restituisce immediatamente il codice di errore E \_ PENDING. L'applicazione deve quindi selezionare il tipo di carattere nel contesto di dispositivo. Per la maggior parte delle applicazioni, ciò consente di migliorare le prestazioni evitando la preparazione ripetuta di un handle del contesto di dispositivo con chiamate a [**SelectObject.**](/windows/win32/api/wingdi/nf-wingdi-selectobject)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
