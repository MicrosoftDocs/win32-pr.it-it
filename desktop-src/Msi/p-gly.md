---
description: Informazioni sui Windows del programma di installazione che iniziano con la lettera P, ad esempio il codice del pacchetto e l'applicazione di patch.
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74af2780852bcb59124390042bfdbbc7bf2e7618cdb4167f58b15fc04ab1b15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942761"
---
# <a name="p-windows-installer"></a>P (Windows di installazione)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**Pacchetto**
</dt> <dd>

[*.msi file ed*](m-gly.md) [*eventuali file di origine esterni*](e-gly.md) a cui può fare riferimento questo file. Un pacchetto contiene quindi tutte le informazioni necessarie Windows installer per eseguire l'interfaccia utente e installare o disinstallare l'applicazione. Per altre informazioni, vedere anche database [*del programma di installazione.*](i-gly.md)

</dd> <dt>

<span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**codice del pacchetto**
</dt> <dd>

GUID che identifica un pacchetto specifico. È necessario un codice di pacchetto univoco perché alcune trasformazioni o pacchetti di patch possono essere applicati a più di un'applicazione o possono aggiornare un'applicazione in un'altra applicazione o versione. Per altre informazioni, vedere [Codici di pacchetto.](package-codes.md)

</dd> <dt>

<span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**Patch**
</dt> <dd>

Metodo di aggiornamento di un file che sostituisce solo i bit modificati, anziché l'intero file. Ciò significa che gli utenti possono scaricare una patch di aggiornamento per un prodotto molto più piccolo dell'intero prodotto. Per altre informazioni, vedere [Patch Packages](patch-packages.md).

</dd> <dt>

<span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**file di patch**
</dt> <dd>

Pacchetto [P atch usato](patch-packages.md) per l'applicazione di patch. Per altre informazioni, vedere [Applicazione di patch e aggiornamenti.](patching-and-upgrades.md)

</dd> <dt>

<span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**modalità di anteprima**
</dt> <dd>

Modalità per la visualizzazione della progettazione dell'interfaccia utente. Per altre informazioni, vedere [Anteprima del Interfaccia utente](previewing-the-user-interface.md).

</dd> <dt>

<span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**Indicatore**
</dt> <dd>

Controllare che il programma di installazione possa essere visualizzato durante l'esecuzione dello script che rappresenta lo stato di avanzamento dell'installazione. Per altre informazioni, vedere [Creazione di un controllo ProgressBar.](authoring-a-progressbar-control.md)

</dd> <dt>

<span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**Proprietà**
</dt> <dd>

Variabili globali usate durante un'installazione. Vedere [Informazioni sulle proprietà.](about-properties.md)

Il termine "proprietà" si riferisce anche a un attributo di un oggetto di automazione. Vedere Interfaccia [di automazione.](automation-interface.md)

</dd> <dt>

<span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**Pubblicazione**
</dt> <dd>

Metodo di [*annuncio di*](a-gly.md) una funzionalità o di un'applicazione. La pubblicazione non popola l'interfaccia utente. Tuttavia, se un'altra applicazione tenta di aprire un'applicazione pubblicata, sono disponibili informazioni sufficienti per il programma di installazione per assegnare l'applicazione pubblicata. Per altre informazioni, vedere [*Assegnazione di*](a-gly.md) componenti [e funzionalità.](components-and-features.md)

</dd> </dl>

 

 



