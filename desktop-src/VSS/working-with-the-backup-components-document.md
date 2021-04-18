---
description: Un richiedente crea un documento di componenti di backup all'inizio dell'esecuzione di un backup.
ms.assetid: 5e40e45d-6afa-401a-a6b4-7bec460cb9ec
title: Utilizzo del documento componenti di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d5d3c97696b85d589501f6d3af0b6c7d0e6d47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307121"
---
# <a name="working-with-the-backup-components-document"></a>Utilizzo del documento componenti di backup

Un richiedente crea un documento di componenti di backup all'inizio dell'esecuzione di un backup. Il documento contiene inizialmente solo una descrizione dello stato dell'operazione di backup. Durante il ripristino, nel documento devono essere fornite istruzioni sul modo in cui un richiedente deve procedere alla copia dei file sul disco. Nel corso dell'operazione di ripristino, il documento componenti di backup viene modificato e contiene lo stato dell'operazione.

Diversamente dal documento di metadati del writer, che è di sola lettura, è presente una finestra in cui il documento dei componenti di backup può essere modificato da richiedenti e writer. Il documento può essere aggiornato fino alla generazione di un evento [*BackupComplete*](vssgloss-b.md) o [*BackupShutdown*](vssgloss-b.md) durante le operazioni di backup e fino a quando non viene eseguito il ripristino di un evento [*PostRestore*](vssgloss-p.md) .

Per utilizzare il documento dei componenti di backup di un richiedente è necessario conoscere gli argomenti seguenti:

-   [Ciclo di vita del documento dei componenti di backup](backup-components-document-life-cycle.md)
-   [Contenuto del documento dei componenti di backup](backup-components-document-contents.md)

 

 



