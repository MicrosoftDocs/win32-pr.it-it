---
description: È possibile utilizzare l'opzione di disinstallazione patch azione personalizzata per specificare che il programma di installazione esegue l'azione personalizzata solo quando viene disinstallata una patch.
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: Patch disinstallare azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90cfffbdb37f1f2fab046b794010a790e9a5212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306575"
---
# <a name="patch-uninstall-custom-actions"></a>Patch disinstallare azioni personalizzate

È possibile utilizzare l' [opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md) per specificare che il programma di installazione esegue l'azione personalizzata solo quando viene disinstallata una patch.

**Windows Installer 4,5 e versioni successive:** È possibile utilizzare l' [opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md) per specificare che il programma di installazione esegue l'azione personalizzata solo quando viene disinstallata una patch.

**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md): * *

L' [opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md) non è disponibile. Non esiste alcun metodo per contrassegnare un' [azione personalizzata](custom-actions.md) all'interno di un pacchetto di patch da eseguire quando la patch viene disinstallata perché il programma di installazione non applica i pacchetti di patch da disinstallare.

Per eseguire un' [azione personalizzata](custom-actions.md) quando viene disinstallata una patch particolare, è necessario che l'azione personalizzata sia presente nell'applicazione originale o che si trovi in una patch per il prodotto che viene sempre applicato.

Gli sviluppatori possono utilizzare la proprietà [**MsiPatchRemovalList**](msipatchremovallist.md) per creare un pacchetto di Windows Installer o una patch che esegue [azioni personalizzate](custom-actions.md) sulla rimozione di una patch. L'azione personalizzata può essere creata nel pacchetto di installazione originale, una patch che è già stata applicata al pacchetto o una patch che non è una [patch non installabile](uninstallable-patches.md). L'azione personalizzata può essere condizionata nella proprietà **MsiPatchRemovalList** delle tabelle di sequenza. Per ulteriori informazioni sulle azioni conditionalizing, vedere [utilizzo delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md) .

L'azione personalizzata può ottenere i GUID delle patch da rimuovere dal valore della proprietà [**MsiPatchRemovalList**](msipatchremovallist.md) . L'azione personalizzata può determinare se lo stato di installazione della patch è applicato, obsoleto o sostituito chiamando il [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o la proprietà [**PatchProperty**](patch-patchproperty.md) dell' [oggetto patch](patch-object.md).

Se l'azione personalizzata richiede metadati speciali dalla patch, la patch deve contenere un'azione personalizzata che scrive i metadati in un percorso del registro di sistema o di file quando viene applicata la patch. L'azione personalizzata nell'applicazione originale o una patch che viene sempre applicata può ottenere le informazioni necessarie per rimuovere le modifiche apportate alla patch.

Le patch che apportano modifiche difficili da annullare correttamente non devono essere contrassegnate come [patch non installabili](uninstallable-patches.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenza di patch](sequencing-patches.md)
</dt> <dt>

[Rimozione di patch](removing-patches.md)
</dt> <dt>

[Patch disinstallabili](uninstallable-patches.md)
</dt> <dt>

[Disinstallazione di patch](uninstalling-patches.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



