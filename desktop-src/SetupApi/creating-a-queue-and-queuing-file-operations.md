---
description: L'accodamento delle operazioni dei file è utile perché consente di elaborare l'intera installazione, anziché tramite la sezione INF.
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: Creazione di una coda e operazioni di Accodamento di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313706"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a>Creazione di una coda e operazioni di Accodamento di file

L'accodamento delle operazioni dei file è utile perché consente di elaborare l'intera installazione, anziché tramite la sezione INF.

Per creare una coda di file, dichiarare una variabile per archiviare l'handle della coda, quindi chiamare la funzione [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) . Dopo la creazione della coda, è possibile accodare le operazioni di copia, ridenominazione ed eliminazione, nonché analizzare la coda dei file per verificare le operazioni accodate.

Per aggiungere singole operazioni su file alla coda, usare le funzioni [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)e [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) .

Tutte le operazioni sui file elencate nella sezione **copiare file**, **eliminare file** o **rinominare file** possono essere aggiunte alla coda usando rispettivamente [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)o [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).

Un altro modo per accodare tutti i file nelle sezioni **copia file** elencati in una sezione di **installazione** di un file inf consiste nell'usare la funzione [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).

Nell'esempio seguente viene usata la funzione [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) per accodare le operazioni di copia per tutti i file elencati in una sezione **copy files** di un file inf.

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

Nell'esempio, la coda è la coda a cui aggiungere le operazioni di copia, "A: \\ " specifica il percorso dell'origine e MyInf è l'handle per il file inf aperto. Il parametro *ListInfHandle* è impostato su **null**, a indicare che la sezione per la copia si trova in MyInf. Section è la sezione in MyInf contenente i file da accodare per la copia.

I flag SP \_ copy \_ NOSKIP e SP \_ copy \_ nobrows sono stati combinati usando un operatore OR per indicare che all'utente non devono essere offerte opzioni per ignorare o cercare i file se si verificano errori.

 

 



