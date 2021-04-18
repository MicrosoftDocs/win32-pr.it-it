---
description: Usare il flag di opzione seguente per specificare che il programma di installazione esegue l'azione personalizzata solo quando viene disinstallata una patch. Per impostare l'opzione, aggiungere il valore di questa tabella al valore nel campo ExtendedType della tabella CustomAction.
ms.assetid: aa4d9e21-5316-42b5-a22e-c7a5becd3cae
title: Opzione di disinstallazione patch azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108365876393733f7cc520ae565bb2c5ea7ff3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319022"
---
# <a name="custom-action-patch-uninstall-option"></a>Opzione di disinstallazione patch azione personalizzata

Usare il flag di opzione seguente per specificare che il programma di installazione esegue l'azione personalizzata solo quando viene disinstallata una patch. Per impostare l'opzione, aggiungere il valore di questa tabella al valore nel campo ExtendedType della [tabella CustomAction](customaction-table.md).

**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato. Questa opzione è disponibile a partire da Windows Installer 4,5.



| Costante                                | Valore esadecimale | Decimal | Descrizione                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| **msidbCustomActionTypePatchUninstall** | 0x8000      | 32768   | L'azione personalizzata viene eseguita solo quando è in corso la disinstallazione di una patch. |



 

## <a name="remarks"></a>Commenti

Questo attributo può essere aggiunto a un'azione personalizzata mediante la relativa creazione nel pacchetto di Windows Installer (file con estensione msi). Una nuova azione personalizzata con questo attributo può essere aggiunta da una patch. Un'azione personalizzata con questo attributo può essere aggiornata da una patch. Questo attributo non può essere aggiunto o rimosso da una patch a un'azione personalizzata esistente.

Se una patch aggiunge o aggiorna un'azione personalizzata con questo attributo, Windows Installer esegue l'azione personalizzata nuova o aggiornata quando la patch viene disinstallata. Windows Installer rende gli aggiornamenti all'interno della patch disinstallati disponibili per l'azione personalizzata di disinstallazione della patch. La patch deve includere una [tabella *<PatchGUID>* MsiTransformView](msitransformview.md) per fornire queste informazioni Windows Installer.

Quando si installa un pacchetto che contiene un'azione personalizzata con l'attributo **msidbCustomActionTypePatchUninstall** con una versione del programma di installazione precedente alla Windows Installer 4,0, il programma di installazione non chiama l'azione personalizzata quando la patch viene disinstallata. L'installazione può eseguire l'azione personalizzata durante l'installazione, il ripristino o l'aggiornamento del pacchetto.

Le azioni personalizzate con l'attributo **msidbCustomActionTypePatchUninstall** devono essere condizionate mediante la proprietà [**MSIPATCHREMOVE**](msipatchremove.md) per impedire l'esecuzione dell'azione personalizzata durante l'installazione, il ripristino o l'aggiornamento tramite un sistema con Windows Installer 4,0 o versioni precedenti. Quando si installa Windows Installer 4,5 e versioni successive, tutte le patch del sistema con azioni personalizzate contrassegnate con l'attributo **msidbCustomActionTypePatchUninstall** eseguono l'azione personalizzata durante la disinstallazione della patch. Se Windows Installer 4,5 o versione successiva viene rimossa dal sistema, le patch perdono la funzionalità di disinstallazione della patch dell'azione personalizzata.

Per informazioni sull'esecuzione di un'azione personalizzata durante la disinstallazione di una patch con una versione precedente alla Windows Installer 4,5, vedere [patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Opzioni di esecuzione In-Script azione personalizzata](custom-action-in-script-execution-options.md)
</dt> <dt>

[Riferimento all'azione personalizzata](custom-action-reference.md)
</dt> <dt>

[Informazioni sulle azioni personalizzate](about-custom-actions.md)
</dt> <dt>

[Uso di azioni personalizzate](using-custom-actions.md)
</dt> <dt>

[MsiTransformView *<PatchGUID>*](msitransformview.md)
</dt> </dl>

 

 



