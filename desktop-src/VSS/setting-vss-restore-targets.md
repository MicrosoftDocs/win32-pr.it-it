---
description: L'interfaccia IVssComponent consente a un writer di ottimizzare esattamente il modo in cui i file vengono ripristinati in base al componente.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Impostazione delle destinazioni di ripristino VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8815e552db518c447bd63b9f02ba9228850384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310666"
---
# <a name="setting-vss-restore-targets"></a>Impostazione delle destinazioni di ripristino VSS

L'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) consente a un writer di ottimizzare esattamente il modo in cui i file vengono ripristinati in base al componente.

Poiché è possibile che la configurazione di sistema durante l'operazione di ripristino sia diversa da quella prevista durante il backup, viene fornito il meccanismo di destinazione del ripristino.

Consente ai writer di chiamare [**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) per modificare il modo in cui vengono ripristinati i componenti [*inclusi in modo esplicito*](vssgloss-e.md) nel documento dei componenti di backup. Questa operazione modifica anche il meccanismo di ripristino utilizzato in questi componenti [*inclusi in modo implicito*](vssgloss-i.md).

Ripristino del file che si verifica durante un riavvio del sistema (nei valori di enumerazione VSS [**\_ RESTOREMETHOD \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) VSS \_ RME \_ Restore \_ al \_ riavvio e VSS \_ RME \_ Restore \_ al \_ riavvio \_ se \_ non è possibile \_ sostituire) non può essere influenzato dalle destinazioni di ripristino perché non sono in esecuzione servizi VSS quando **MoveFileEx** copia i file nel percorso finale.

Analogamente, \_ i \_ ripristini personalizzati di VSS RME possono o meno essere interessati, perché ogni ripristino personalizzato è specifico di un determinato writer e può scegliere di rispettare o ignorare le destinazioni di ripristino.

I richiedenti e i writer possono utilizzare [**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) per verificare la destinazione di ripristino di un set di componenti.

[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) supporta le seguenti destinazioni di ripristino, che possono essere impostate su un componente impostato in base al set di componenti:

-   \_originale VSS RT \_ . Verrà rispettato il metodo di ripristino specificato dall'enumerazione [**\_ RESTOREMETHOD \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) dell'enumerazione VSS.
-   \_alternativa VSS RT \_ . I file vengono ripristinati in un percorso determinato da un mapping del percorso alternativo esistente. Se esiste un mapping del percorso alternativo corrispondente a un percorso in un sottocomponente del set di componenti, eseguire il ripristino nel percorso alternativo, se possibile; in caso contrario, viene restituito un errore.

 

 



