---
description: Ogni file recapitato al pacchetto di installazione di destinazione dal modulo unione deve essere archiviato all'interno di un file cab incorporato come flusso all'interno del file con estensione msm. Il nome di questo archivio è sempre MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Generazione di MergeModule.CABfile CAB inet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 962cf46b95db1fe186878d23a7cc7fcd1b91d3b2d202a85741eee7ef1c2bc7e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649650"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a>Generazione di MergeModule.CABfile CAB inet

Ogni file recapitato al pacchetto di installazione di destinazione dal modulo unione deve essere archiviato all'interno di un file cab incorporato come flusso all'interno del file con estensione msm. Il nome di questo archivio è sempre MergeModule.CABinet.

I nomi dei file in MergeModule.CABinet devono corrispondere alle chiavi primarie usate nella tabella [File](file-table.md) del modulo di merge e devono rispettare la convenzione descritta in [Denominazione](naming-primary-keys-in-merge-module-databases.md)delle chiavi primarie nei database del modulo unione .

Il programma di installazione ignora i file aggiuntivi inclusi MergeModule.CABinet non elencati nella tabella [File del modulo unione.](file-table.md) I numeri di sequenza dei file specificati nella tabella File non devono essere consecutivi, ma devono seguire la stessa sequenza dei file archiviati all'interno MergeModule.CABinet. Per altre informazioni, vedere [Creazione di tabelle di file del modulo unione](authoring-merge-module-file-tables.md).

Ciò significa che un singolo file CAB può contenere tutti i file necessari per il supporto di più lingue in un modulo unione. A tutti i file di lingua possono essere assegnati numeri di sequenza univoci nel file cab e quindi è possibile usare una trasformazione linguistica per aggiungere o rimuovere file dalla tabella File per ottenere un modulo unione per una determinata lingua. Per informazioni dettagliate, vedere [Creazione di moduli unione in più linguaggi.](authoring-multiple-language-merge-modules.md)

MergeModule.CAB'inet può essere aggiunto al modulo unione aprendo una tabella [ \_ Flussi tabella](-streams-table.md). Ad esempio, lo strumento Msidb.exe fornito con Windows Installer SDK può essere usato per aggiungere l'MergeModule.CABinet al modulo unione. Per altre informazioni, vedere [Inclusione di un file CAB in un'installazione](including-a-cabinet-file-in-an-installation.md).

 

 



