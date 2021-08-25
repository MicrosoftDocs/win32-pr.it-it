---
description: 'Il documento dei metadati del writer contiene tre set di dati: informazioni di identificazione e classificazione del writer, specifiche a livello di writer e dati dei componenti.'
ms.assetid: 1a84790a-8f46-4e1b-8e45-5036830e8fee
title: Contenuto del documento dei metadati del writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbdb8cf4c2313d17cfd9059626f97356f27ba9168f9e19e4a796fae8797728d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905051"
---
# <a name="writer-metadata-document-contents"></a>Contenuto del documento dei metadati del writer

Il documento dei metadati del writer contiene tre set di dati: informazioni di identificazione e classificazione del writer, specifiche a livello di writer e dati dei componenti.

## <a name="writer-identification-information"></a>Informazioni di identificazione del writer

Le informazioni di identificazione e classificazione del writer includono quanto segue:

-   Nome del writer
-   [*ID classe writer*](vssgloss-w.md)
-   [*Istanza del writer*](vssgloss-w.md)
-   Come vengono usati i dati gestiti dal writer nel sistema host (vedere [**VSS \_ USAGE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Tipo di dati gestiti dal writer (vedere [**VSS \_ SOURCE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Ad eccezione dell'istanza del writer, univoca e generata dal sistema quando viene inizializzato un oggetto [**CVssWriter,**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) tutti questi valori vengono impostati da un writer quando chiama [**CVssWriter::Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) e sono disponibili per un richiedente chiamando [**IVssExamineWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity).

Poiché l'istanza del writer viene generata in modo univoco, un'istanza del writer archiviata recuperata da un documento di metadati del writer archiviato non è probabilmente utile.

Controllando [**VSS \_ USAGE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type), un'applicazione può determinare se un writer gestisce i dati generali dell'applicazione o se i file con cui funziona fanno parte dello stato di avvio del sistema o vengono usati da un servizio di sistema. Le applicazioni di backup e ripristino devono rispettare i tipi di utilizzo per mantenere la stabilità del sistema.

Il flag [**VSS \_ SOURCE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type) indica il tipo di applicazione eseguita dal writer che gestisce i dati di cui eseguire il backup durante il normale funzionamento.

Attualmente, la distinzione è limitata a specificare se il writer produce file come parte di operazioni di database transazionali o non transazionali o se i file sono il risultato di un tipo di attività più generale. Questo elenco può aumentare nel tempo. Queste informazioni possono essere utili per determinare il livello normale di attività previsto nei file di un writer.

## <a name="writer-level-specification"></a>Writer-Level specifica

Le specifiche a livello di writer contengono informazioni a livello di writer nel relativo ambito, che si applicano a tutti i dati indipendentemente dal componente che lo gestisce.

Un writer deve sempre specificare i [*metodi di ripristino*](vssgloss-r.md).

Facoltativamente, è possibile specificare quanto segue:

-   Escludi elenco di file
-   [*Mapping di percorsi alternativi per*](vssgloss-a.md) il ripristino

Gli elenchi di file di inclusione ed esclusione contengono informazioni sui file oltre a queste nei componenti e la relativa specifica sostituisce la specifica del componente.

## <a name="restore-method-specification"></a>Specifica del metodo di ripristino

Il metodo [*di*](vssgloss-r.md) ripristino viene impostato nel documento di metadati del writer [**da IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) e recuperato da un richiedente con [**IVssExamineWriterMetadata::GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

Nell'impostazione di un metodo di ripristino, un writer indica il modo preferito di ripristino dei file, noto anche come destinazione di ripristino originale, per tutti i file gestiti da un writer. Ad esempio, il metodo restore specifica se tutti i file gestiti da un writer devono essere autorizzati a sovrascrivere i file attualmente su disco. Per altre [informazioni, vedere Configurazioni di](vss-restore-configurations.md) ripristino vss e ENUMERAZIONE [**\_ RESTOREMETHOD \_ di VSS.**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)

## <a name="exclude-file-list-specification"></a>Specifica dell'elenco di file di esclusione

L'elenco di esclusione consente di ottimizzare le specifiche dei caratteri jolly nei componenti impedendo in modo esplicito l'inclusione di determinati file in un set di backup.

Ad esempio, un componente potrebbe avere un [*set di file*](vssgloss-f.md) contenente una specifica di file c: Database \\ \\ \* \* . Anche se si tratta di una definizione pratica, talvolta possono essere generati file temporanei (ad esempio nel formato tmp) e il writer vuole sempre impedire \* il backup.

In questo caso, un writer aggiungerebbe .tmp al relativo elenco di esclusione \* [**usando IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles). Questa specifica potrebbe essere ricorsiva.

Un richiedente esegue una query su queste informazioni [**usando IVssExamineWriterMetadata::GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile).

L'elenco di file di esclusione ha la precedenza rispetto a quello dei file dei componenti.

Di conseguenza, l'elenco dei file specificati per il backup in [](vssgloss-e.md) un documento di metadati del writer sarebbe costituito da tutti i file specificati nei componenti inclusi in modo esplicito e dai componenti inclusi in modo [*implicito,*](vssgloss-i.md) meno tutti i file esclusi.

## <a name="alternate-location-mappings-specification"></a>Specifica dei mapping di percorsi alternativi

I mapping dei percorsi alternativi vengono impostati inizialmente durante la creazione di un documento di metadati del writer e indicano un percorso su disco in cui è possibile ripristinare i file se non è possibile ripristinare un file nel percorso originale.

Le informazioni vengono aggiunte come stringa di caratteri wide con terminazione Null con [**IVssCreateWriterMetadata::AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) e recuperate come oggetto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) [**da IVssExamineWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping).

Nonostante i mapping dei percorsi alternativi siano specificati ed esaminati usando le interfacce a livello di writer ([**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)), vengono specificati in termini di [*set di file*](vssgloss-f.md). Il set di file usato per specificare un mapping di percorso alternativo (percorso, specifica del file e flag di ricorsione) deve corrispondere a uno dei set di file già aggiunti a uno dei componenti del writer (vedere Aggiunta di file ai componenti [).](definition-of-components-by-writers.md)

Per altre informazioni, vedere Percorsi di backup e [ripristino non predefiniti.](non-default-backup-and-restore-locations.md)

## <a name="component-level-information"></a>Component-Level informazioni

[*I*](vssgloss-c.md) componenti sono raccolte di file che formano un'unità logica ai fini del backup e del ripristino. È necessario eseguire il backup e il ripristino di tutti i file in un componente, ad eccezione di quelli esclusi in modo esplicito, come unità.

I writer aggiungono componenti [**usando IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), specificando le informazioni sui componenti seguenti:

-   Type
-   Nome
-   Percorso logico (se presente)
-   Funzionalità supportata
-   [*Selezionabilità*](vssgloss-s.md)
-   Metadati che devono essere usati dal writer durante il ripristino
-   Visualizzare le informazioni
-   Informazioni sulle notifiche

[*La selezionabilità*](vssgloss-s.md) [](vssgloss-s.md) per il backup e la selezionabilità per il ripristino sono completamente indipendenti l'una dall'altra e un writer le usa insieme ai percorsi logici per indicare le relazioni tra i vari componenti gestiti. I writer possono indicare quali componenti sono necessari per l'incluso in modo esplicito [*(quelli*](vssgloss-e.md) che possono essere inclusi in modo esplicito a discrezione di un richiedente) e quelli che possono essere inclusi [*solo in modo implicito.*](vssgloss-i.md) Vedere [Uso della selezionabilità e dei percorsi logici.](working-with-selectability-and-logical-paths.md)

I file vengono aggiunti a un determinato componente usando [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles). Vedere [Aggiunta di file ai componenti](definition-of-components-by-writers.md).

Quando si aggiungono file a un componente durante il backup, un writer deve specificare un set di file (un percorso, una specifica del file e un flag di ricorsione) che definisce i file di cui eseguire il backup.

I writer possono anche specificare un [*percorso alternativo per*](vssgloss-a.md) il backup, che non deve essere confuso con i mapping dei percorsi [*alternativi*](vssgloss-a.md) indicati in precedenza. Questo percorso alternativo indica un percorso non predefinito da cui copiare i file quando viene eseguito il backup di un volume.

Le informazioni su un determinato componente nel documento di metadati del writer possono essere ottenute tramite [**un'interfaccia IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) restituita da [**IVssExamineWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent).

I file e i percorsi vengono restituiti in [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) [**come oggetti IVssWMFiledesc.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)

Le informazioni sui componenti di un writer sono descritte in dettaglio in [Definizione dei componenti da parte di writer](definition-of-components-by-writers.md).

 

 



