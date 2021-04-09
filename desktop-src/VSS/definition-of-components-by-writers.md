---
description: I componenti vengono definiti da e di cui viene creata un'istanza dal writer nel documento di metadati del writer in risposta a un evento di identificazione all'inizio di un'operazione di backup (vedere Panoramica dell'inizializzazione del backup) quando il documento di metadati del writer viene popolato.
ms.assetid: 5e1c3f9b-ca83-4e70-963b-0a237c6f4b0d
title: Definizione dei componenti per Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5383e9bc87620f23bb2a3ab067c1913a323782
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885406"
---
# <a name="definition-of-components-by-writers"></a>Definizione dei componenti per Writer

I componenti vengono definiti da e di cui viene creata un'istanza dal writer nel documento di metadati del writer in risposta a un [*evento di identificazione*](vssgloss-i.md) all'inizio di un'operazione di backup (vedere [Panoramica dell'inizializzazione del backup](overview-of-backup-initialization.md)) quando il documento di metadati del writer viene popolato.

Quando si crea un componente nel documento di metadati del writer, usando [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssCreateWriterMetadata:: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), un writer deve specificare:

-   Indica se il componente è [ *selezionabile per il backup*](vssgloss-s.md)
-   Tipo di componente
-   Nome del componente (che deve essere univoco non solo all'interno di un' [*istanza di writer*](vssgloss-w.md) specificata, ma in tutte le istanze del writer)
-   Indica se al componente sono associati metadati specifici del writer
-   Indica se il writer richiede una notifica dopo un backup completato

I writer possono facoltativamente specificare:

-   [*Percorso logico*](vssgloss-l.md) di un componente (che deve essere univoco non solo all'interno di un'istanza di writer specificata, ma in tutte le istanze del writer)
-   Descrizione o didascalia di un componente
-   Icona da usare con le GUI per indicare il componente

Non è necessario che un componente contenga effettivamente alcun file. Questo tipo di componente vuoto o "fittizio" può essere utile per organizzare i componenti. Tale componente può essere utilizzato per definire un [*set di componenti*](vssgloss-c.md) e un componente del writer (vedere il [percorso logico dei componenti](logical-pathing-of-components.md)).

## <a name="setting-up-component-organization"></a>Configurazione dell'organizzazione di componenti

L'impostazione della [*selezione*](vssgloss-s.md) di un componente (la relativa [*selezione per il backup*](vssgloss-s.md)e la relativa [*selezione per il ripristino*](/windows)) e i relativi [*percorsi logici*](vssgloss-l.md) consentono a un writer di richiedere o rendere facoltativo l'inclusione di determinati componenti in un'operazione di backup o ripristino e di raggruppare i componenti in [*set*](vssgloss-c.md) di componenti con un componente selezionabile che funge da punto di ingresso per l'intero gruppo.

L'appartenenza a questi raggruppamenti determina quali componenti verranno utilizzati durante le operazioni di backup e ripristino. Utilizzando "selezionabile" per indicare selezionabile per indietro per l'operazione di backup e selezionabile per il ripristino per l'operazione di ripristino, gli sviluppatori devono comprendere quanto segue:

-   Se viene eseguito il backup di tutti i componenti gestiti da un determinato writer, un richiedente deve [*includere in modo esplicito*](vssgloss-e.md) tutti i [*componenti*](vssgloss-c.md) non selezionabili senza predecessori selezionabili nel [*percorso logico*](vssgloss-l.md) del documento componenti di backup ed eseguire il backup e il ripristino di tali componenti come gruppo.
-   Un richiedente può aggiungere esplicitamente componenti selezionabili al documento dei componenti di backup durante le operazioni di backup e ripristino. una volta aggiunto, il componente deve essere sottoposto a backup o ripristino.
-   Se un componente è selezionabile, il componente e tutti i relativi [*sottocomponenti*](vssgloss-s.md) (definiti da percorsi logici) formano un set di componenti, che può essere considerato come una singola unità che può eventualmente partecipare alle operazioni di backup e ripristino.
-   Un richiedente non aggiunge mai esplicitamente un componente non selezionabile con i predecessori selezionabili, un sottocomponente di un set di componenti, al documento relativo ai componenti di backup durante le operazioni di backup e ripristino. Questi componenti devono essere [*inclusi in modo implicito*](/windows) se il relativo predecessore selezionabile viene aggiunto in modo esplicito, nel qual caso è necessario eseguirne il backup o il ripristino (vedere [uso dei componenti da parte del richiedente](use-of-components-by-the-requestor.md)).
-   Un componente selezionabile con un predecessore selezionabile è ancora un [*sottocomponente*](vssgloss-s.md) (membro di un set di componenti) e può essere incluso in modo implicito se il relativo predecessore selezionabile è incluso in modo esplicito nell'operazione. In questo caso, le informazioni non vengono aggiunte al documento componenti di backup. Se il predecessore selezionabile non è incluso nell'operazione, il componente può essere selezionato in modo esplicito per l'inclusione nell'operazione, nel qual caso le informazioni sono incluse nel documento componenti di backup.
-   Un sottocomponente incluso in modo implicito in un backup può essere incluso in modo esplicito in un'operazione di ripristino, indipendentemente dallo stato di qualsiasi predecessore selezionabile, se è selezionabile per il ripristino. Eventuali sottocomponenti selezionabili per il ripristino inclusi durante un'operazione di ripristino devono includere le informazioni aggiunte al documento componenti di backup.
-   Un writer privo di componente aggiunto in modo esplicito al documento componenti di backup prima della generazione di [*PrepareForBackup*](vssgloss-p.md) e gli eventi di [*preripristino*](vssgloss-p.md) non riceveranno altri eventi VSS.

