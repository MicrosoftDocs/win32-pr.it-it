---
description: Il termine &\# 0034; language&\# 0034; indica una raccolta di proprietà utilizzate per la comunicazione pronunciata e scritta.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Impostazioni locali e lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2c0d0fa41b9186b2135d9497d52de24577bbae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308706"
---
# <a name="locales-and-languages"></a>Impostazioni locali e lingue

Il termine "lingua" indica una raccolta di proprietà utilizzate per la comunicazione vocale e scritta. Ogni lingua dispone di un nome di lingua e di un identificatore di lingua che indicano la [tabella codici](code-pages.md) specifica (ANSI, DOS, Macintosh) utilizzata per rappresentare la [posizione geografica](table-of-geographical-locations.md) per la lingua del sistema operativo. Una lingua neutra è indicata da un nome, ad esempio "en" per l'inglese. Un linguaggio più geograficamente specifico può essere indicato da un nome che include le informazioni sulle impostazioni locali e il paese/area geografica. Ad esempio, le impostazioni locali Inglese (Stati Uniti) hanno il nome della lingua "en-US".

Le "impostazioni locali" sono una raccolta di informazioni sulle preferenze utente correlate al linguaggio rappresentate come un elenco di valori. Windows XP supporta più di 150 impostazioni locali e Windows Vista supporta circa 200. Ogni impostazione locale è definita da un linguaggio e un ordinamento e ha sia un nome delle impostazioni locali che un identificatore delle impostazioni locali. Un esempio di nome delle impostazioni locali per la lingua tedesca (Germania) è "de-DE \_ Rubrica".

Ogni sistema operativo ha almeno un'impostazione locale installata e spesso ha molte impostazioni locali da cui l'utente può selezionare. A ogni impostazione locale sono associate numerose informazioni, tranne il nome e l'identificatore. I tipi di informazioni sulle impostazioni locali sono descritti in [costanti di informazioni sulle impostazioni locali](locale-information-constants.md).

Il sistema operativo assegna impostazioni locali a ogni thread, assegnando inizialmente le impostazioni locali predefinite del sistema, definite dalle [impostazioni locali del \_ sistema \_ ](locale-system-default.md). Le impostazioni locali vengono impostate quando viene installato il sistema operativo o quando l'utente lo seleziona utilizzando la parte opzioni internazionali e della lingua del pannello di controllo. Quando si esegue un thread in un processo appartenente all'utente, il sistema operativo assegna al thread le impostazioni locali predefinite dell'utente. Questa impostazione locale è definita da [impostazioni locali \_ dell' \_ utente](locale-user-default.md). Un'applicazione può eseguire l'override di entrambi i valori predefiniti utilizzando la funzione [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) per impostare in modo esplicito le impostazioni locali per un thread.

Per l'implementazione di un linguaggio è necessario specificare le impostazioni locali corrispondenti. Il sistema operativo implementa una lingua neutra selezionando i dati per le impostazioni locali associate a una versione specifica del linguaggio, in genere le impostazioni locali più diffuse.

A partire da Windows Vista, è possibile che una determinata lingua corrisponda a un'impostazione locale supplementare, ovvero un tipo di impostazioni locali personalizzate. Poiché tutte le impostazioni locali aggiuntive condividono un solo identificatore delle impostazioni locali, le applicazioni devono gestire queste impostazioni locali e le lingue corrispondenti per nome anziché per identificatore.

I concetti relativi alla lingua sono strettamente correlati ai concetti locali, ma i due termini non sono intercambiabili. Come regola generale, le funzioni correlate all' [interfaccia utente multilingue](multilingual-user-interface.md) gestiscono le lingue, mentre le funzioni NLS agiscono sulle impostazioni locali.

Questo articolo descrive gli argomenti seguenti:

-   [Impostazioni locali personalizzate](custom-locales.md)
-   [Identificatori di lingua](language-identifiers.md)
-   [Nomi di lingua](language-names.md)
-   [Identificatori delle impostazioni locali](locale-identifiers.md)
-   [Nomi delle impostazioni locali](locale-names.md)
-   [Pseudo-impostazioni locali](pseudo-locales.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul supporto linguistico nazionale](about-national-language-support.md)
</dt> <dt>

[Tabelle codici](code-pages.md)
</dt> <dt>

[Costanti di informazioni sulle impostazioni locali](locale-information-constants.md)
</dt> <dt>

[Interfaccia utente multilingue](multilingual-user-interface.md)
</dt> <dt>

[Tabella delle posizioni geografiche](table-of-geographical-locations.md)
</dt> <dt>

[Gestione della lingua dell'interfaccia utente](user-interface-language-management.md)
</dt> <dt>

[**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



