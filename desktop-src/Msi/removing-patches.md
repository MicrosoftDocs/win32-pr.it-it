---
description: A partire da Windows Installer&\# 160;versione&160;3.0, è possibile creare e installare patch che possono essere disinstallate in modo autonomo e in qualsiasi ordine, senza dover disinstallare e reinstallare l'intera applicazione e \# altre patch.
ms.assetid: 2ad30ac9-eac9-49cf-98ae-5c053a0b500a
title: Rimozione di patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18998207ead28729101fd8782432cb25bf31f0d4763faa8e99c341f9b1fde7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990701"
---
# <a name="removing-patches"></a>Rimozione di patch

A partire da Windows Installer versione 3.0, è possibile creare e installare patch che possono essere disinstallate in modo autonomo e in qualsiasi ordine, senza dover disinstallare e reinstallare l'intera applicazione e altre patch. Windows Il programma di installazione 3.0 consente anche di creare pacchetti [di patch](patch-packages.md) con una tabella [MsiPatchSequence](msipatchsequence-table.md) che contiene informazioni sulla sequenziazione delle patch. Con le versioni di Windows Installer precedenti Windows Installer 3.0, l'unico metodo per rimuovere determinate patch da un'applicazione è disinstallare l'intera applicazione con patch e quindi reinstallarla senza riapplicare le patch rimosse.

La disinstallazione di una patch dipende dalla modalità di creazione della patch, dalla versione del programma di installazione di Windows usata per installare la patch e dalle modifiche apportate dalla patch all'applicazione. Se una patch non è disinstallabile, l'unico modo per rimuoverla è disinstallare l'intera applicazione e reinstallarla senza applicare la patch da rimuovere.

È possibile disinstallare una o più patch usando un'opzione della riga di comando, l'interfaccia di scripting o chiamando [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) da un'altra applicazione. Per [altre informazioni su come disinstallare le patch,](uninstalling-patches.md) vedere Disinstallazione di patch.

Il valore della [**proprietà MSIPATCHREMOVE**](msipatchremove.md) elenca le patch da disinstallare. Per ogni patch nell'elenco, il programma di installazione verifica che la patch sia disinstallabile. Se l'utente non dispone dei privilegi per rimuovere la patch, la patch è sconosciuta per il prodotto, i criteri di patch impediscono la rimozione o la patch è stata contrassegnata come non disinstallabile, il programma di installazione restituisce un errore che indica una transazione di installazione non riuscita. Per [altre informazioni su ciò che](uninstallable-patches.md) determina se una patch non è disinstallabile, vedere Patch disinstallabili.

Dopo che la patch è stata verificata come rimovibile, il programma di installazione rimuove la patch dalla sequenza dell'applicazione patch. Per altre informazioni su come Windows Installer 3.0 determina la sequenza da usare per l'applicazione di patch, vedere [Sequenziazione delle patch](sequencing-patches.md). Si noti che la rimozione di patch dalla sequenza può causare l'attività delle patch contrassegnate come obsolete o sostituite.

Tutte le patch selezionate per la rimozione sono elencate nella [**proprietà MsiPatchRemovalList.**](msipatchremovallist.md) Questa proprietà è una proprietà privata impostata dal programma di installazione e può essere utilizzata nelle espressioni condizionali o su cui vengono eseguite query da [azioni personalizzate.](custom-actions.md) La proprietà contiene l'elenco dei GUID del codice patch delle patch da rimuovere. Un'azione personalizzata può determinare se lo stato di installazione della patch viene applicato, obsoleto o sostituito chiamando [**msiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o la [**proprietà PatchProperty**](patch-patchproperty.md) dell'oggetto [patch](patch-object.md).

Dopo la rimozione di una patch, lo stato dell'applicazione è uguale a quello di se la patch non è mai stata installata. Se possibile, il programma di installazione limita il processo al subset di funzionalità interessate dalla patch da rimuovere. Il programma di installazione imposta [**automaticamente**](reinstall.md) la proprietà REINSTALL sull'elenco delle funzionalità interessate. I file aggiunti dalla patch vengono rimossi e i file modificati dalla patch vengono sovrascritti. I file e le voci del Registro di sistema vengono ripristinati alla versione prevista dal prodotto meno la patch. Le funzionalità e i componenti aggiunti dalla patch vengono annullati dall'applicazione. Si noti che il contenuto aggiuntivo aggiunto dalla patch può rimanere nel computer dell'utente se il contenuto viene usato da un'altra patch ancora applicabile.

Se un file di un componente condiviso viene aggiornato da una patch, la modifica influisce su tutte le applicazioni che condividono il componente. Quando la patch viene rimossa, la modifica influisce su tutte le applicazioni che condividono il componente. Ciò significa che la rimozione di una patch da parte di un'applicazione può ripristinare il file del componente condiviso a una versione inferiore a quella richiesta da un'altra applicazione. In questo modo è possibile correggere la prima applicazione, ma la seconda applicazione smette di funzionare. In questo caso, la seconda applicazione può essere ripristinata reinstallando la seconda applicazione usando i metodi descritti in [Reinstallazione di una funzionalità o di un'applicazione](reinstalling-a-feature-or-application.md). Verrà ripristinata la versione con patch del file.

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

[Sequenziazione delle patch](sequencing-patches.md)
</dt> <dt>

[Azioni personalizzate di disinstallazione patch](patch-uninstall-custom-actions.md)
</dt> <dt>

[Patch disinstallabili](uninstallable-patches.md)
</dt> <dt>

[Disinstallazione delle patch](uninstalling-patches.md)
</dt> </dl>

 

 