Per ulteriori informazioni, vedere [utilizzo della selezione e dei percorsi logici](working-with-selectability-and-logical-paths.md).

## <a name="adding-files-to-a-component"></a>Aggiunta di file a un componente

Un componente contiene informazioni sui file nel formato di un [*set di file*](vssgloss-f.md) contenente:

-   Una directory radice dei file nel componente.
-   Specifica di file per i file nel componente.
-   Flag che indica se la specifica del componente è ricorsiva.

A seconda del tipo di componente, che può essere un database o un gruppo di file e (nel caso di componenti di database) se i file da caricare sono file di dati o di log, un writer chiama [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) per aggiungere un set di file.

Quando si usano queste funzioni, è necessario specificare i file da aggiungere al set di file come indicato di seguito:

-   *wszPath*: percorso della directory che contiene i file da aggiungere al set di file. Se il parametro *bRecursive* è impostato su **true**, il parametro *wszPath* specifica una gerarchia di directory da attraversare in modo ricorsivo e tutte le directory devono essere ricreate, incluse le directory vuote.
-   *wszFilespec*: questa stringa specifica i file in ogni directory da aggiungere al set di file.

Si supponga, ad esempio, che esista la struttura di directory seguente:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ directory1 \\ directory2 \\File1.txt  
C: \\ directory1 \\ directory2 \\File2.txt  
C: \\ directory1 \\ Directory3\\  
</dl>

Se il writer specifica "C: \\ directory1" per *wszPath*, "file1. \* " per *wszFilespec* e **true** per *bRecursive*, il richiedente deve includere questi file:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ directory1 \\ directory2 \\File1.txt  
</dl>

Se invece il writer specifica "C: \\ directory1" per *wszPath*, " \* " per *wszFilespec* e **true** per *bRecursive*, il richiedente deve includere questi file:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ directory1 \\ directory2 \\File1.txt  
C: \\ directory1 \\ directory2 \\File2.txt  
</dl>

Se il writer specifica "C: \\ directory1" per *wszPath*, " \* " per *wszFilespec* e **false** per *bRecursive*, il richiedente deve includere questi file:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
</dl>

In tutti gli esempi precedenti, ogni volta che il writer specifica **true** per *bRecursive*, \\ \\ \\ è necessario ricreare la directory vuota C: directory1 Directory3.

Per un set di file aggiunto a un componente del gruppo di file, nei casi in cui i file attualmente presenti sul disco non sono in quello che il writer considererà il percorso appropriato o predefinito, un writer può scegliere di aggiungere un percorso alternativo. In questi casi, la definizione del set di file del percorso contiene la posizione normale dei file e la posizione in cui devono essere ripristinati i file, mentre il percorso alternativo contiene il percorso corrente dei file di cui eseguire il backup.

Tutti i file del set di file devono esistere al momento del backup. I richiedenti devono presupporre che tutti i file elencati nel set di file siano necessari per il backup e non riusciranno a eseguire il backup se mancano alcuni file. Si noti che quando \* si specifica "" per il parametro *wszFilespec* , può corrispondere a zero o a più file.

Si noti che tali attributi del documento di metadati del writer come mapping di percorsi alternativi, file inclusi ed esclusi in modo esplicito e metodi di ripristino vengono impostati a livello di writer, non a livello di componente. Per ulteriori informazioni, vedere [utilizzo del documento di metadati del writer](working-with-the-writer-metadata-document.md).

## <a name="component-definition-for-backup-and-restore-operations"></a>Definizione del componente per le operazioni di backup e ripristino

Sia le operazioni di ripristino che quelle di backup generano necessariamente un [*evento di identificazione*](vssgloss-i.md)e, per i backup e i ripristini, verranno gestite dallo stesso metodo [**CVssWriter:: onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) .

Durante le operazioni di backup, i richiedenti utilizzano le informazioni restituite dai metodi [**CVssWriter:: Onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) del writer per determinare quali sono i writer presenti nel sistema e quindi determinare quale dei file eseguire il backup.

Durante le operazioni di ripristino, le informazioni restituite dall'evento [**CVssWriter:: Onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) del writer vengono utilizzate solo per stabilire l'identità e lo stato dei writer attualmente presenti nel sistema. le informazioni sulle specifiche del file generate durante un ripristino non vengono utilizzate. Al contrario, per ottenere questi dati vengono utilizzati i documenti di metadati del writer archiviati in fase di backup.

Una volta generati durante un'operazione di backup, le informazioni sul componente writer, insieme al resto delle informazioni del writer, vengono salvate per essere recuperate per supportare le operazioni di ripristino. In genere è responsabilità del richiedente archiviare queste informazioni.

 

 
