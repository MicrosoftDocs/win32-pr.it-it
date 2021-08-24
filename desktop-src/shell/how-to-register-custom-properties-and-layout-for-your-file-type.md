---
description: Dopo aver compreso la modalità Risultato della ricerca, la modalità Sfoglia e i modelli di layout, è possibile registrare un elenco di proprietà personalizzate per il tipo di file. Per registrare un elenco di proprietà personalizzate e un modello di layout per il tipo di file, seguire questa procedura.
ms.assetid: 29B863B3-E5FD-4E0A-B76B-4AFE5A6A76E3
title: Come registrare proprietà personalizzate e layout per il tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9388965a781d4104ae13de689b72208a8b69e213a758c9b34552c03bb938453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714901"
---
# <a name="how-to-register-custom-properties-and-layout-for-your-file-type"></a>Come registrare proprietà personalizzate e layout per il tipo di file

Dopo aver compreso la modalità Risultato della ricerca, la modalità Sfoglia e i modelli di layout, è possibile registrare un elenco di proprietà personalizzate per il tipo di file.

Per registrare un elenco di proprietà personalizzate e un modello di layout per il tipo di file, seguire questa procedura.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Scegliere uno dei quattro modelli di layout: Alpha, Beta, Gamma o Delta.

### <a name="step-2"></a>Passaggio 2:

Si considerino le regole di formattazione seguenti, che si applicano in modo uniforme a tutti e quattro i modelli di layout:

-   La proprietà 1 viene sempre visualizzata con dimensioni del carattere maggiori. La dimensione del carattere di grandi dimensioni usata in genere per il nome dell'elemento, ma può essere usata anche per l'ancoraggio o per altre proprietà dell'elemento.
-   La proprietà 4 è destinata agli estratti nei modelli di layout Alfa, Beta e Gamma. Questa proprietà ha più spazio in questi modelli e viene visualizzata in un colore grigio del carattere, a differenza del nero come le altre proprietà, per distinguerlo.
-   Le misure in pixel seguenti sono in pixel relativi e le dimensioni includono l'icona/anteprima a sinistra delle proprietà e lo spazio tra l'icona/anteprima e il rettangolo di selezione.
-   La maggior parte delle proprietà ha una dimensione di visualizzazione minima. Pertanto, non verranno visualizzati se non è disponibile spazio sufficiente per le dimensioni di visualizzazione specifiche. La dimensione minima è in genere di 100 pixel.
-   Ogni modello di layout definisce il numero di righe e il numero di proprietà in ogni riga.

### <a name="step-3"></a>Passaggio 3:

Decidere le proprietà da visualizzare nel layout e la proprietà da visualizzare in ogni posizione. Quando si decide quale proprietà visualizzare in ogni posizione nel layout, considerare la lunghezza tipica della proprietà, la sua importanza per l'utente e se deve essere eliminata quando le dimensioni della finestra sono troppo piccole per contenere tutte le proprietà.

### <a name="step-4"></a>Passaggio 4:

Registrare un modello di layout e un elenco di proprietà per il tipo di file o l'elemento aggiungendo le chiavi seguenti nella chiave del Registro di sistema ProgID per il tipo di file o l'elemento (in questo esempio, per il tipo di file con estensione xyz).

```
HKEY_CLASSES_ROOT\*
   Contoso.xyzfile
      (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
      (ContentViewModeLayoutPatternForSearch) = <PropertyList>
```

### <a name="step-5"></a>Passaggio 5:

Osservare le linee guida di formattazione seguenti per la registrazione delle proprietà:

-   Ogni registrazione inizia con `prop:`
-   Ogni proprietà richiede il nome completo della proprietà.
-   Le proprietà sono separate da un punto e virgola senza spazio.
-   Le proprietà vengono visualizzate nell'ordine definito dal modello di layout selezionato.
-   `~` indica che l'etichetta della proprietà non deve essere visualizzata.
-   `~System.LayoutPattern.PlaceHolder` deve essere usato se si vuole lasciare vuota una proprietà specificata nel modello di layout.

La chiave del Registro di sistema di esempio seguente illustra queste linee guida di formattazione.

```
HKEY_CLASSES_ROOT\
   Kind.Document
      (ContentViewModeForBrowse) = <PropertyList>
```

I valori possibili per (ContentViewModeForBrowse) includono i seguenti: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`

 

 



