---
description: Il ripristino dei file in un sistema in esecuzione può essere problematico. È importante che le applicazioni in esecuzione (writer) indichi cosa fare quando si verificano difficoltà durante i ripristini, ad esempio se il file da ripristinare è attualmente in uso.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: Configurazioni di ripristino vss
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48b3486128c6a91f601a89d697a4db9d8ab27fe9d3ac4cbef28dc870928d37d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344201"
---
# <a name="vss-restore-configurations"></a>Configurazioni di ripristino vss

Il ripristino dei file in un sistema in esecuzione può essere problematico. È importante che le applicazioni in esecuzione (writer) indichi cosa fare quando si verificano difficoltà durante i ripristini, ad esempio se il file da ripristinare è attualmente in uso.

In VSS, i writer hanno due modi complementari per gestire i ripristini: i [*metodi di ripristino*](vssgloss-r.md) e le destinazioni di [*ripristino*](vssgloss-r.md).

Inoltre, i richiedenti possono scegliere di ripristinare i file in posizioni non specifiche in precedenza e inviare notifiche agli autori (vedere [**IVssBackupComponents::AddNewTarget).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)

Il metodo restore (chiamato anche destinazione di ripristino originale) viene specificato da un writer in fase di backup e imposta una definizione a livello di writer del metodo da usare per ripristinare tutti i relativi componenti in futuro. Tutti i file e i componenti gestiti da un writer condividono lo stesso metodo di ripristino.

Le destinazioni di ripristino consentono ai writer di modificare la modalità di ripristino di componenti specifici in fase di ripristino. A differenza dei metodi di ripristino, le destinazioni di ripristino sono definite per un set di componenti.

Una descrizione dettagliata dell'utilizzo dei metodi di ripristino e delle destinazioni di ripristino è disponibile negli argomenti elencati di seguito:

-   [Stato di ripristino vss](vss-restore-state.md)
-   [Impostazione dei metodi di ripristino vss](setting-vss-restore-methods.md)
-   [Impostazione delle destinazioni di ripristino vss](setting-vss-restore-targets.md)
-   [Impostazione delle opzioni di ripristino vss](setting-vss-restore-options.md)

Per informazioni sui ripristini che non usano questi meccanismi, vedere Ripristini [senza partecipazione al writer.](restores-without-writer-participation.md)

 

 



