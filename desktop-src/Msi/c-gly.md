---
description: Informazioni sui Windows Installer concetti che iniziano con la lettera C, ad esempio file cab e checksum.
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: C (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e7af99ad32d8dff7f4e8509976b0004045477b
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010924"
---
# <a name="c-windows-installer"></a>C (Windows Installer)

[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P Q](p-gly.md) [](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**file cab**
</dt> <dd>

Singolo file, in genere con un'.cab, che archivia i file compressi in una libreria di file. Il formato cab è un modo efficiente per creare un pacchetto di più file perché la compressione viene eseguita tra i limiti dei file, migliorando in modo significativo il rapporto di compressione. Per informazioni sulla creazione di file cab, vedere [File CAB](cabinet-files.md).

</dd> <dt>

<span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**Checksum**
</dt> <dd>

Valore calcolato che dipende dal contenuto di un file. Viene archiviato con i dati per rilevare il danneggiamento dei file. Il sistema controlla questo valore per assicurarsi che i dati non siano interrotta.

</dd> <dt>

<span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**Componente**
</dt> <dd>

Parte più piccola di un'installazione gestita dal programma di installazione, anche un blocco predefinito di un'applicazione o di una funzionalità dal punto di vista del programmatore. Esempi di componenti sono un gruppo di file correlati, un oggetto COM o una libreria. Per altre informazioni, vedere [Componenti e funzionalità](components-and-features.md).

</dd> <dt>

<span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**commit di database**
</dt> <dd>

Modifiche accumulate apportate in un database. Le modifiche vengono riflesse nel database effettivo solo dopo il commit del database. Per altre informazioni, vedere [Commit di database](committing-databases.md).

</dd> <dt>

<span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**
</dt> <dd>

Aspetto della funzionalità dell'interfaccia utente del programma di installazione. Un tipico ControlEvent attiva un'azione da parte del programma di installazione all'attivazione di un controllo della finestra di dialogo o di un altro evento. Per altre informazioni, vedere [Cenni preliminari su ControlEvent](controlevent-overview.md).

</dd> <dt>

<span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**Costano**
</dt> <dd>

Metodo usato dal programma di installazione per determinare i requisiti di spazio su disco per l'installazione. La determinazione dei costi tiene conto di fattori quali la necessità di sovrascrittura dei file esistenti. Per altre informazioni, vedere [Determinazione dei costi dei file.](file-costing.md)

</dd> <dt>

<span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**File con estensione cub**
</dt> <dd>

Modulo di convalida che archivia e fornisce l'accesso alle azioni personalizzate ICE. Per altre informazioni, vedere [File con estensione cub di esempio.](sample--cub-file.md) Per altre informazioni, vedere anche Windows Installer [file .](windows-installer-file-extensions.md)

</dd> <dt>

<span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**azione personalizzata**
</dt> <dd>

Scritto dall'autore del [*pacchetto ma*](p-gly.md) non incorporato nel programma di installazione come azione standard. Per altre informazioni, vedere [Azioni personalizzate](custom-actions.md).

</dd> </dl>

 

 



