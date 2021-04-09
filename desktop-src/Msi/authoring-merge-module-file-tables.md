---
description: In ogni modulo merge è necessaria una tabella di file e deve avere un record per ogni file che viene recapitato al pacchetto di installazione di destinazione dal modulo merge.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Creazione di tabelle di file del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2687ed69c1a0362f96db896a5fdf4237ac4681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049910"
---
# <a name="authoring-merge-module-file-tables"></a>Creazione di tabelle di file del modulo merge

In ogni modulo merge è necessaria una [tabella di file](file-table.md) e deve avere un record per ogni file che viene recapitato al pacchetto di installazione di destinazione dal modulo merge. Quando il modulo merge viene unito in un file con estensione msi, ogni file nella tabella dei file del modulo merge viene archiviato in un [*file CAB*](c-gly.md) nel file con estensione MSM. Il nome del file CAB in un modulo merge è sempre il seguente: MergeModule.CABinet.

Per altre informazioni, vedere [generazione di file CAB di MergeModule.CABinet](generating-mergemodule-cabinet-cabinet-files.md).

-   Poiché i file di un modulo merge vengono sempre archiviati all'interno di un file CAB, non è necessario impostare i flag di bit **msidbFileAttributesNoncompressed** o **MsidbFileAttributesCompressed** nella colonna attributi della [tabella file](file-table.md).
-   I nomi dei file in MergeModule.CABinet devono corrispondere alla chiave primaria nella [tabella dei file](file-table.md)del modulo merge.

    La colonna file è la chiave primaria della [tabella file](file-table.md) e le voci di questo campo devono seguire la convenzione descritta in [denominazione di chiavi primarie nei database dei moduli di merge](naming-primary-keys-in-merge-module-databases.md).

-   I numeri di sequenza del file vengono specificati nella colonna sequenza della [tabella dei file](file-table.md).

    I file devono essere elencati nella [tabella dei file](file-table.md) del modulo merge nella stessa sequenza in cui sono archiviati in MergeModule.CABinet. I numeri di sequenza dei file non devono essere consecutivi, ma devono seguire la stessa sequenza dei file archiviati all'interno del cabinet. Ad esempio, il primo, il secondo e il terzo file archiviati nell'archivio possono avere i numeri di sequenza 100, 200 e 300.

-   Il programma di installazione ignora i file aggiuntivi inclusi in MergeModule.CABinet che non sono elencati nella [tabella file](file-table.md).

    Un file CAB può contenere tutti i file necessari per un modulo merge che supporta più lingue usando le trasformazioni. A tutti i file della lingua può essere assegnato un numero di sequenza univoco nell'archivio, quindi una trasformazione può aggiungere o rimuovere file dalla [tabella file](file-table.md) quando necessario per una lingua specifica. Per ulteriori informazioni, vedere la pagina relativa alla creazione di modelli di [Unione di più linguaggi](authoring-multiple-language-merge-modules.md).

Per ulteriori informazioni, vedere [file table](file-table.md).

 

 



