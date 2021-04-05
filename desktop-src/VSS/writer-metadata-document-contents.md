---
description: 'Il documento dei metadati del writer contiene tre set di dati: informazioni di identificazione e classificazione del writer, specifiche a livello di writer e dati del componente.'
ms.assetid: 1a84790a-8f46-4e1b-8e45-5036830e8fee
title: Contenuto del documento dei metadati del writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f222977f1c8d785e6f69613f219545dc3402af7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049496"
---
# <a name="writer-metadata-document-contents"></a>Contenuto del documento dei metadati del writer

Il documento dei metadati del writer contiene tre set di dati: informazioni di identificazione e classificazione del writer, specifiche a livello di writer e dati del componente.

## <a name="writer-identification-information"></a>Informazioni di identificazione del writer

Le informazioni di identificazione e classificazione del writer includono quanto segue:

-   Nome writer
-   [*ID classe Writer*](vssgloss-w.md)
-   [*Istanza writer*](vssgloss-w.md)
-   Modalità di utilizzo dei dati gestiti dal writer nel sistema host (vedere [**\_ \_ tipo di utilizzo VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Tipo di dati gestiti dal writer (vedere il [**tipo di \_ origine \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Fatta eccezione per l'istanza del writer, che è univoca e viene generata dal sistema quando viene inizializzato un oggetto [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) , tutti questi valori vengono impostati da un writer quando chiama [**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) e sono disponibili per un richiedente chiamando [**IVssExamineWriterMetadata:: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity).

Poiché l'istanza del writer viene generata in modo univoco, un'istanza di writer archiviata recuperata da un documento di metadati del writer archiviato non può essere utile.

Controllando [**il \_ \_ tipo di utilizzo VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type), un'applicazione può determinare se un writer gestisce i dati generali dell'applicazione o se i file che utilizza fanno parte dello stato di avvio del sistema o vengono utilizzati da un servizio di sistema. Le applicazioni di backup e ripristino devono rispettare i tipi di utilizzo per garantire la stabilità del sistema.

Il flag del [**\_ \_ tipo di origine VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type) indica il tipo di applicazione che il writer gestisce i dati di cui eseguire il backup durante il normale funzionamento.

Attualmente, la distinzione è limitata a specificare se il writer produce file come parte delle operazioni di database transazionali o non transazionali o se i file sono il risultato di un tipo di attività più generale. Questo elenco può aumentare nel tempo. Queste informazioni possono essere utili per determinare il livello di attività normale previsto nei file di un writer.

## <a name="writer-level-specification"></a>Specifica Writer-Level

Le specifiche a livello di writer contengono informazioni che sono a livello di writer nell'ambito, applicando a tutti i dati indipendentemente da quali un componente lo gestisce.

Un writer deve sempre specificare i [*metodi di ripristino*](vssgloss-r.md).

Facoltativamente, è possibile specificare quanto segue:

-   Escludi elenco file
-   [*Mapping dei percorsi alternativi*](vssgloss-a.md) per il ripristino

Gli elenchi di file include ed exclude contengono informazioni sui file oltre a quelle nei componenti e la relativa specifica sostituisce il componente.

## <a name="restore-method-specification"></a>Specifica del metodo Restore

Il [*Metodo Restore*](vssgloss-r.md) viene impostato nel documento di metadati del writer da [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) e recuperato da un richiedente con [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

Quando si imposta un metodo Restore, un writer indica il modo preferito per il ripristino dei file, noto anche come destinazione di ripristino originale, per tutti i file gestiti da un writer. Ad esempio, il metodo Restore specifica se tutti i file gestiti da un writer devono essere autorizzati a sovrascrivere i file attualmente presenti sul disco. Per ulteriori informazioni, vedere [configurazioni di ripristino VSS](vss-restore-configurations.md) e [**\_ \_ enumerazione RESTOREMETHOD VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) .

## <a name="exclude-file-list-specification"></a>Specifica elenco file esclusi

L'elenco di esclusioni consente di ottimizzare le specifiche dei caratteri jolly nei componenti impedendo in modo esplicito l'inclusione di determinati file in un set di backup.

È ad esempio possibile che un componente disponga di un [*set di file*](vssgloss-f.md) contenente una specifica del file c: \\ database \\ \* . \* Sebbene si tratta di una definizione pratica, è possibile che vengano generati occasionalmente file temporanei (ad esempio, form \* . tmp) e che il writer desideri sempre impedire il backup.

In questo caso, un writer aggiungerà \* . tmp al relativo elenco di esclusioni usando [**IVssCreateWriterMetadata:: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles). Questa specifica può essere ricorsiva.

Un richiedente esegue una query di queste informazioni usando [**IVssExamineWriterMetadata:: GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile).

L'elenco di file di esclusione ha la precedenza sugli elenchi di file dei componenti.

Pertanto, l'elenco dei file specificati per il backup in un documento di metadati del writer è costituito da tutti i file specificati nei componenti [*inclusi in modo esplicito*](vssgloss-e.md) e dai componenti inclusi in modo [*implicito*](vssgloss-i.md) , meno tutti i file esclusi.

## <a name="alternate-location-mappings-specification"></a>Specifica mapping percorsi alternativi

I mapping dei percorsi alternativi vengono inizialmente impostati durante la creazione di un documento di metadati del writer e indicano un percorso su disco in cui è possibile ripristinare i file se non è possibile ripristinare un file nel percorso originale.

Le informazioni vengono aggiunte come stringa di caratteri wide con terminazione null con [**IVssCreateWriterMetadata:: AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) e recuperate come oggetto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) da [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping).

Nonostante il fatto che i mapping dei percorsi alternativi siano specificati ed esaminati utilizzando le interfacce a livello di Writer ([**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)), vengono specificati in termini di [*set di file*](vssgloss-f.md). Il set di file usato per specificare un mapping del percorso alternativo (percorso, specifica di file e flag di ricorsione) deve corrispondere a uno dei set di file già aggiunti a uno dei componenti del writer (vedere [aggiunta di file ai componenti](definition-of-components-by-writers.md)).

Per ulteriori informazioni, vedere [percorsi di backup e ripristino non predefiniti](non-default-backup-and-restore-locations.md).

## <a name="component-level-information"></a>Informazioni Component-Level

I [*componenti*](vssgloss-c.md) sono raccolte di file che formano un'unità logica a scopo di backup e ripristino. Tutti i file in un componente, eccetto quelli esclusi in modo esplicito, devono essere sottoposti a backup e ripristinati come unità.

I writer aggiungono componenti usando [**IVssCreateWriterMetadata:: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), specificando le informazioni seguenti sul componente:

-   Type
-   Nome
-   Percorso logico (se presente)
-   Funzionalità supportata
-   [*Selezionabilità*](vssgloss-s.md)
-   Metadati che devono essere utilizzati dal writer durante il ripristino
-   Visualizza informazioni
-   Informazioni di notifica

La [*selezione per il backup*](vssgloss-s.md) e la [*selezione per il ripristino*](vssgloss-s.md) sono completamente indipendenti tra loro e un writer li utilizza insieme ai percorsi logici per indicare le relazioni tra i vari componenti gestiti. I writer possono indicare i componenti necessari per l' [*inclusione esplicita*](vssgloss-e.md) (quelli che possono essere inclusi in modo esplicito a discrezione di un richiedente) e quelli che possono essere inclusi solo in [*modo implicito*](vssgloss-i.md). (Vedere [uso di selezione e percorsi logici](working-with-selectability-and-logical-paths.md)).

I file vengono aggiunti a un determinato componente usando [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles). (Vedere [aggiunta di file ai componenti](definition-of-components-by-writers.md)).

Quando si aggiungono file a un componente durante il backup, è necessario che un writer specifichi un set di file, ovvero un percorso, una specifica del file e un flag di ricorsione, che definisce i file di cui eseguire il backup.

I writer possono inoltre specificare un [*percorso alternativo*](vssgloss-a.md) per il backup, che non deve essere confuso con i [*mapping dei percorsi alternativi*](vssgloss-a.md) citati in precedenza. Questo percorso alternativo indica una posizione non predefinita dalla quale i file devono essere copiati quando viene eseguito il backup di un volume.

Le informazioni su un determinato componente nel documento di metadati del writer possono essere ottenute tramite un'interfaccia [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) restituita da [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent).

I file e i percorsi vengono restituiti in [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) come oggetti [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) .

Le informazioni sul componente di un writer sono descritte in dettaglio nella [definizione dei componenti da parte dei writer](definition-of-components-by-writers.md).

 

 



