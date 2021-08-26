---
description: Una tabella file è necessaria in ogni modulo unione e deve avere un record per ogni file recapitato al pacchetto di installazione di destinazione dal modulo unione.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Creazione di tabelle di file del modulo unione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715fe570a96015f62e45b0c2924b2a83be8eefc067e5d054decd59110b7797c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045471"
---
# <a name="authoring-merge-module-file-tables"></a>Creazione di tabelle di file del modulo unione

Una [tabella file](file-table.md) è necessaria in ogni modulo unione e deve avere un record per ogni file recapitato al pacchetto di installazione di destinazione dal modulo unione. Quando il modulo unione viene unito in un file .msi, ogni file nella tabella file del modulo unione viene archiviato all'interno di un [*file cab*](c-gly.md) nel file con estensione msm. Il nome dell'archivio in un modulo unione è sempre il seguente: MergeModule.CABinet.

Per altre informazioni, vedere [Generazione di MergeModule.CABfile CAB inet](generating-mergemodule-cabinet-cabinet-files.md).

-   Poiché i file di un modulo unione vengono sempre archiviati all'interno di un file cab, non è necessario impostare i flag di bit **msidbFileAttributesNoncompressed** o **msidbFileAttributesCompressed** nella colonna Attributi della tabella [file](file-table.md).
-   I nomi dei file in MergeModule.CABinet devono corrispondere alla chiave primaria nella tabella file del modulo [unione.](file-table.md)

    La colonna File è la chiave primaria della tabella [File](file-table.md) e le voci in questo campo devono seguire la convenzione descritta in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).

-   I numeri di sequenza dei file vengono specificati nella colonna Sequenza della [tabella file](file-table.md).

    I file devono essere elencati nella tabella [file](file-table.md) del modulo unione nella stessa sequenza in cui sono archiviati MergeModule.CABinet. I numeri di sequenza dei file non devono essere consecutivi, ma devono seguire la stessa sequenza dei file archiviati all'interno dell'archivio. Ad esempio, il primo, il secondo e il terzo file archiviati nell'archivio possono avere i numeri di sequenza 100, 200 e 300.

-   Il programma di installazione ignora i file aggiuntivi inclusi MergeModule.CABinet non elencati nella [tabella file](file-table.md).

    Un file cab può contenere tutti i file necessari per un modulo unione che supporta più lingue tramite trasformazioni. A tutti i file di lingua può essere assegnato un numero di sequenza univoco nell'archivio e quindi una trasformazione può aggiungere o rimuovere file dalla tabella [file](file-table.md) quando necessario per una lingua specifica. Per altre informazioni, vedere [Creazione di moduli unione in più linguaggi.](authoring-multiple-language-merge-modules.md)

Per altre informazioni, vedere [Tabella file](file-table.md).

 

 



