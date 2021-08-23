---
description: Potrebbe essere necessario che un servizio venga arrestato prima e riavviato in seguito a un'operazione di ripristino.
ms.assetid: 111d1281-ad83-49bc-868c-1106a0e25a2a
title: Arresto dei servizi per il ripristino da parte dei richiedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa8051fc20c5ba1bd930da8c7da5c40829c07772572c2b1fb795250d34b8c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511621"
---
# <a name="stopping-services-for-restore-by-requesters"></a>Arresto dei servizi per il ripristino da parte dei richiedenti

Potrebbe essere necessario che un servizio venga arrestato prima e riavviato in seguito a un'operazione di ripristino.

In genere, l'arresto e l'avvio di un servizio per supportare un ripristino vengono eseguiti da un writer durante la gestione dell'evento [*PreRestore*](vssgloss-p.md) (con [**CVssWriter::OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) e dell'evento [*PostRestore*](vssgloss-p.md) (con [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)).

Tuttavia, possono verificarsi casi in cui è necessario che un richiedente arresti in modo esplicito un servizio in esecuzione. I writer indicano se questo è il caso impostando il valore VSS RME STOP RESTORE START o VSS RME RESTORE STOP START dell'enumerazione VSS RESTOREMETHOD ENUM come argomento del metodo di ripristino di una chiamata al metodo \_ \_ \_ \_ \_ \_ \_ \_ [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) [**\_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) e specificando il nome del servizio da arrestare.

Un richiedente ottiene informazioni sul metodo di ripristino e sul nome del servizio da arrestato quando si usano i metadati del writer usando il metodo [**IVssExamineWriterMetadata::GetRestoreMethod.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)

È importante che il writer, quando si specifica il nome di un servizio da arrestato, usi il nome noto pubblicamente corretto del servizio. Un nome ambiguo o impreciso può causare l'arresto del servizio errato da parte dei richiedenti o l'impossibilità di determinare quale servizio arrestare.

Al termine dell'operazione di ripristino, i richiedenti devono riavviare il servizio.

È necessario prestare attenzione nella progettazione e nell'implementazione di writer che supportano i servizi che i richiedenti devono arrestare e riavviare. In particolare, tali writer non devono effettivamente far parte del servizio, ovvero il writer stesso non deve essere arrestato e quindi riavviato nel corso dell'operazione di ripristino.

Un writer il cui processo viene arrestato avrà un'istanza del writer diversa al riavvio. La nuova istanza del writer non riceverà eventi vss destinati all'istanza originale del writer. In particolare, se il processo di un'istanza del writer viene arrestato dopo la gestione di un evento PreRestore, la nuova istanza non riceverà l'evento PostRestore. VsS genererà inoltre un errore che indica la perdita di un writer partecipante nell'operazione di ripristino e [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) può restituire un errore.

 

 



