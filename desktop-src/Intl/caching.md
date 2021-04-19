---
description: Uniscribe Salva i mapping da Unicode a glifo (CMAP), le larghezze del glifo e le tabelle di shaping degli script OpenType.
ms.assetid: c06c0eaf-41cb-4fd1-9750-a78355217f12
title: Caching (internazionalizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf8bf7dd10fe414bc170086ff9b8c34142dc197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319988"
---
# <a name="caching-internationalization"></a>Caching (internazionalizzazione)

Uniscribe Salva i mapping da Unicode a glifo (CMAP), le larghezze del glifo e le tabelle di shaping degli script OpenType. Un handle per le tabelle per un particolare tipo di carattere di una determinata dimensione è denominato "cache script". Molte funzioni Uniscribe richiedono sia un parametro di handle del contesto di dispositivo che un puntatore a una struttura [**\_ della cache di script**](script-cache.md) . Queste funzioni ricercano prima di tutto le informazioni tramite la cache di script, usando il contesto di dispositivo solo quando le tabelle obbligatorie non sono già memorizzate nella cache. Quando si chiama la funzione [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)o [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) , l'applicazione deve passare un puntatore a una **struttura \_ della cache di script** . L'handle deve essere inizializzato su **null** prima della prima volta che l'applicazione passa a una funzione Uniscribe. L'applicazione non deve mai passare lo stesso handle per diversi tipi di carattere o dimensioni diverse.

Un'applicazione può liberare una cache di script in qualsiasi momento. Uniscribe mantiene i conteggi dei riferimenti nelle cache del tipo di carattere e del shaper, libera i dati del tipo di carattere solo quando vengono liberate tutte le dimensioni del tipo di carattere e libera i dati di shaper solo quando vengono liberati tutti i tipi di carattere supportati dallo shaper. Quando l'applicazione viene eseguita con uno stile, deve chiamare la funzione [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache) per liberare la cache di script per lo stile.

Per [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) e [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace), è possibile che l'applicazione passi un contesto di dispositivo null. Spesso la chiamata avrà esito positivo, in quanto le tabelle obbligatorie sono già memorizzate nella cache. Se il data shaping o la selezione host richiede l'accesso a un contesto di dispositivo, **ScriptShape** o **ScriptPlace** restituisce immediatamente il \_ codice di errore E in sospeso. Quindi, l'applicazione deve selezionare il tipo di carattere nel contesto di dispositivo. Per la maggior parte delle applicazioni, questo consente di migliorare le prestazioni evitando la preparazione ripetuta di un handle di contesto di dispositivo con chiamate a [**SelezionaOggetto**](/windows/win32/api/wingdi/nf-wingdi-selectobject).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
