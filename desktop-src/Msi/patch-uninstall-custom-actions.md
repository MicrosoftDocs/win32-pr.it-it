---
description: È possibile usare l'opzione Custom Action Patch Uninstall per specificare che il programma di installazione deve eseguire l'azione personalizzata solo quando viene disinstallata una patch.
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: Azioni personalizzate di disinstallazione patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69077337b80177984ff43f12038edb1daa48215f92c627f4ed22ea2f69c876b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145424"
---
# <a name="patch-uninstall-custom-actions"></a>Azioni personalizzate di disinstallazione patch

È possibile usare [l'opzione Custom Action Patch Uninstall](custom-action-patch-uninstall-option.md) per specificare che il programma di installazione deve eseguire l'azione personalizzata solo quando viene disinstallata una patch.

**Windows Installer 4.5 e versioni successive:** È possibile usare [l'opzione custom action patch uninstall per](custom-action-patch-uninstall-option.md) specificare che il programma di installazione esegue l'azione personalizzata solo quando viene disinstallata una patch.

**[Windows Installer 4.0 e versioni precedenti](not-supported-in-windows-installer-4-0.md): **

[L'opzione Custom Action Patch Uninstall (Disinstallazione patch](custom-action-patch-uninstall-option.md) azione personalizzata) non è disponibile. Non esiste alcun metodo [](custom-actions.md) per contrassegnare un'azione personalizzata all'interno di un pacchetto di patch da eseguire quando la patch viene disinstallata perché il programma di installazione non applica i pacchetti di patch da disinstallare.

Per eseguire [un'azione](custom-actions.md) personalizzata quando viene disinstallata una determinata patch, l'azione personalizzata deve essere presente nell'applicazione originale o essere in una patch per il prodotto che viene sempre applicata.

Gli sviluppatori possono usare la [**proprietà MsiPatchRemovalList**](msipatchremovallist.md) per creare un [](custom-actions.md) pacchetto Windows Installer o una patch che esegue azioni personalizzate sulla rimozione di una patch. È possibile creare l'azione personalizzata nel pacchetto di installazione originale, in una patch già applicata al pacchetto o in una patch che non è una [patch disinstallabile.](uninstallable-patches.md) L'azione personalizzata può essere condizionale nella **proprietà MsiPatchRemovalList** nelle tabelle di sequenza. Per [altre informazioni sulla condizionalizzazione delle azioni,](using-properties-in-conditional-statements.md) vedere Uso delle proprietà nelle istruzioni condizionali.

L'azione personalizzata può ottenere i GUID delle patch rimosse dal valore della [**proprietà MsiPatchRemovalList.**](msipatchremovallist.md) L'azione personalizzata può determinare se lo stato di installazione della patch viene applicato, obsoleto o sostituito chiamando [**msiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o la [**proprietà PatchProperty**](patch-patchproperty.md) dell'oggetto [Patch](patch-object.md).

Se l'azione personalizzata richiede metadati speciali dalla patch, la patch deve contenere un'azione personalizzata che scrive i metadati in un registro o in un percorso di file quando viene applicata la patch. L'azione personalizzata nell'applicazione originale o in una patch sempre applicata può ottenere le informazioni necessarie per rimuovere le modifiche della patch.

Le patch che apportano modifiche difficili da annullare correttamente non devono essere contrassegnate come [patch disinstallabili.](uninstallable-patches.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenziazione delle patch](sequencing-patches.md)
</dt> <dt>

[Rimozione di patch](removing-patches.md)
</dt> <dt>

[Patch disinstallabili](uninstallable-patches.md)
</dt> <dt>

[Disinstallazione delle patch](uninstalling-patches.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



