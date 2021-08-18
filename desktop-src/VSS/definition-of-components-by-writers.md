---
description: I componenti vengono definiti da e ne viene creata un'istanza dai writer nel documento di metadati del writer in risposta a un evento Identify all'inizio di un'operazione di backup (vedere Panoramica dell'inizializzazione del backup) quando il documento di metadati del writer viene popolato.
ms.assetid: 5e1c3f9b-ca83-4e70-963b-0a237c6f4b0d
title: Definizione di componenti per writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82fa08acba3c49cd99e83a5dcc901d4a12108a9dc6dde9891add93bcc54e3566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136384"
---
# <a name="definition-of-components-by-writers"></a>Definizione di componenti per writer

I componenti vengono definiti da e ne viene creata un'istanza dai writer nel relativo documento di metadati del writer in risposta a un evento [*Identify*](vssgloss-i.md) all'inizio di un'operazione di backup (vedere [Panoramica](overview-of-backup-initialization.md)dell'inizializzazione del backup) quando il documento di metadati del writer viene popolato.

Quando si crea un componente nel relativo documento di metadati del writer, usando [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssCreateWriterMetadata::AddComponent,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)un writer deve specificare:

-   Se il componente è [ *selezionabile per il backup*](vssgloss-s.md)
-   Tipo di componente
-   Nome del componente (che deve essere univoco non solo all'interno di una determinata istanza del [*writer,*](vssgloss-w.md) ma in tutte le istanze del writer)
-   Indica se al componente sono associati metadati specifici del writer
-   Indica se il writer richiede una notifica dopo un backup riuscito

I writer possono specificare facoltativamente:

-   Percorso logico di un componente [*(che*](vssgloss-l.md) deve essere univoco non solo all'interno di una determinata istanza del writer, ma in tutte le istanze del writer)
-   Descrizione (o didascalia) di un componente
-   Icona da usare con le guis per indicare il componente

Non è necessario che un componente contenga effettivamente alcun file. Questo tipo di componente vuoto o "fittizio" può essere utile per organizzare i componenti. Tale componente può essere usato per definire un [*set di*](vssgloss-c.md) componenti e un componente del writer (vedere Percorso logico [dei componenti).](logical-pathing-of-components.md)

## <a name="setting-up-component-organization"></a>Configurazione dell'organizzazione dei componenti

L'impostazione della selezionabilità di un componente (la sua selezionabilità [](vssgloss-l.md) per il [*backup*](vssgloss-s.md)e la relativa selezionabilità per il [*ripristino)*](/windows)e i relativi [](vssgloss-c.md) percorsi logici consentono a un writer di rendere obbligatorio o facoltativo l'inclusione di determinati componenti in un'operazione di backup o ripristino e di raggruppare i componenti in set di componenti con un componente selezionabile che funge da punto di ingresso all'intero gruppo. [](vssgloss-s.md)

L'appartenenza a questi raggruppamenti determina quali componenti verranno usati durante le operazioni di backup e ripristino. Usando "selectable" per indicare che è possibile selezionare nuovamente per l'operazione di backup e può essere selezionato per il ripristino per l'operazione di ripristino, gli sviluppatori devono comprendere che:

-   Se viene eseguito il backup di tutti i componenti gestiti da un [](vssgloss-c.md) determinato writer, un [](vssgloss-l.md) richiedente deve includere in modo esplicito tutti i componenti non selezionabili senza predecessori selezionabili nel percorso logico del documento dei componenti di backup ed eseguire il backup e il ripristino di tali componenti come gruppo. [](vssgloss-e.md)
-   Un richiedente ha la possibilità di aggiungere in modo esplicito componenti selezionabili al documento dei componenti di backup durante le operazioni di backup e ripristino. Dopo l'aggiunta, è necessario eseguire il backup o il ripristino del componente.
-   Se un componente è selezionabile, il componente e tutti i relativi sottocomponenti [*(come*](vssgloss-s.md) definito dai percorsi logici) formano un set di componenti, che può essere considerato come una singola unità che può facoltativamente partecipare alle operazioni di backup e ripristino.
-   Un richiedente non aggiunge mai in modo esplicito un componente non selezionabile con predecessori selezionabili, un sottocomponente in un set di componenti, al documento dei componenti di backup durante le operazioni di backup e ripristino. Questi componenti devono essere [*inclusi in modo implicito*](/windows) se il predecessore selezionabile viene aggiunto in modo esplicito, nel qual caso è necessario eseguire il backup o il ripristino (vedere Uso dei componenti da parte [del richiedente).](use-of-components-by-the-requestor.md)
-   Un componente selezionabile con un predecessore selezionabile è ancora un [*sottocomponente*](vssgloss-s.md) (un membro di un set di componenti) e può essere incluso in modo implicito se il predecessore selezionabile è incluso in modo esplicito nell'operazione. In questo caso, le relative informazioni non vengono aggiunte al documento backup components. Se il predecessore selezionabile non è incluso nell'operazione, il componente può essere selezionato in modo esplicito per l'inclusione nell'operazione, nel qual caso le relative informazioni vengono incluse nel documento dei componenti di backup.
-   Un sottocomponente incluso in modo implicito in un backup può essere incluso in modo esplicito in un'operazione di ripristino, indipendentemente dello stato di qualsiasi predecessore selezionabile, se selezionabile per il ripristino. Per qualsiasi sottocomponente selezionabile per il ripristino incluso durante un'operazione di ripristino, le informazioni devono essere aggiunte al documento Dei componenti di backup.
-   Un writer che non ha aggiunto in modo esplicito alcun componente al documento dei componenti di backup prima della generazione degli eventi [*PrepareForBackup*](vssgloss-p.md) e [*PreRestore*](vssgloss-p.md) non riceverà altri eventi VSS.

Per altre informazioni, vedere [Uso della selezionabilità e dei percorsi logici.](working-with-selectability-and-logical-paths.md)

## <a name="adding-files-to-a-component"></a>Aggiunta di file a un componente

Un componente contiene informazioni sul file sotto forma di [*un set di file*](vssgloss-f.md) che contiene:

-   Directory radice dei file nel componente.
-   Specifica di file per i file nel componente.
-   Flag che indica se la specifica del componente è ricorsiva.

A seconda del tipo di componente, che può essere un database o un filegroup, e (nel caso dei componenti di database) se i file da caricare sono file di dati o di log, un writer chiama [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) per aggiungere un set di file.

Quando si usano queste funzioni, è necessario specificare i file da aggiungere al set di file come indicato di seguito:

-   *wszPath:* percorso della directory che contiene i file da aggiungere al set di file. Se il *parametro bRecursive* è impostato su **true,** il *parametro wszPath* specifica una gerarchia di directory da attraversare in modo ricorsivo e tutte le directory devono essere ricreate, incluse le directory vuote.
-   *wszFilespec:* questa stringa specifica i file in ogni directory da aggiungere al set di file.

Si supponga, ad esempio, che esista la struttura di directory seguente:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File2.txt  
C: \\ Directory1 \\ Directory3\\  
</dl>

Se il writer specifica "C: \\ Directory1" per *wszPath*, "File1. " per \* *wszFilespec* e **true** per *bRecursive*, il richiedente deve includere questi file:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
</dl>

Se invece il writer specifica "C: \\ Directory1" per *wszPath*, " " per \* *wszFilespec* e **true** per *bRecursive*, il richiedente deve includere questi file:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File2.txt  
</dl>

Se il writer specifica "C: \\ Directory1" per *wszPath*, " " per \* *wszFilespec* e **false** per *bRecursive*, il richiedente deve includere questi file:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
</dl>

In tutti gli esempi precedenti, ogni volta che il writer specifica **true** per *bRecursive*, la directory vuota C: \\ Directory1 \\ Directory3 \\ deve essere ricreata.

Per un set di file aggiunto a un componente del file group, nei casi in cui i file attualmente su disco non si trovano nel percorso appropriato o predefinito, un writer ha la possibilità di aggiungere un percorso alternativo. In questi casi, la definizione del percorso del set di file contiene la posizione normale dei file e la posizione in cui ripristinare i file, mentre il percorso alternativo contiene il percorso corrente dei file di cui eseguire il backup.

Tutti i file nel set di file devono esistere al momento del backup. I richiedenti devono presupporre che tutti i file elencati nel set di file siano necessari per il backup e, se mancano file, il backup avrà esito negativo. Si noti che quando \* si specifica " " per il parametro *wszFilespec,* può corrispondere a zero o più file.

Si noti che tali attributi del documento di metadati del writer come mapping di percorsi alternativi, file inclusi ed esclusi in modo esplicito e metodi di ripristino vengono impostati a livello di writer, non a livello di componente. Per altre informazioni, vedere [Uso del documento di metadati del writer.](working-with-the-writer-metadata-document.md)

## <a name="component-definition-for-backup-and-restore-operations"></a>Definizione dei componenti per le operazioni di backup e ripristino

Sia le operazioni di ripristino che di backup generano necessariamente un evento [*Identify*](vssgloss-i.md)e per i backup e i ripristini verrà gestito dallo stesso metodo [**CVssWriter::OnIdentify.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)

Durante le operazioni di backup, i richiedenti usano le informazioni restituite dai metodi [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) di un writer per determinare quali writer sono presenti nel sistema e quindi per determinare di quali file eseguire il backup.

Durante le operazioni di ripristino, le informazioni restituite dall'evento [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) di un writer vengono usate solo per stabilire l'identità e lo stato dei writer attualmente presenti nel sistema. Le informazioni sulla specifica del file generate durante un ripristino non vengono utilizzate. I documenti dei metadati del writer archiviati in fase di backup vengono invece utilizzati per ottenere questi dati.

Dopo la generazione durante un'operazione di backup, le informazioni sul componente writer, insieme alle altre informazioni sul writer, vengono salvate per essere recuperate per supportare le operazioni di ripristino. È in genere responsabilità del richiedente archiviare queste informazioni.

 

 
