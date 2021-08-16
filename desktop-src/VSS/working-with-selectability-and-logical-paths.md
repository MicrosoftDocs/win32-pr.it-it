---
description: La partecipazione di un writer a un'operazione di backup o ripristino e a quale dei relativi dati vengono salvati dipende da quale dei relativi componenti viene incluso in modo esplicito come parte del documento dei componenti di backup del richiedente e dalla relazione tra tali componenti e il percorso logico di altri componenti all'interno del documento dei metadati del writer.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Uso della selezionabilità e dei percorsi logici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f008b086ea50a1695a76f8b7beecab473b767fb1e2835fd5686197bb1b583175
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344254"
---
# <a name="working-with-selectability-and-logical-paths"></a>Uso della selezionabilità e dei percorsi logici

La partecipazione di un writer a un'operazione di backup o ripristino e a [](vssgloss-e.md) quale dei relativi dati vengono salvati dipende da quale dei relativi componenti viene incluso in modo esplicito come parte del documento dei componenti di backup del richiedente e dalla relazione tra tali componenti e il percorso logico di altri componenti all'interno del documento dei metadati del writer.

I writer senza componenti aggiunti al documento del componente di backup del richiedente prima della generazione di un evento [*PrepareForBackup*](vssgloss-p.md) (nel caso di operazioni di backup) o di un evento [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (nel caso di operazioni di ripristino) non ricevono eventi dopo questo punto e non partecipano all'operazione di backup o ripristino.

Tuttavia, la libertà di un richiedente di includere o escludere un determinato componente in un backup o in un ripristino è disciplinata dai seguenti elementi:

-   Qualsiasi gerarchia esistente tra i componenti gestiti da un writer ed espressa da [ *percorsi logici*](vssgloss-l.md)
-   Indica se il componente è designato come [ *selezionabile per il backup*](vssgloss-s.md)
-   Indica se è designato come selezionabile [ *per il ripristino*](vssgloss-s.md)
-   Indica se esiste una dipendenza esplicita tra un determinato componente in un writer specificato e altri componenti in altri writer

Altre informazioni su questi problemi sono disponibili negli argomenti seguenti:

-   [Percorso logico dei componenti](logical-pathing-of-components.md)
-   [Uso della selezionabilità per il backup](working-with-selectability-for-backup.md)
-   [Uso della selezionabilità per il ripristino e i sottocomponenti](working-with-selectability-for-restore-and-subcomponents.md)
-   [Selezionabilità e uso delle proprietà dei componenti](selectability-and-working-with-component-properties.md)
-   [Dipendenze tra componenti gestiti da writer diversi](dependencies-between-components-managed-by-different-writers.md)

 

 



