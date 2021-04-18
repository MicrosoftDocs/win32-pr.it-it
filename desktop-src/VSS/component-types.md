---
description: I componenti indicano il tipo di dati che rappresentano tramite un tipo.
ms.assetid: 19d785d5-09a7-48b9-a0a2-eca3049d67fe
title: Tipi di componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f89355b4b26090b7d43f9753c086b4ccc79df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318904"
---
# <a name="component-types"></a>Tipi di componenti

I componenti indicano il tipo di dati che rappresentano tramite un tipo.

Attualmente, i tipi di componente (vedere il [**\_ \_ tipo di componente VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) sono limitati agli elementi seguenti:

-   Componenti database
-   Filegroup

Per informazioni sull'implementazione sull'impostazione dei tipi di componenti, vedere [definizione di componenti per Writer](definition-of-components-by-writers.md).

I writer hanno una digitazione dei dati che ne indica l'utilizzo (vedere il [**\_ \_ tipo di origine VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), che può essere il seguente:

-   Un database transazionale (ad esempio, SQL Server)
-   Un database non transazionale (ad esempio un client del foglio di calcolo)
-   Filegroup (altro)

La specifica di un tipo di componente come database consente un'identificazione più semplice del contenuto, consente la gestione separata dei file di log e di dati (vedere [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) per i dettagli) e impone un maggiore rigore nella selezione dei file non consentendo la selezione di file ricorsivi o usando un [*percorso alternativo*](vssgloss-a.md) (vedere [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) e [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).

Con un componente del gruppo di file, d'altra parte, a meno che non si conoscano i dati in esso contenuti, si ha maggiore libertà di come vengono inseriti i file, perché è possibile usare la specifica ricorsiva e i percorsi alternativi.

In futuro è possibile aggiungere altri tipi di componenti.

 

 



