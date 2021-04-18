---
description: Dopo aver compreso la modalità dei risultati della ricerca, la modalità browse e i modelli di layout, è possibile registrare un elenco di proprietà personalizzato per il tipo di file. Per registrare un elenco di proprietà e un modello di layout personalizzati per il tipo di file, seguire questa procedura.
ms.assetid: 29B863B3-E5FD-4E0A-B76B-4AFE5A6A76E3
title: Come registrare le proprietà personalizzate e il layout per il tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da55d0a90d4dd0f3ca109a3ca9f628a3c0912520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994661"
---
# <a name="how-to-register-custom-properties-and-layout-for-your-file-type"></a>Come registrare le proprietà personalizzate e il layout per il tipo di file

Dopo aver compreso la modalità dei risultati della ricerca, la modalità browse e i modelli di layout, è possibile registrare un elenco di proprietà personalizzato per il tipo di file.

Per registrare un elenco di proprietà e un modello di layout personalizzati per il tipo di file, seguire questa procedura.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Scegliere tra i quattro modelli di layout: Alpha, beta, gamma o Delta.

### <a name="step-2"></a>Passaggio 2:

Prendere in considerazione le seguenti regole di formattazione che si applicano ugualmente a tutti e quattro i modelli di layout:

-   La proprietà 1 viene sempre visualizzata in dimensioni maggiori. Dimensioni del carattere di grandi dimensioni generalmente utilizzate per il nome dell'elemento, ma possono essere utilizzate anche per la proprietà ancoraggio o altro elemento.
-   La proprietà 4 è destinata agli estratti nei modelli di layout Alpha, beta e gamma. Questa proprietà è assegnata più spazio in tali modelli e viene visualizzata in un colore grigio, invece che in nero come le altre proprietà, per consentirne l'emergere.
-   Le misurazioni dei pixel indicate di seguito si trovano in pixel relativi e le dimensioni includono l'icona o l'anteprima a sinistra delle proprietà e lo spazio tra l'icona e l'anteprima e il rettangolo di selezione.
-   La maggior parte delle proprietà ha una dimensione di visualizzazione minima. Pertanto, non verranno visualizzati se lo spazio disponibile non è sufficiente a una determinata dimensione di visualizzazione. La dimensione minima è in genere di 100 pixel.
-   Ogni schema di layout definisce il numero di righe e il numero di proprietà in ogni riga.

### <a name="step-3"></a>Passaggio 3:

Decidere quali proprietà si desidera visualizzare nel layout e quale proprietà si desidera visualizzare in ogni posizione. Quando si decide quale proprietà visualizzare in ogni posizione nel layout, prendere in considerazione la lunghezza tipica della proprietà, la sua importanza per l'utente e se deve essere eliminata quando la dimensione della finestra è troppo piccola per contenere tutte le proprietà.

### <a name="step-4"></a>Passaggio 4:

Registrare un modello di layout e un elenco di proprietà per il tipo di file o per il tipo di elemento aggiungendo le seguenti chiavi sotto la chiave del registro di sistema ProgID per il tipo di file o l'elemento (in questo esempio, per il tipo di file xyz).

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
-   `~System.LayoutPattern.PlaceHolder` usare se si vuole lasciare vuota una proprietà specificata nel modello di layout.

La chiave del registro di sistema di esempio seguente illustra queste linee guida per la formattazione.

```
HKEY_CLASSES_ROOT\
   Kind.Document
      (ContentViewModeForBrowse) = <PropertyList>
```

I valori possibili per (ContentViewModeForBrowse) includono i seguenti: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`

 

 



