---
description: Questo articolo include procedure consigliate e domande frequenti sulla creazione e la registrazione di gestori di proprietà da usare con il sistema di proprietà di Windows.
ms.assetid: E583A00B-F615-41c8-AECF-061F1396DB9A
title: Procedure consigliate e domande frequenti sul gestore delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5605c39f1021fcfe91259405bb99f8981510d3dc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405954"
---
# <a name="property-handler-best-practices-and-faq"></a>Procedure consigliate e domande frequenti sul gestore delle proprietà

Questo argomento illustra come creare e registrare gestori di proprietà da usare con il sistema di proprietà di Windows.

Questo argomento è organizzato come segue:

-   [Procedure consigliate](#property-handler-best-practices-and-faq)
    -   [Override delle proprietà del file system](#overriding-file-system-properties)
    -   [Archiviazione di proprietà in formati di file basati su XML](#storing-properties-in-xml-based-file-formats)
    -   [Proprietà calcolate](#computed-properties)
-   [Domande frequenti](#property-handler-best-practices-and-faq)
-   [Argomenti correlati](#related-topics)

## <a name="best-practices"></a>Procedure consigliate

Le procedure consigliate descritte di seguito offrono suggerimenti utili per l'implementazione.

### <a name="overriding-file-system-properties"></a>Override delle proprietà del file system

Alcune proprietà per i file vengono fornite dall'origine file system dati, ad esempio:

-   PKEY \_ FileName
-   Estensione \_ PKEY
-   PKEY \_ ModifiedTime

In generale, i gestori di proprietà non possono fornire valori per queste proprietà. Tuttavia, in alcuni casi queste proprietà possono essere sottoposte a override in base alle informazioni di registrazione fornite dal gestore delle proprietà. I gestori di proprietà popolano **HKEY \_ CLASSES \_ ROOT** \\ **CLSID** \\ *{handler clsid}* \\ **OverrideFileSystemProperties** con i nomi delle proprietà di cui vogliono eseguire l'override. Questo è limitato a un set fisso di proprietà illustrato nell'elenco seguente di cui il sistema dispone di informazioni.

L'override di è supportato per i valori di proprietà seguenti:

-   [System.Kind](./props-system-kind.md)
-   [System.FileName](./props-system-filename.md)
-   [System.IsPinnedToNameSpaceTree](./props-system-ispinnedtonamespacetree.md)
-   [System.ItemNameDisplay](./props-system-itemnamedisplay.md)
-   [System.SFGAOFlags](./props-system-sfgaoflags.md)
-   [System.ItemPathDisplay](./props-system-itempathdisplay.md)
-   [System.ItemPathDisplayNarrow](./props-system-itempathdisplaynarrow.md)
-   [System.ItemFolderNameDisplay](./props-system-itemfoldernamedisplay.md)
-   [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md)
-   [System.ItemFolderPathDisplayNarrow](./props-system-itemfolderpathdisplaynarrow.md)

Per un elenco completo di tutte le proprietà della shell, vedere [Proprietà della shell.](./props.md)

> [!IMPORTANT]
> I valori delle proprietà sottoposte a override vengono usati solo quando i file vengono indicizzati. Di conseguenza, l'esplorazione dei file file system'origine dati non rivela i valori sottoposti a override.

 

### <a name="storing-properties-in-xml-based-file-formats"></a>Archiviazione di proprietà in formati di file basati su XML

Sono disponibili due opzioni di base per l'archiviazione delle proprietà in formati di file basati su XML:

-   Archiviare ogni proprietà utilizzando elementi e attributi XML in base all'XML Schema del documento. Questo approccio è più "xml friendly".
-   Serializzare l'intero archivio delle proprietà in un BLOB (Binary large object) in memoria, convertire il BLOB in una stringa con codifica Base64 e quindi archiviare tale stringa nel codice XML. Questo è il più semplice dei due approcci e può essere usato per fornire in modo semplice il supporto per i metadati aperti.

Alcuni gestori potrebbero combinare questi approcci, archiviando alcuni valori importanti in formato XML standard e archiviando il resto in un BLOB, ad esempio.

### <a name="computed-properties"></a>Proprietà calcolate

Alcune proprietà derivano da attributi specifici di un file. Ad esempio, la [proprietà System.Image.Dimensions](./props-system-image-dimensions.md) è determinata dalle dimensioni effettive dell'immagine in un file di immagine. Poiché tali valori di proprietà non possono essere modificati dal gestore delle proprietà, vengono contrassegnati `isInnate="true"` nella descrizione della proprietà. Altre proprietà vengono calcolate da una parte di una proprietà specifica o aggregando i valori di più proprietà. Poiché gli aggiornamenti a queste proprietà "calcolate" creerebbe ambiguità sulla modalità di modifica dei valori di "origine", le proprietà calcolate devono essere contrassegnate nella descrizione della proprietà o segnalate come di sola `isInnate="true"` lettura. Quest'ultima opzione è disponibile indicando al gestore di restituire S FALSE da \_ [**IPropertyStoreCapabilities::IsPropertyWritable.**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable)

## <a name="frequently-asked-questions"></a>Domande frequenti

Questa sezione fornisce le risposte alle domande frequenti sulle proprietà e sui gestori di proprietà e le relative risposte.

-   **Domanda:** Perché il gestore delle proprietà non viene caricato dall'Windows Search indicizzatore?

    L Windows Search indicizzatore viene eseguito come servizio di sistema e non può caricare DLL archiviate nella directory del profilo utente. Se si compila e si esegue il debug usando Microsoft Visual Studio, la DLL verrà posizionata nel profilo utente e pertanto non verrà caricata dall'indicizzatore. Per risolvere questo problema, copiare la DLL all'esterno della cartella del profilo ( ad esempio, in **C: \\ Programmi \\ NomeApp**) e registrarla in tale cartella.

    Per indicazioni più specifiche sullo sviluppo di gestori di proprietà da usare con l'indicizzatore Windows Search, vedere Sviluppo di gestori di proprietà [per Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).

-   **Domanda:** Quali proprietà devono essere individuabili tramite i [**metodi di enumerazione IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore::GetAt?**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85))

    Non tutti i client degli oggetti archivio proprietà usano questi metodi. Alcuni client sono a conoscenza delle proprietà che pianificano di richiedere direttamente (in base al nome PKEY) o di ricevere informazioni sulle proprietà tramite un elenco di descrizione delle proprietà. I metodi di individuazione delle proprietà sopportano diversi altri scenari. Se non è necessario che una proprietà partecipi a questi scenari, non è necessario enumerarla. Di conseguenza, un gestore delle proprietà può produrre un valore non VT EMPTY per le proprietà che non vengono individuate tramite i metodi \_ [**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore::GetAt.**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85))

    Tuttavia, le proprietà devono essere visibili tramite questi metodi se viene soddisfatta una delle condizioni seguenti:

    -   **Se la proprietà è indicizzata in modo che sia disponibile per la ricerca:** Ciò significa che è incluso nell'Windows Search proprietà di ricerca (denotato da nello schema di descrizione della proprietà) o disponibile per le ricerche `isColumn = "true"` full-text ( `inInvertedIndex = "true"` ). In assenza di questi flag o in assenza di una descrizione della proprietà, le proprietà di tipo "string" verranno aggiunte automaticamente all'indice invertito per abilitare la ricerca. Poiché l'elenco delle proprietà note (quelle con descrizioni delle proprietà installate) nel sistema di proprietà è molto grande (più di 800 proprietà), sarebbe poco pratico chiedere a ogni gestore delle proprietà per ogni proprietà registrata nel sistema di proprietà. Al contrario, il processo di indicizzazione enumera le proprietà pertinenti dal gestore delle proprietà per ogni elemento indicizzato e usa i valori delle proprietà enumerate per compilare l'indice full-text.
    -   **Se la proprietà deve essere copiata quando il set di proprietà dell'elemento è duplicato:** Per implementare una funzione di "copia di un set di proprietà", l'elemento di origine rende visibili le proprietà che devono essere copiate tramite i metodi [**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore::GetAt.**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) Le proprietà che non devono essere copiate o che non hanno senso essere copiate non devono essere incluse.
    -   **Se il valore della proprietà non è vuoto (VT \_ EMPTY):** i valori delle proprietà vuoti non sono utili per i client. Quando i client tentano di restituire valori di proprietà vuoti, viene restituito un valore VT \_ EMPTY. Di conseguenza, le proprietà con valori vuoti non devono essere enumerate.
    -   **Se la proprietà deve essere rimossa quando si richiama la funzione "remove properties":** Questa funzionalità è disponibile per proteggere la privacy. individua tutti i valori dal gestore delle proprietà tramite l'enumerazione e rimuove ogni valore selezionato per la rimozione da parte dell'utente.
        > [!Note]  
        > L'enumerazione delle proprietà non comunica il set di proprietà supportate da un gestore di proprietà specifico se il gestore supporta uno schema fisso (e non i metadati aperti). Tali gestori devono invece documentare il set di proprietà supportate.

         

-   **Domanda:** Ricerca per categorie quali formati di file supportano i metadati aperti?

    Per informazioni sul supporto per i metadati aperti, vedere "Tipi di file che supportano metadati aperti" in [Tipi di file.](../shell/fa-file-types.md)

-   **Domanda:** I valori NULL VT \_ possono essere archiviati usando un gestore delle proprietà?

    No. I valori NULL VT verranno convertiti in VT EMPTY nelle chiamate \_ \_ a [**IPropertyStore::GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)) e [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

-   **Domanda:** Quali formati di stringa di data sono supportati [**dalla funzione PropVariantChangeType?**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype)

    In genere, le proprietà che rappresentano valori di data/ora devono essere rappresentate usando \_ FILETIME VT. Tuttavia, molte origini dati forniscono queste informazioni in formato stringa. L'API helper [**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) supporta la coesistenza di alcuni formati di data stringa in [**valori FILETIME,**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) come illustrato nella tabella seguente.

    

    | Formato                  | Windows Vista, Windows XP e Microsoft Windows Desktop Search (WDS) | Windows 7 | Note                                                                                                                                                                                                 |
    |-------------------------|-----------------------------------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | aaaa/mm/gg:hh:mm:ss.uuu | Sì                                                                   | Sì       | UTC; y=year, m=month, d=date, h=hours (formato a 24 ore), m=minuti, s=secondi, u=microsecondi                                                                                                           |
    | aaaa-mm-ggThh:mm:ssZ    | No                                                                    | Sì       | **Specifica di formato ISO8601** UTC (con l'indicatore del fuso orario 'Z'); y=year, m=month, d=date, h=hours (formato a 24 ore), m=minuti, s=secondi; 'T' è un delimitatore per la parte relativa all'ora.<br/> |

    

     

-   **Domanda:** È possibile creare un gestore di proprietà di sola lettura?

    Sì. Alcune implementazioni del gestore proprietà non supportano la scrittura di valori di proprietà. Questi gestori di proprietà devono restituire STGM E ACCESSDENIED nelle chiamate a \_ \_ **IInitializeXXX::Initialize** che passano STGM READWRITE o in qualsiasi chiamata a \_ [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

    Tutti i gestori di proprietà aperti in modalità STGM READ devono restituire STGM E ACCESSDENIED nelle chiamate \_ \_ a \_ [**IPropertyStore::SetValue.**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))

-   **Domanda:** Un gestore di proprietà può considerare una proprietà come di sola lettura, anche se lo schema indica che la proprietà è scrivibile?

    Sì. Nel sistema di schemi le proprietà vengono annotate come di sola lettura (incluse quelle con `isInnate = "true"` ) o di lettura/scrittura. I gestori di proprietà che non supportano la scrittura di una particolare proprietà che lo schema dichiara che deve essere scrivibile devono implementare [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) e restituire S FALSE nelle chiamate a \_ [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) per tale proprietà. Ciò indica che nel contesto di questo gestore e di questo file la proprietà non è scrivibile.

    > [!Note]  
    > L'azione inversa non è possibile. Non è possibile abilitare un gestore delle proprietà per scrivere una proprietà contrassegnata come di sola lettura nello schema

     

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui gestori di proprietà](./building-property-handlers-properties.md)
</dt> <dt>

[Uso di nomi di tipi](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Uso degli elenchi di proprietà](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inizializzazione di gestori di proprietà](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md)
</dt> </dl>

 

 
