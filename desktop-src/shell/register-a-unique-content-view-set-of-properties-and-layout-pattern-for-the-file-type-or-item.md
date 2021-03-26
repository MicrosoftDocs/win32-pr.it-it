---
description: È possibile registrare un elenco di proprietà di visualizzazione contenuto univoco e il modello di layout per il tipo di file o l'elemento.
ms.assetid: EA5A3ADA-4DFD-4F85-A176-93577D822815
title: Registrare un set di visualizzazioni contenuto di proprietà e pattern di layout per un tipo di file o un elemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e84861a0761f2f5ebb9737f62409c8f72e00bd
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104350801"
---
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a>Come registrare un set di visualizzazioni di contenuto univoco di proprietà e pattern di layout per il tipo di file o l'elemento

È possibile registrare un elenco di proprietà di visualizzazione contenuto univoco e il modello di layout per il tipo di file o l'elemento. Se il tipo di file o l'elemento è associato anche a un tipo, la registrazione della visualizzazione contenuto specifica del tipo di file o dell'elemento eseguirà l'override della registrazione del tipo. Questo può essere utile se le proprietà più importanti di questo elemento sono diverse da quelle di altri elementi dello stesso tipo. Se non si associa il tipo di file o l'elemento a un tipo di elemento o si registra direttamente la visualizzazione contenuto, il sistema utilizza le informazioni di visualizzazione del contenuto predefinite (archiviate in una chiave del registro di sistema a cui fa riferimento l'ultimo elemento di tutti gli elementi ' array di associazione, HKEY \_ classi \_ radice \\ \* )

Prima di registrare un elenco di proprietà personalizzato per il tipo di file, è necessario comprendere la modalità di ricerca e la modalità di visualizzazione dei risultati e i modelli di layout disponibili.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a>Passaggio 1: informazioni sulla modalità di visualizzazione e visualizzazione dei risultati della ricerca

Per la visualizzazione contenuto è necessario definire un modello di layout e un set di elenchi di proprietà per un elemento in un set di risultati di ricerca (modalità risultato ricerca) e quando si passa a una posizione della shell (modalità Browse). È possibile usare gli stessi valori per i risultati della ricerca e l'esplorazione, così come sono `Kind.Music` . In alternativa, è possibile definire un elenco di proprietà e/o un modello di layout diverso `Kind.Document` .

Nel caso di `Kind.Document` , gli utenti spesso cercano parole nel testo del documento. Pertanto, l'inclusione di più testo di esempio nel risultato della ricerca potrebbe essere la scelta migliore. Nell'esempio seguente viene illustrata la visualizzazione contenuto di Esplora `Kind.Document` .

![sfogliare la visualizzazione contenuto di kind.document](images/content-view/browsecontentviewkinddocument.png)

Poiché gli utenti cercano raramente un particolare testo quando si esplorano i documenti, l'ottimizzazione della scelta delle proprietà e del layout per adattare più risultati della ricerca sullo schermo potrebbe essere la scelta migliore. Lo screenshot seguente illustra la visualizzazione del contenuto di ricerca di `Kind.Document` .

### <a name="step-2-understanding-layout-patterns"></a>Passaggio 2: informazioni sui modelli di layout

Sono disponibili quattro modelli di layout: Alpha, beta, gamma e Delta.

**Layout alfa**

Il modello di layout alfa è ottimizzato per i risultati della ricerca di documenti che contengono estratti. Include le specifiche seguenti:

-   Righe: 4
-   Proprietà: 7
-   Layout alfa quando l'elemento ha 350 pixel o più di spazio orizzontale, come illustrato nella figura seguente.

    ![schema di layout Alpha](images/content-view/layout1.png)

-   Nella figura seguente viene illustrato il layout alfa quando l'elemento ha 350 pixel o più di spazio orizzontale.

    ![Diagramma che mostra un esempio di layout alfa](images/content-view/alphaviewmore.png)

-   Nella figura seguente viene illustrato il layout alfa quando l'elemento ha meno di 350 pixel di spazio orizzontale.

    ![Screenshot che mostra un esempio di layout alfa in Microsoft Word.](images/content-view/layout2.png)

-   Nella figura seguente viene illustrato il layout alfa quando l'elemento ha meno di 350 pixel di spazio orizzontale.

    ![esempio di layout alfa](images/content-view/alphaviewless.png)

**Layout beta**

Il modello di layout beta è ottimizzato per i risultati della ricerca dei documenti di posta elettronica che contengono estratti. Include le specifiche seguenti:

-   Righe: 4
-   Proprietà: 5
-   Layout beta quando l'elemento ha 350 pixel o più di spazio orizzontale, come illustrato nella figura seguente.

    ![Diagramma che mostra un esempio di layout beta.](images/content-view/layout3.png)

-   Nella figura seguente viene illustrato il layout beta quando l'elemento ha 350 pixel o più di spazio orizzontale.

    ![Screenshot che mostra un esempio di layout beta per la posta elettronica.](images/content-view/betaviewmore.png)

-   Nella figura seguente viene illustrato il layout beta quando l'elemento ha meno di 350 pixel di spazio orizzontale.

    ![Diagramma che mostra un esempio di layout beta con meno di 350 pixel di spazio orizzontale.](images/content-view/layout4.png)

-   La figura seguente mostra il layout beta quando l'elemento ha meno di 350 pixel di spazio orizzontale:

    ![esempio di layout beta](images/content-view/betaviewless.png)

**Layout gamma**

