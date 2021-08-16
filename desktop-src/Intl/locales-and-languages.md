---
description: Il termine &\# 0034;lingua&0034; indica una raccolta di proprietà usate nella comunicazione \# parlata e scritta.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Impostazioni locali e lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462fc66a3296312de73a472309457e12954b6f30c80857594808350306bf4994
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147154"
---
# <a name="locales-and-languages"></a>Impostazioni locali e lingue

Il termine "lingua" indica una raccolta di proprietà usate nella comunicazione parlata e scritta. Ogni lingua ha un nome di lingua e un identificatore di lingua che indicano la [](table-of-geographical-locations.md) tabella codici [specifica](code-pages.md) (ANSI, DOS, Macintosh) usata per rappresentare la posizione geografica per la lingua nel sistema operativo. Una lingua neutra è indicata da un nome, ad esempio "en" per l'inglese. Una lingua più specifica dal punto di vista geografico può essere indicata da un nome che include informazioni sulle impostazioni locali e sul paese/area geografica. Ad esempio, le impostazioni locali inglese (Stati Uniti) hanno il nome di lingua "en-US".

Le "impostazioni locali" sono una raccolta di informazioni sulle preferenze utente correlate alla lingua rappresentate come elenco di valori. Windows XP supporta più di 150 impostazioni locali e Windows Vista ne supporta circa 200. Ogni impostazione locale è definita da una lingua e da un ordinamento e ha sia un nome di impostazioni locali che un identificatore delle impostazioni locali. Un esempio di nome delle impostazioni locali per il tedesco (Germania) è "de-DE \_ phonebook".

Ogni sistema operativo ha almeno un'impostazione locale installata e spesso ha molte impostazioni locali tra cui l'utente può selezionare. A ogni impostazione locale è associata un'ampia gamma di informazioni, diverse dal nome e dall'identificatore. I tipi di informazioni sulle impostazioni locali sono descritti in [Costanti di informazioni sulle impostazioni locali](locale-information-constants.md).

Il sistema operativo assegna le impostazioni locali a ogni thread, assegnando inizialmente le "impostazioni locali predefinite del sistema", definite da [IMPOSTAZIONI \_ LOCALI SYSTEM \_ DEFAULT](locale-system-default.md). Queste impostazioni locali vengono impostate quando il sistema operativo è installato o quando l'utente lo seleziona usando la parte relativa alle opzioni internazionali e della lingua del Pannello di controllo. Quando si esegue un thread in un processo appartenente all'utente, il sistema operativo assegna le "impostazioni locali predefinite dell'utente" al thread. Queste impostazioni locali sono definite da [IMPOSTAZIONI LOCALI \_ USER \_ DEFAULT](locale-user-default.md). Un'applicazione può eseguire l'override di entrambe le impostazioni predefinite usando [**la funzione SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) per impostare in modo esplicito le impostazioni locali per un thread.

L'implementazione di una lingua richiede impostazioni locali corrispondenti. Il sistema operativo implementa una lingua neutra selezionando i dati per le impostazioni locali associate a una versione specifica della lingua, in genere le impostazioni locali più diffuse.

A partire Windows Vista, è possibile che una determinata lingua corrisponda a impostazioni locali supplementari, ovvero un tipo di impostazioni locali personalizzate. Poiché le impostazioni locali supplementari condividono tutti un singolo identificatore delle impostazioni locali, le applicazioni devono gestire queste impostazioni locali e le lingue corrispondenti in base al nome anziché in base all'identificatore.

I concetti relativi alla lingua sono strettamente correlati ai concetti relativi alle impostazioni locali, ma i due termini non sono intercambiabili. Come regola generale, le funzioni correlate al interfaccia utente multilingue [riguardano](multilingual-user-interface.md) le lingue, mentre le funzioni NLS agiscono sulle impostazioni locali.

Questo articolo descrive gli argomenti seguenti:

-   [Impostazioni locali personalizzate](custom-locales.md)
-   [Identificatori di lingua](language-identifiers.md)
-   [Nomi delle lingue](language-names.md)
-   [Identificatori delle impostazioni locali](locale-identifiers.md)
-   [Nomi delle impostazioni locali](locale-names.md)
-   [Pseudo-impostazioni locali](pseudo-locales.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul supporto linguistico nazionale](about-national-language-support.md)
</dt> <dt>

[Code Pages](code-pages.md)
</dt> <dt>

[Costanti di informazioni sulle impostazioni locali](locale-information-constants.md)
</dt> <dt>

[Interfaccia utente multilingue](multilingual-user-interface.md)
</dt> <dt>

[Tabella delle posizioni geografiche](table-of-geographical-locations.md)
</dt> <dt>

[Interfaccia utente Language Management](user-interface-language-management.md)
</dt> <dt>

[**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



