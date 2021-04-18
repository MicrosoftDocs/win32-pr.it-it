---
description: A partire da Windows Installer&\# 160; versione&\# 160; 3.0, è possibile creare e installare patch che possono essere disinstallate singolarmente e in qualsiasi ordine senza dover disinstallare e reinstallare l'intera applicazione e altre patch.
ms.assetid: 2ad30ac9-eac9-49cf-98ae-5c053a0b500a
title: Rimozione di patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd54db3bde3a356a0c3adb299555248bbc87a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313800"
---
# <a name="removing-patches"></a>Rimozione di patch

A partire da Windows Installer versione 3,0, è possibile creare e installare patch che possono essere disinstallate singolarmente e in qualsiasi ordine senza dover disinstallare e reinstallare l'intera applicazione e altre patch. Windows Installer 3,0 consente inoltre di creare [pacchetti di patch](patch-packages.md) con una [tabella MsiPatchSequence](msipatchsequence-table.md) che contiene informazioni di sequenziazione delle patch. Con le versioni di Windows Installer precedenti alla Windows Installer 3,0, l'unico metodo per rimuovere determinate patch da un'applicazione consiste nel disinstallare l'intera applicazione con patch e quindi reinstallare senza riapplicare le patch rimosse.

Il fatto che una patch possa essere disinstallata dipende dalla modalità di creazione della patch, dalla versione di Windows Installer usata per installare la patch e dalle modifiche apportate dalla patch all'applicazione. Se una patch non è disinstallabile, l'unico modo per rimuovere la patch è disinstallare l'intera applicazione e reinstallare senza applicare la patch da rimuovere.

È possibile disinstallare una o più patch usando un'opzione della riga di comando, l'interfaccia di scripting o chiamando [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) da un'altra applicazione. Per ulteriori informazioni su come disinstallare le patch, vedere [Disinstallazione delle patch](uninstalling-patches.md) .

Il valore della proprietà [**MSIPATCHREMOVE**](msipatchremove.md) elenca le patch da disinstallare. Per ogni patch nell'elenco, il programma di installazione verifica che la patch sia disinstallabile. Se l'utente non dispone dei privilegi necessari per rimuovere la patch, la patch non è nota per il prodotto, il criterio patch impedisce la rimozione o la patch è stata contrassegnata come non disinstallabile, il programma di installazione restituisce un errore che indica una transazione di installazione non riuscita. Per ulteriori informazioni su come determinare se una patch non è disinstallabile, vedere [patch disinstallabili](uninstallable-patches.md) .

Quando la patch viene verificata come rimovibile, il programma di installazione rimuove la patch dalla sequenza dell'applicazione patch. Per ulteriori informazioni su come Windows Installer 3,0 determina quale sequenza utilizzare quando si applicano le patch, vedere [sequenziazione delle patch](sequencing-patches.md). Si noti che la rimozione di patch dalla sequenza può causare l'attivazione delle patch contrassegnate come obsolete o sostituite.

Tutte le patch selezionate per la rimozione sono elencate nella proprietà [**MsiPatchRemovalList**](msipatchremovallist.md) . Questa proprietà è una proprietà privata impostata dal programma di installazione e può essere utilizzata nelle espressioni condizionali o sottoposta a query da [azioni personalizzate](custom-actions.md). La proprietà contiene l'elenco dei GUID di codice delle patch da rimuovere. Un'azione personalizzata può determinare se lo stato di installazione della patch è applicato, obsoleto o sostituito chiamando il [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o la proprietà [**PatchProperty**](patch-patchproperty.md) dell' [oggetto patch](patch-object.md).

Dopo la rimozione di una patch, lo stato dell'applicazione è identico a quello in cui la patch non è mai stata installata. Se possibile, il programma di installazione limita il processo al subset di funzionalità interessate dalla patch da rimuovere. Il programma di installazione imposta automaticamente la proprietà [**REINSTALL**](reinstall.md) sull'elenco delle funzionalità interessate. I file aggiunti dalla patch vengono rimossi e i file modificati dalla patch vengono sovrascritti. I file e le voci del registro di sistema vengono ripristinati nella versione prevista dal prodotto meno la patch. La registrazione delle funzionalità e dei componenti aggiunti dalla patch viene annullata dall'applicazione. Si noti che il contenuto aggiuntivo aggiunto dalla patch può rimanere nel computer dell'utente se il contenuto viene usato da un'altra patch ancora applicabile.

Se un file di un componente condiviso viene aggiornato da una patch, la modifica avrà effetto su tutte le applicazioni che condividono il componente. Quando la patch viene rimossa, la modifica ha effetto su tutte le applicazioni che condividono il componente. Ciò significa che la rimozione di una patch da parte di un'applicazione può ripristinare il file del componente condiviso a una versione precedente rispetto a quella richiesta da un'altra applicazione. Questa operazione potrebbe risolvere la prima applicazione, ma la seconda applicazione smette di funzionare. In questo caso, la seconda applicazione può essere ripristinata reinstallando la seconda applicazione usando i metodi descritti in [reinstallazione di una funzionalità o di un'applicazione](reinstalling-a-feature-or-application.md). Verrà ripristinata la versione con patch del file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Sequenza di patch](sequencing-patches.md)
</dt> <dt>

[Patch disinstallare azioni personalizzate](patch-uninstall-custom-actions.md)
</dt> <dt>

[Patch disinstallabili](uninstallable-patches.md)
</dt> <dt>

[Disinstallazione di patch](uninstalling-patches.md)
</dt> </dl>

 

 



