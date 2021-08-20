---
description: Esistono diversi motivi per cui un richiedente non dovrebbe o potrebbe non essere in grado di ripristinare i file dai supporti di backup nel percorso originale.
ms.assetid: 2a9cfd99-5a2c-4c0c-98ff-11c745298cda
title: Uso di percorsi alternativi durante il ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907732c7b4b97668f1a317f9e03c3ea35bdec9618ff0e3e3c1a2f1e319eb19fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056149"
---
# <a name="working-with-alternate-locations-during-restore"></a>Uso di percorsi alternativi durante il ripristino

Esistono diversi motivi per cui un richiedente non dovrebbe o potrebbe non essere in grado di ripristinare i file dai supporti di backup nel percorso originale. Ad esempio, un metodo o una destinazione di ripristino può richiedere un ripristino di questo tipo oppure il percorso di ripristino corrente può essere occupato e non scrivibile.

Per gestire questi casi, un writer può aver definito un [*mapping*](vssgloss-a.md)di percorso alternativo, una destinazione di ripristino non standard da usare in circostanze speciali.

Il termine mapping del percorso alternativo, usato con VSS, non deve essere confuso con il termine [*percorso alternativo.*](vssgloss-a.md) I mapping dei percorsi alternativi vengono usati solo durante le operazioni di ripristino e fanno riferimento a una destinazione alternativa per le operazioni di ripristino. I percorsi alternativi vengono usati solo durante le operazioni di backup e fanno riferimento a un'origine alternativa da cui eseguire il backup.

Per usare mapping di percorsi alternativi durante il ripristino, un richiedente può eseguire le operazioni seguenti (in genere in seguito alla generazione di un [**evento PreRestore):**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)

1.  Usando un'istanza dell'interfaccia [**IVssExamineWriterMetadata ottenuta**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) recuperando un writer archiviato, un richiedente usa il metodo [**IVssExamineWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) per ottenere i mapping di percorsi alternativi di un writer come istanze dell'interfaccia [**IVssWMFiledesc.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)

    > [!Note]  
    > Il richiedente usa [**IVssExamineWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping), non [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping). Il primo restituisce i mapping di percorso alternativi disponibili per l'uso da parte di un richiedente. Quest'ultimo viene usato per indicare i mapping dei percorsi alternativi effettivamente usati da un richiedente.

     

2.  La chiamata a [**IVssExamineWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) restituisce un'istanza [**dell'interfaccia IVssWMFiledesc.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) Questa istanza contiene informazioni sul set di file, ovvero un percorso specificato da [**IVssWMFiledesc::GetPath,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)una specifica di file restituita tramite [**IVssWMFiledesc::GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)e un flag di ricorsione ottenuto da [**IVssWMFiledesc::GetRecursive:**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)corrisponde a uno dei set di file aggiunti (usando [**IVssCreateWriterMetadata::AddDatabaseFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) a uno dei componenti gestiti dal writer.

    Il valore restituito da [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) è il mapping del percorso alternativo per questo set di file.

3.  I mapping dei percorsi alternativi non contengono informazioni sui componenti, quindi sarà necessario confrontare le informazioni sul set di file (percorso, specifica del file e flag di ricorsione) ottenute chiamando [**IVssExamineWriterMetadata::GetAlternateLocationMapping con**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) quella contenuta nei componenti del writer.

    Queste informazioni sono disponibili tramite l'iterazione dei componenti del writer e la chiamata a [**IVssExamineWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) per ottenere un'istanza dell'interfaccia [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) e usare [**IVssWMComponent::GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) per ottenere un'istanza [**di IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) contenente le informazioni sul set di file del componente.

    Quando le informazioni sul set di file restituite dall'istanza di [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) ottenute da [**IVssExamineWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) e [**IVssWMComponent::GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) corrispondono a quella ottenuta dall'istanza **di IVssWMFiledesc** derivata da [**IVssWMFiledesc::GetAlternateLocation,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)è stato trovato il componente che gestisce i file con il mapping di percorso alternativo specifico.

4.  Dopo aver individuato il componente, il richiedente può determinare le condizioni in cui deve essere usato un mapping di percorso alternativo eseguendo le operazioni seguenti:

    -   Esame del metodo di ripristino del componente, ottenuto chiamando [**IVssExamineWriterMetadata::GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).
    -   Verifica se una destinazione di ripristino esegue l'override del metodo di ripristino chiamando [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget).

        Se il componente trovato nel documento di metadati del writer è stato [*incluso*](vssgloss-e.md) in modo esplicito nel backup, l'istanza dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrisponderà a tale componente. Se il componente è stato [*incluso in*](vssgloss-i.md) modo implicito nel backup, l'istanza di **IVssComponent** corrisponderà al componente che definisce il set di componenti di cui il componente nel documento di metadati del writer è un sottocomponente.

5.  Con queste informazioni, il richiedente può determinare in base al componente se deve ripristinare un determinato set di file di un determinato componente in una destinazione definita dal mapping del percorso alternativo.

6.  Quando si usa un mapping di percorso alternativo, il richiedente rispetta il descrittore di file e il flag ricorsivo del set di file e usa il percorso fornito dal mapping del percorso alternativo.

    Il richiedente indica di aver usato un mapping di percorso alternativo durante un'operazione di ripristino chiamando [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) con le informazioni sul percorso predefinito del set di file, la destinazione di ripristino alternativa usata e un nome di componente.

    Se il set di file è stato gestito da un componente incluso in modo esplicito nel backup, verrà usato il nome del componente. Se il set di file è stato gestito da un componente incluso in modo implicito nel backup, il nome usato sarà quello del componente che definisce il set di componenti di cui il componente che gestisce il set di file è un sottocomponente.

I writer verificano se i set di file di uno dei relativi componenti sono stati ripristinati in un mapping di percorso alternativo chiamando [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).

 

 



