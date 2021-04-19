---
description: Potrebbe essere necessario arrestare un servizio prima e riavviare dopo un'operazione di ripristino.
ms.assetid: 111d1281-ad83-49bc-868c-1106a0e25a2a
title: Arresto dei servizi per il ripristino da richiedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548af25a4b4550d35a8e6fa4d4c0e791897b6e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311591"
---
# <a name="stopping-services-for-restore-by-requesters"></a>Arresto dei servizi per il ripristino da richiedenti

Potrebbe essere necessario arrestare un servizio prima e riavviare dopo un'operazione di ripristino.

In genere, l'arresto e l'avvio di un servizio per il supporto di un ripristino vengono eseguiti da un writer durante la gestione dell'evento di [*preripristino*](vssgloss-p.md) (con [**CVssWriter:: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) e l'evento [*PostRestore*](vssgloss-p.md) (con [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)).

Tuttavia, in alcuni casi è necessario che un richiedente arresti in modo esplicito un servizio in esecuzione. I writer indicano se questo è il caso, impostando il valore di avvio dell'arresto del \_ ripristino VSS RME o del servizio Copia Shadow del volume \_ \_ \_ \_ RME \_ \_ \_ per l'arresto del ripristino dell'enumerazione [**VSS \_ \_ RESTOREMETHOD**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) come argomento del metodo Restore di una chiamata al metodo [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) e specificando il nome del servizio da arrestare.

Un richiedente ottiene informazioni sul metodo Restore e il nome del servizio da arrestare quando si utilizzano i metadati del writer tramite il metodo [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod) .

È importante che il writer, quando si specifica il nome di un servizio da arrestare, usi il nome noto pubblicamente corretto del servizio. Un nome ambiguo o non accurato può comportare l'arresto del servizio errato da parte dei richiedenti o l'impossibilità di determinare quale servizio arrestare.

Al termine dell'operazione di ripristino, i richiedenti devono riavviare il servizio.

È necessario prestare attenzione nella progettazione e nell'implementazione di writer che supportano servizi che i richiedenti devono arrestare e riavviare. In particolare, tali writer non devono far parte del servizio, ovvero il writer stesso non deve essere interrotto e quindi riavviato nel corso dell'operazione di ripristino.

Un writer il cui processo viene arrestato avrà un'istanza di writer diversa al riavvio. La nuova istanza del writer non riceverà gli eventi VSS destinati all'istanza originale del writer. In particolare, se il processo di un'istanza di writer viene arrestato dopo la gestione di un evento di preripristino, la nuova istanza non riceverà l'evento di post-ripristino. VSS genera inoltre un errore che indica la perdita di un writer partecipante nell'operazione di ripristino e [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) può restituire un errore.

 

 



