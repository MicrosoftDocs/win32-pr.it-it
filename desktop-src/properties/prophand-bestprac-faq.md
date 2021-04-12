---
description: In questo argomento viene illustrato come creare e registrare gestori di proprietà per utilizzare il sistema di proprietà di Windows.
ms.assetid: E583A00B-F615-41c8-AECF-061F1396DB9A
title: Procedure consigliate e domande frequenti sul gestore delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5188e66f08f3c6cf449f8bc61feb6aac829d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233607"
---
# <a name="property-handler-best-practices-and-faq"></a>Procedure consigliate e domande frequenti sul gestore delle proprietà

In questo argomento viene illustrato come creare e registrare gestori di proprietà per utilizzare il sistema di proprietà di Windows.

Questo argomento è organizzato nel modo seguente:

-   [Procedure consigliate](#property-handler-best-practices-and-faq)
    -   [Override delle proprietà del file System](#overriding-file-system-properties)
    -   [Archiviazione di proprietà nei formati di file basati su XML](#storing-properties-in-xml-based-file-formats)
    -   [Proprietà calcolate](#computed-properties)
-   [Domande frequenti](#property-handler-best-practices-and-faq)
-   [Argomenti correlati](#related-topics)

## <a name="best-practices"></a>Procedure consigliate

Le procedure consigliate illustrate di seguito forniscono suggerimenti utili per l'implementazione.

### <a name="overriding-file-system-properties"></a>Override delle proprietà del file System

Alcune proprietà dei file vengono fornite dall'origine dati file system, ad esempio:

-   \_Nome file pkey
-   \_Estensione pkey
-   \_MODIFIEDTIME pkey

In generale, i gestori di proprietà non possono fornire valori per queste proprietà. Tuttavia, in alcuni casi è possibile eseguire l'override di queste proprietà in base alle informazioni di registrazione fornite dal gestore della proprietà. I gestori di proprietà popolano le **classi HKEY CLSID \_ \_ radice** \\  \\ *{handler CLSID}* \\ **OverrideFileSystemProperties** con i nomi delle proprietà di cui si desidera eseguire l'override. Questa operazione è limitata a un set fisso di proprietà mostrato nell'elenco seguente di cui il sistema ha la conoscenza.

L'override di è supportato per i valori di proprietà seguenti:

-   [System. Kind](./props-system-kind.md)
-   [System. FileName](./props-system-filename.md)
-   [System. IsPinnedToNameSpaceTree](./props-system-ispinnedtonamespacetree.md)
-   [System.ItemNameDisplay](./props-system-itemnamedisplay.md)
-   [System. SFGAOFlags](./props-system-sfgaoflags.md)
-   [System. ItemPathDisplay](./props-system-itempathdisplay.md)
-   [System. ItemPathDisplayNarrow](./props-system-itempathdisplaynarrow.md)
-   [System. ItemFolderNameDisplay](./props-system-itemfoldernamedisplay.md)
-   [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md)
-   [System. ItemFolderPathDisplayNarrow](./props-system-itemfolderpathdisplaynarrow.md)

Per un elenco completo di tutte le proprietà della shell, vedere [Proprietà](./props.md)della shell.

> [!IMPORTANT]
> I valori delle proprietà sottoposti a override vengono utilizzati solo quando i file vengono indicizzati. Di conseguenza, l'esplorazione dei file dall'origine dati file system non rivela i valori sottoposti a override.

 

### <a name="storing-properties-in-xml-based-file-formats"></a>Archiviazione di proprietà nei formati di file basati su XML

Sono disponibili due opzioni di base per archiviare le proprietà nei formati di file basati su XML:

-   Archiviare ogni proprietà usando gli elementi e gli attributi XML in base all'XML Schema del documento. Questo approccio è più "XML friendly".
-   Serializzare l'intero archivio delle proprietà in un BLOB (Binary Large Object) di memoria, convertire il BLOB in una stringa con codifica Base64 e quindi archiviare tale stringa nel codice XML. Questo è il più semplice dei due approcci e può essere usato per fornire il supporto per i metadati aperti.

Alcuni gestori potrebbero combinare questi approcci, archiviando alcuni valori importanti nel formato XML standard e archiviando il resto in un BLOB, ad esempio.

### <a name="computed-properties"></a>Proprietà calcolate

Alcune proprietà derivano da attributi specifici di un file. Ad esempio, la proprietà [System. image. Dimensions](./props-system-image-dimensions.md) è determinata dalle dimensioni effettive dell'immagine in un file di immagine. Poiché tali valori di proprietà non possono essere modificati dal gestore della proprietà, sono contrassegnati `isInnate="true"` nella descrizione della proprietà. Altre proprietà vengono calcolate da una parte di una proprietà specifica o aggregando i valori di più proprietà. Poiché gli aggiornamenti a queste proprietà "calcolate" creeranno ambiguità sulla modalità di modifica dei valori di "origine", le proprietà calcolate dovrebbero essere contrassegnate `isInnate="true"` nella descrizione della proprietà o restituite come di sola lettura. La seconda opzione è disponibile indicando al gestore di restituire \_ false da [**IPropertyStoreCapabilities:: IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable).

## <a name="frequently-asked-questions"></a>Domande frequenti

In questa sezione vengono fornite le risposte alle domande frequenti relative alle proprietà e ai gestori di proprietà e alle risposte correlate.

-   **Domanda:** Perché il gestore delle proprietà non viene caricato dall'indicizzatore di ricerca di Windows?

    L'indicizzatore di ricerca di Windows viene eseguito come servizio di sistema e non è in grado di caricare le dll archiviate nella directory del profilo utente. Se si compila e si esegue il debug con Microsoft Visual Studio, il file verrà inserito nel profilo utente e pertanto non verrà caricato dall'indicizzatore. Per ovviare a questo problema, copiare la DLL all'esterno della cartella del profilo, ad esempio in **C: \\ Program Files \\ YourAppName**, e registrarla in tale cartella.

    Per indicazioni più specifiche sullo sviluppo di gestori di proprietà per lavorare con l'indicizzatore di ricerca di Windows, vedere [sviluppo di gestori di proprietà per la ricerca di Windows](../search/-search-3x-wds-extidx-propertyhandlers.md).

-   **Domanda:** Quali proprietà devono essere individuabili tramite i metodi di enumerazione [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore:: Geta**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) ?

    Non tutti i client degli oggetti archivio proprietà utilizzano questi metodi. Alcuni client sono in grado di riconoscere le proprietà che prevedono di richiedere direttamente (in base al nome PKEY) o di ricevere informazioni sulle proprietà tramite un elenco di descrizioni di proprietà. I metodi di individuazione delle proprietà supporto diversi altri scenari. Se non è necessario che una proprietà partecipi a questi scenari, non è necessario che venga enumerata. Di conseguenza, un gestore proprietà può produrre un \_ valore vuoto non VT per le proprietà che non vengono individuate tramite i metodi [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore:: Geta**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) .

    Tuttavia, le proprietà devono essere visibili tramite questi metodi se viene soddisfatta una delle condizioni seguenti:

    -   **Se la proprietà è indicizzata in modo che sia ricercabile:** Ciò significa che è incluso nell'archivio delle proprietà di ricerca di Windows (indicato da `isColumn = "true"` nello schema della descrizione della proprietà) o disponibile per le ricerche full-text ( `inInvertedIndex = "true"` ). In assenza di questi flag o dell'assenza di una descrizione della proprietà, le proprietà di tipo "String" verranno aggiunte automaticamente all'indice invertito per consentire la ricerca. Poiché l'elenco delle proprietà note (quelle con le descrizioni delle proprietà installate) nel sistema di proprietà è molto grande (più di 800 proprietà), non sarebbe pratico chiedere a ogni gestore di proprietà di ogni proprietà registrata nel sistema di proprietà. Al contrario, il processo di indicizzazione enumera le proprietà rilevanti dal gestore delle proprietà per ogni elemento indici e usa i valori delle proprietà enumerate per compilare l'indice full-text.
    -   **Se la proprietà deve essere copiata quando il set di proprietà dell'elemento viene duplicato:** Per implementare una funzione "copia set di proprietà", l'elemento di origine rende visibili le proprietà che devono essere copiate tramite i metodi [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore:: Geta**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) . Non è necessario includere le proprietà che non devono essere copiate o che non hanno senso di essere copiate.
    -   **Se il valore della proprietà non è vuoto (VT \_ vuoto):** i valori di proprietà vuoti non sono utili per i client. Quando i client tentano di restituire valori di proprietà vuoti, viene restituito il valore VT \_ Empty. Pertanto, le proprietà con valori vuoti non devono essere enumerate.
    -   **Se la proprietà deve essere rimossa quando si richiama la funzione "Rimuovi proprietà":** Questa funzionalità è disponibile per proteggere la privacy. individua tutti i valori dal gestore delle proprietà tramite l'enumerazione e rimuove ognuno di essi selezionati per la rimozione da parte dell'utente.
        > [!Note]  
        > L'enumerazione delle proprietà non comunica il set di proprietà supportato da un particolare gestore di proprietà se il gestore supporta uno schema fisso (e non i metadati aperti). Al contrario, questi gestori dovrebbero documentare il set di proprietà supportate.

         

-   **Domanda:** Ricerca per categorie informazioni sui formati di file che supportano i metadati aperti?

    Per informazioni sul supporto per i metadati aperti, vedere la sezione relativa ai tipi di file che supportano i metadati aperti in [tipi di file](../shell/fa-file-types.md).

-   **Domanda:** È possibile \_ archiviare i valori null del VT usando un gestore proprietà?

    No. \_I valori null VT verranno convertiti in VT \_ vuoti per le chiamate a [**IPropertyStore:: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)) e [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

-   **Domanda:** Quali formati di stringa di data sono supportati dalla funzione [**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) ?

    In genere, le proprietà che rappresentano i valori di data/ora devono essere rappresentate utilizzando il \_ FILETIME VT. Tuttavia, molte origini dati forniscono queste informazioni in formato stringa. L'API helper [**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) supporta la coercizione di alcuni formati di data stringa in valori [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) , come illustrato nella tabella seguente.

    

    | Formato                  | Windows Vista, Windows XP e Microsoft Windows Desktop Search (WDS) | Windows 7 | Note                                                                                                                                                                                                 |
    |-------------------------|-----------------------------------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | aaaa/mm/gg: HH: mm: SS. UUU | Sì                                                                   | Sì       | UTC y = anno, m = mese, d = data, h = ore (orario a 24 ore), m = minuti, s = secondi, u = microsecondi                                                                                                           |
    | aaaa-mm-ggThh: mm: ssZ    | No                                                                    | Sì       | **Specifica del formato ISO8601** UTC (indicata dall'indicatore di fuso orario ' Z '); y = anno, m = mese, d = data, h = ore (orario a 24 ore), m = minuti, s = secondi; ' T'è un delimitatore per la parte relativa all'ora.<br/> |

    

     

-   **Domanda:** È possibile creare un gestore di proprietà di sola lettura?

    Sì. Alcune implementazioni di gestori di proprietà non supportano la scrittura di valori di proprietà. Questi gestori di proprietà devono restituire STGM \_ E \_ AccessDenied sulle chiamate a **IInitializeXXX:: Initialize** che passano STGM \_ ReadWrite o su qualsiasi chiamata a [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

    Tutti i gestori di proprietà aperti in \_ modalità di lettura STGM devono restituire STGM \_ E \_ AccessDenied sulle chiamate a [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

-   **Domanda:** Un gestore di proprietà può considerare una proprietà come di sola lettura, anche se lo schema indica che la proprietà è scrivibile?

    Sì. Nel sistema dello schema le proprietà sono annotate come di sola lettura (incluse quelle con `isInnate = "true"` ) o di lettura/scrittura. I gestori di proprietà che non supportano la scrittura di una proprietà specifica che lo schema deve essere scrivibile devono implementare [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) e restituire \_ false sulle chiamate a [**IPropertyStoreCapabilities:: IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) per la proprietà. Ciò indica che nel contesto di questo gestore e questo file la proprietà non è scrivibile.

    > [!Note]  
    > L'azione inversa non è possibile. Non è possibile abilitare un gestore di proprietà per la scrittura di una proprietà contrassegnata come di sola lettura nello schema

     

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui gestori delle proprietà](./building-property-handlers-properties.md)
</dt> <dt>

[Uso dei nomi dei tipi](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Uso degli elenchi di proprietà](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inizializzazione di gestori di proprietà](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md)
</dt> </dl>

 

 