Il modello di layout gamma è simile a alfa ma usa un layout a due righe anziché quattro. Questo layout è ideale per gli scenari in cui si desidera visualizzare un frammento, ma si desidera inserire più elementi sullo schermo o per i tipi di file che richiedono meno spazio per visualizzare le informazioni più importanti. Il layout gamma presenta le specifiche seguenti:

-   Righe: 2
-   Proprietà: 4
-   La figura seguente mostra il layout gamma quando l'elemento ha 350 pixel o più di spazio orizzontale.

    ![Diagramma che mostra un esempio di layout gamma.](images/content-view/layout5.png)

-   La figura seguente mostra il layout gamma quando l'elemento ha 350 pixel o più di spazio orizzontale.

    ![Screenshot che mostra un esempio di layout gamma per un elemento dell'elenco di controllo.](images/content-view/gammaviewmore.png)

-   La figura seguente mostra il layout gamma quando l'elemento ha meno di 350 pixel di spazio orizzontale.

    ![Diagramma che mostra un esempio di layout gamma con meno di 350 pixel di spazio orizzontale.](images/content-view/layout6.png)

-   Esempio di layout gamma quando l'elemento ha meno di 350 pixel di spazio orizzontale.

    ![esempio di layout gamma](images/content-view/gammaviewless.png)

**Layout Delta**

Il modello di layout Delta è ottimizzato per la visualizzazione di molte proprietà più brevi, ad esempio per musica e immagini. Include le specifiche seguenti:

-   Righe: 2
-   Proprietà: 6
-   Layout Delta quando l'elemento ha 700 pixel o più di spazio orizzontale, come illustrato nella figura seguente.

    ![Diagramma che mostra un esempio di layout Delta.](images/content-view/layout7.png)

-   Esempio di layout Delta quando l'elemento ha 700 pixel o più di spazio orizzontale.

    ![Screenshot che mostra un esempio di layout Delta per un file musicale.](images/content-view/deltalayoutmore.png)

-   Layout Delta quando l'elemento ha una lunghezza compresa tra 350 e 700 pixel di spazio orizzontale.

    ![Diagramma che mostra un esempio di layout Delta con una lunghezza compresa tra 350 e 700 pixel di spazio orizzontale.](images/content-view/layout8.png)

-   Esempio di layout Delta quando l'elemento ha una lunghezza compresa tra 350 e 700 pixel di spazio orizzontale.

    ![esempio di layout Delta](images/content-view/deltaviewbetween.png)

-   Layout Delta quando l'elemento ha meno di 350 pixel di spazio orizzontale.

    ![esempio di layout](images/content-view/layout9.png)

-   Esempio di layout Delta quando l'elemento ha meno di 350 pixel di spazio orizzontale.

    ![Screenshot che mostra un esempio di layout Delta per un file musicale con meno di 350 pixel di spazio orizzontale.](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a>Passaggio 3: registrazione delle proprietà personalizzate e del layout per il tipo di file

Dopo aver compreso la modalità dei risultati della ricerca, la modalità browse e i modelli di layout, è possibile registrare un elenco di proprietà personalizzato per il tipo di file.

**Per registrare un elenco di proprietà e un modello di layout personalizzati per il tipo di file.**

1.  Scegliere tra i quattro modelli di layout: Alpha, beta, gamma o Delta.
2.  Prendere in considerazione le seguenti regole di formattazione che si applicano ugualmente a tutti e quattro i modelli di layout:
    -   La proprietà 1 viene sempre visualizzata in dimensioni maggiori. Dimensioni del carattere di grandi dimensioni generalmente utilizzate per il nome dell'elemento, ma possono essere utilizzate anche per la proprietà ancoraggio o altro elemento.
    -   La proprietà 4 è destinata agli estratti nei modelli di layout Alpha, beta e gamma. Questa proprietà è assegnata più spazio in tali modelli e viene visualizzata in un colore grigio, invece che in nero come le altre proprietà, per consentirne l'emergere.
    -   Le misurazioni dei pixel indicate di seguito si trovano in pixel relativi e le dimensioni includono l'icona o l'anteprima a sinistra delle proprietà e lo spazio tra l'icona e l'anteprima e il rettangolo di selezione.
    -   La maggior parte delle proprietà ha una dimensione di visualizzazione minima. Pertanto, non verranno visualizzati se lo spazio disponibile non è sufficiente a una determinata dimensione di visualizzazione. La dimensione minima è in genere di 100 pixel.
    -   Ogni schema di layout definisce il numero di righe e il numero di proprietà in ogni riga.
3.  Decidere quali proprietà si desidera visualizzare nel layout e quale proprietà si desidera visualizzare in ogni posizione. Quando si decide quale proprietà visualizzare in ogni posizione nel layout, prendere in considerazione la lunghezza tipica della proprietà, la sua importanza per l'utente e se deve essere eliminata quando la dimensione della finestra è troppo piccola per contenere tutte le proprietà.
4.  Registrare un modello di layout e un elenco di proprietà per il tipo di file o per il tipo di elemento aggiungendo le seguenti chiavi sotto la chiave del registro di sistema ProgID per il tipo di file o l'elemento (in questo esempio, per il tipo di file xyz).

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  Osservare le linee guida di formattazione seguenti per la registrazione delle proprietà:

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

    I valori possibili per (ContentViewModeForBrowse) includono i seguenti: prop: ~ System. ItemNameDisplay; System. Author; System. LayoutPattern. segnaposto; System. Keywords; System. DateModified; ~ System. size

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di file](fa-file-types.md)
</dt> <dt>

[Nomi dei tipi](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[System. Propin. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[System. Propin. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
