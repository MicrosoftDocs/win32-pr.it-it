---
description: Ogni file che viene recapitato al pacchetto di installazione di destinazione dal modulo merge deve essere archiviato all'interno di un file CAB incorporato come flusso all'interno del file. msm. Il nome di questo file CAB è sempre MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Generazione di MergeModule.CABfile CAB inet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a26eb9bb3daf92d81e21267b2f56706b74d9179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314264"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a>Generazione di MergeModule.CABfile CAB inet

Ogni file che viene recapitato al pacchetto di installazione di destinazione dal modulo merge deve essere archiviato all'interno di un file CAB incorporato come flusso all'interno del file. msm. Il nome di questo file CAB è sempre MergeModule.CABinet.

I nomi dei file in MergeModule.CABinet devono corrispondere alle chiavi primarie utilizzate nella [tabella dei file](file-table.md) del modulo merge e devono rispettare la convenzione descritta in [denominazione delle chiavi primarie nei database dei moduli di merge](naming-primary-keys-in-merge-module-databases.md).

Il programma di installazione ignora i file aggiuntivi inclusi in MergeModule.CABinet che non sono elencati nella [tabella file](file-table.md)del modulo merge. I numeri di sequenza dei file specificati nella tabella file non devono essere consecutivi, ma devono seguire la stessa sequenza dei file archiviati all'interno di MergeModule.CABinet. Per ulteriori informazioni, vedere [creazione di tabelle di file del modulo merge](authoring-merge-module-file-tables.md).

Ciò significa che un singolo file CAB può contenere tutti i file necessari per il supporto di più lingue da parte di un modulo merge. A tutti i file della lingua è possibile assegnare numeri di sequenza univoci nel file CAB, quindi è possibile utilizzare una trasformazione lingua per aggiungere o rimuovere file dalla tabella file per ottenere un modulo merge per una determinata lingua. Per informazioni dettagliate, vedere la pagina relativa alla creazione di modelli di [Unione di più linguaggi](authoring-multiple-language-merge-modules.md).

È possibile aggiungere MergeModule.CABinet al modulo merge aprendo una [ \_ tabella dei flussi](-streams-table.md)temporanei. Ad esempio, lo strumento Msidb.exe fornito con Windows Installer SDK può essere usato per aggiungere il MergeModule.CABinet al modulo merge. Per ulteriori informazioni, vedere [inclusione di un file CAB in un'installazione](including-a-cabinet-file-in-an-installation.md).

 

 



