---
description: L'antialiasing Microsoft ClearType è un metodo di smussamento che migliora la risoluzione dello schermo dei caratteri rispetto all'antialiasing tradizionale.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: ClearType Antialiasing (Anti-aliasing ClearType)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc8444c1e1b594559f9c5b7f96529a0db00b20c6a10e560bc1dcb4574e079d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117888096"
---
# <a name="cleartype-antialiasing"></a>ClearType Antialiasing (Anti-aliasing ClearType)

L'antialiasing Microsoft ClearType è un metodo di smussamento che migliora la risoluzione dello schermo dei caratteri rispetto all'antialiasing tradizionale. Migliora notevolmente la leggibilità sui monitor LCD a colori con un'interfaccia digitale, ad esempio quelli in portatili e schermi desktop flat di alta qualità. Anche la leggibilità nelle schermate CRT è leggermente migliorata.

ClearType dipende tuttavia dall'orientamento e dall'ordinamento delle strisce LCD. Attualmente ClearType viene implementato solo per le unità LCD con strisce verticali ordinate RGB. In particolare, questo influisce sui PC tablet, in cui lo schermo può essere orientato in qualsiasi direzione e le schermate che possono essere trasformate da orizzontale a verticale.

L'anti-aliasing ClearType è consentito:

-   Per i colori a 16, 24 e 32 bit (disabilitati per 256 colori o meno)
-   Per il controller di dominio dello schermo e il controller di dominio di memoria (non per il controller di dominio della stampante)
-   Per i tipi di carattere TrueType e i tipi di carattere OpenType con strutture TrueType

L'anti-aliasing ClearType è disabilitato:

-   Nel client del server terminal
-   Per i tipi di carattere bitmap, i tipi di carattere vettoriali, i tipi di carattere del dispositivo, i tipi di carattere Di tipo 1 o i tipi di carattere Postscript OpenType senza strutture TrueType
-   Se il tipo di carattere dispone di bitmap incorporate ottimizzate, solo per le dimensioni dei caratteri che contengono le bitmap incorporate

Per attivare l'antialiasing ClearType, chiamare [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) una volta per attivare lo smussamento dei caratteri e quindi una seconda volta per impostare il tipo di smussamento su FE FONTSMOOTHINGCLEARTYPE, come illustrato nell'esempio di codice \_ seguente:


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



È possibile regolare l'aspetto del testo modificando il valore di contrasto usato nell'algoritmo ClearType. Il valore predefinito è 1.400, ma può essere qualsiasi valore compreso tra 1.000 e 2.200. A seconda del dispositivo di visualizzazione e della sensibilità dell'utente ai colori, un valore di contrasto superiore o inferiore può migliorare la leggibilità. Per modificare il contrasto, [**chiamare SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ SETFONTSMOOTHINGCONTRAST. Il codice seguente imposta il valore di contrasto su 1.600.


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



È consigliabile considerare i dettagli seguenti per la compatibilità delle applicazioni:

-   Il rendering del testo con ClearType è leggermente più lento rispetto all'anti-aliasing standard.
-   Le applicazioni non devono usare XOR per visualizzare il testo selezionato. Le applicazioni devono impostare il colore di sfondo e visualizzare nuovamente il testo selezionato.
-   Le applicazioni non devono disegnare lo stesso testo sopra se stesso in modalità trasparente. In questo caso, i pixel del bordo con antialias verranno uniti con se stessi anziché con il colore di sfondo. Ciò comporta bordi scuri e colorati.
-   Le applicazioni non devono disegnare il testo disegnando i caratteri singolarmente in modalità opaca perché il bordo di un carattere può essere ritagliato dal carattere seguente. Ciò si verifica perché un carattere smussato con ClearType può avere una larghezza A o C negativa in cui il carattere regolare ha una larghezza A o C positiva. È garantito che solo la larghezza B del carattere sia la stessa. Analogamente, le applicazioni devono prestare attenzione se il testo smussato è accanto al testo non fumato.
-   Se un'applicazione esegue il rendering del testo e quindi modifica la bitmap, lo smussamento dei caratteri deve essere disattivato impostando il membro **lfQuality** della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) su NONANTIALIASED \_ QUALITY. Ad esempio, un gioco può aggiungere un effetto di ombreggiatura bitmap o il testo sottoposto a rendering in una bitmap può essere ridimensionato per produrre una visualizzazione del cursore.
-   Se l'utente è in esecuzione in modalità verticale,ovvero lo striping del monitoraggio è orizzontale, l'anti-aliasing ClearType deve essere disabilitato.

Il *parametro fdwQuality* in [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) e il membro **lfQuality** di [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) accettano il flag CLEARTYPE \_ QUALITY. La rasterizzazione dei tipi di carattere creati con questo flag userà l'rasterizzazione ClearType. Questo flag non ha alcun effetto sulle versioni precedenti del sistema operativo.

 

 
