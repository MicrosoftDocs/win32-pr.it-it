---
description: Il ripristino di file in un sistema in esecuzione può risultare problematico. È importante che l'esecuzione di applicazioni (writer) indichi cosa fare quando si verificano problemi durante i ripristini, ad esempio se il file da ripristinare è attualmente in uso.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: Configurazioni del ripristino VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13acfc59f250a859e9c62f2df2e1b1b982608ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129294"
---
# <a name="vss-restore-configurations"></a>Configurazioni del ripristino VSS

Il ripristino di file in un sistema in esecuzione può risultare problematico. È importante che l'esecuzione di applicazioni (writer) indichi cosa fare quando si verificano problemi durante i ripristini, ad esempio se il file da ripristinare è attualmente in uso.

In VSS, i writer hanno due modalità complementari per la gestione dei ripristini, ovvero [*metodi di ripristino*](vssgloss-r.md) e [*destinazioni di ripristino*](vssgloss-r.md).

Inoltre, i richiedenti possono scegliere di ripristinare i file in posizioni non specificate in precedenza e inviare notifiche ai writer (vedere [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).

Il metodo Restore (chiama anche la destinazione di ripristino originale) viene specificato da un writer al momento del backup e imposta una definizione a livello di writer del metodo da utilizzare per ripristinare tutti i relativi componenti in futuro. Tutti i file e i componenti gestiti da un writer condividono lo stesso metodo di ripristino.

Le destinazioni di ripristino consentono ai writer di modificare il modo in cui devono essere ripristinati i componenti specifici in fase di ripristino. A differenza dei metodi di ripristino, le destinazioni di ripristino sono definite per un set di componenti.

Una descrizione dettagliata dell'utilizzo dei metodi di ripristino e delle destinazioni di ripristino è disponibile negli argomenti elencati di seguito:

-   [Stato ripristino VSS](vss-restore-state.md)
-   [Impostazione di metodi di ripristino VSS](setting-vss-restore-methods.md)
-   [Impostazione delle destinazioni di ripristino VSS](setting-vss-restore-targets.md)
-   [Impostazione delle opzioni di ripristino VSS](setting-vss-restore-options.md)

Per informazioni sui ripristini che non utilizzano questi meccanismi, vedere [ripristini senza partecipazione del writer](restores-without-writer-participation.md).

 

 



