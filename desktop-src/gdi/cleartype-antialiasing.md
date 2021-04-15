---
description: Anti-aliasing di Microsoft ClearType è un metodo di smussatura che migliora la risoluzione dello schermo del tipo di carattere rispetto all'anti-aliasing tradizionale.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: ClearType Antialiasing (Anti-aliasing ClearType)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbe7ae1a6c99fcee826c576b7671aea6e9ce6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978775"
---
# <a name="cleartype-antialiasing"></a>ClearType Antialiasing (Anti-aliasing ClearType)

Anti-aliasing di Microsoft ClearType è un metodo di smussatura che migliora la risoluzione dello schermo del tipo di carattere rispetto all'anti-aliasing tradizionale. Migliora significativamente la leggibilità dei monitor LCD a colori con un'interfaccia digitale, ad esempio i computer portatili e le visualizzazioni desktop flat di alta qualità. Anche la leggibilità sulle schermate CRT è stata migliorata.

Tuttavia, ClearType dipende dall'orientamento e dall'ordinamento dei nastri LCD. Attualmente, ClearType viene implementato solo per gli LCD con striping verticali ordinati RGB. In particolare, ciò influiscono sui Tablet PC, in cui la visualizzazione può essere orientata in qualsiasi direzione e le schermate che è possibile trasformare dall'orizzontale al verticale.

Anti-aliasing ClearType consentito:

-   Per il colore a 16, 24 e 32 bit (disabilitato per 256 colori o meno)
-   Per il controller di dominio della schermata e della memoria
-   Per i tipi di carattere TrueType e OpenType con le strutture TrueType

Anti-aliasing ClearType disabilitato:

-   In Terminal Server client
-   Per i tipi di carattere bitmap, i tipi di carattere vettoriali, i tipi di carattere del dispositivo, i tipi 1 o i tipi di carattere OpenType
-   Se il tipo di carattere ha ottimizzato le bitmap incorporate, solo per le dimensioni dei tipi di carattere che contengono le bitmap incorporate

Per attivare l'anti-aliasing ClearType, chiamare [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) una volta per attivare la smussatura dei caratteri e quindi una seconda volta per impostare il tipo di smussatura su Fe \_ FONTSMOOTHINGCLEARTYPE, come illustrato nell'esempio di codice seguente:


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHING,
                     TRUE,
                     0,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE);
SystemParametersInfo(SPI_SETFONTSMOOTHINGTYPE,
                     0,
                     (PVOID)FE_FONTSMOOTHINGCLEARTYPE,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



È possibile modificare l'aspetto del testo modificando il valore di contrasto usato nell'algoritmo ClearType. Il valore predefinito è 1.400, ma può essere qualsiasi valore compreso tra 1.000 e 2.200. A seconda del dispositivo di visualizzazione e della sensibilità dell'utente ai colori, un valore di contrasto superiore o inferiore può migliorare la leggibilità. Per modificare il contrasto, chiamare [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ SETFONTSMOOTHINGCONTRAST. Il codice seguente imposta il valore di contrasto su 1.600.


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



Per la compatibilità delle applicazioni, è necessario considerare i seguenti dettagli:

-   Il rendering del testo con ClearType è leggermente più lento rispetto all'anti-aliasing standard.
-   Le applicazioni non devono utilizzare XOR per visualizzare il testo selezionato. Le applicazioni devono impostare il colore di sfondo e visualizzare nuovamente il testo selezionato.
-   Le applicazioni non devono disegnare lo stesso testo in modalità trasparente. In tal caso, i pixel perimetrali con antialias verranno colorati con se stessi anziché con il colore di sfondo. In questo modo si ottiene un bordo oscurato e colorato.
-   Le applicazioni non devono disegnare il testo disegnando i caratteri singolarmente in modalità opaca poiché il bordo di un carattere può essere ritagliato in base al carattere seguente. Questo problema si verifica perché un carattere smussato con ClearType può avere una larghezza negativa A o C, dove il carattere regolare ha una larghezza positiva A o C. È garantita solo la larghezza B del carattere. Analogamente, le applicazioni devono prestare attenzione se il testo smussato è prossimo al testo non uniforme.
-   Se un'applicazione esegue il rendering del testo e quindi modifica la bitmap, la smussatura dei caratteri deve essere disattivata impostando il membro **lfQuality** della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) sulla \_ qualità NONANTIALIASED. Ad esempio, un gioco può aggiungere un effetto ombreggiatura bitmap oppure il testo di cui è stato eseguito il rendering in una bitmap può essere ridimensionato per produrre un ThumbView.
-   Se l'utente è in esecuzione in modalità verticale (ovvero lo striping di monitoraggio è orizzontale), l'anti-aliasing ClearType dovrebbe essere disabilitato.

Il parametro *fdwQuality* in [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) e il membro **lfQuality** di [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) accettano il flag di \_ qualità CLEARTYPE. La rasterizzazione dei tipi di carattere creati con questo flag utilizzerà l'rasterizzatore ClearType. Questo flag non ha alcun effetto sulle versioni precedenti del sistema operativo.

 

 
