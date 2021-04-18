---
description: La partecipazione di un writer a un'operazione di backup o ripristino e i relativi dati vengono salvati, a seconda di quali componenti sono inclusi in modo esplicito come parte del documento dei componenti di backup del richiedente e della relazione tra tali componenti e il percorso logico di altri componenti all'interno del documento di metadati del writer.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Uso della selezione e dei percorsi logici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bc29d629df86562bc9b764b1d83bb8bb511d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307123"
---
# <a name="working-with-selectability-and-logical-paths"></a>Uso della selezione e dei percorsi logici

La partecipazione di un writer a un'operazione di backup o ripristino e i relativi dati vengono salvati, a seconda di quali componenti sono inclusi in [*modo esplicito*](vssgloss-e.md) come parte del documento dei componenti di backup del richiedente e della relazione tra tali componenti e il percorso logico di altri componenti all'interno del documento di metadati del writer.

I writer senza componenti aggiunti al documento del componente di backup di un richiedente prima della generazione di un evento [*PrepareForBackup*](vssgloss-p.md) (nel caso di operazioni di backup) o di un evento di [**preripristino**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (in caso di operazioni di ripristino) non ricevono eventi dopo questo punto e non parteciperanno all'operazione di backup o ripristino.

Tuttavia, la libertà di un richiedente di includere o escludere un determinato componente in un backup o un ripristino è regolata dai seguenti elementi:

-   Qualsiasi gerarchia esistente tra i componenti gestiti da un writer ed espressi da [ *percorsi logici*](vssgloss-l.md)
-   Indica se il componente è designato come [ *selezionabile per il backup*](vssgloss-s.md)
-   Indica se è designato come [ *selezionabile per il ripristino*](vssgloss-s.md)
-   Indica se esiste una dipendenza esplicita tra un determinato componente in un determinato writer e altri componenti di altri writer

Per ulteriori informazioni su questi problemi, vedere gli argomenti seguenti:

-   [Percorso logico dei componenti](logical-pathing-of-components.md)
-   [Utilizzo della selezione per il backup](working-with-selectability-for-backup.md)
-   [Utilizzo della selezione per il ripristino e i sottocomponenti](working-with-selectability-for-restore-and-subcomponents.md)
-   [Selezione e utilizzo delle proprietà dei componenti](selectability-and-working-with-component-properties.md)
-   [Dipendenze tra componenti gestiti da Writer diversi](dependencies-between-components-managed-by-different-writers.md)

 

 



