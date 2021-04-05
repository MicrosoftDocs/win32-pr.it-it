---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4e6b8f1343fdd68f4a6ce042852cff1e28e05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131475"
---
# <a name="p-windows-installer"></a>P (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**pacchetto**
</dt> <dd>

[*file con estensione msi*](m-gly.md) ed eventuali [*file di origine esterni*](e-gly.md) a cui il file può fare riferimento. Un pacchetto contiene pertanto tutte le informazioni necessarie per l'Windows Installer l'esecuzione dell'interfaccia utente e per l'installazione o la disinstallazione dell'applicazione. Per ulteriori informazioni, vedere anche [*database del programma di installazione*](i-gly.md).

</dd> <dt>

<span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**codice pacchetto**
</dt> <dd>

GUID che identifica un pacchetto specifico. È necessario un codice di pacchetto univoco perché alcune trasformazioni o pacchetti di patch possono essere applicati a più di un'applicazione o possono aggiornare un'applicazione in un'altra applicazione o versione. Per ulteriori informazioni, vedere [codici di pacchetto](package-codes.md).

</dd> <dt>

<span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patch**
</dt> <dd>

Metodo di aggiornamento di un file che sostituisce solo i bit modificati, anziché l'intero file. Questo significa che gli utenti possono scaricare una patch di aggiornamento per un prodotto molto più piccolo dell'intero prodotto. Per ulteriori informazioni, vedere la pagina relativa ai [pacchetti di patch](patch-packages.md).

</dd> <dt>

<span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**file patch**
</dt> <dd>

P [prodotto pacchetto](patch-packages.md) usato per l'applicazione di patch. Per ulteriori informazioni, vedere applicazione di [patch e aggiornamenti](patching-and-upgrades.md).

</dd> <dt>

<span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**modalità anteprima**
</dt> <dd>

Modalità per la visualizzazione della progettazione dell'interfaccia utente. Per ulteriori informazioni, vedere [anteprima dell'interfaccia utente](previewing-the-user-interface.md).

</dd> <dt>

<span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**indicatore di stato**
</dt> <dd>

Controllo che il programma di installazione può visualizzare durante l'esecuzione dello script che rappresenta lo stato di avanzamento dell'installazione. Per ulteriori informazioni, vedere la pagina relativa alla [creazione di un controllo ProgressBar](authoring-a-progressbar-control.md).

</dd> <dt>

<span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**Proprietà**
</dt> <dd>

Variabili globali utilizzate durante un'installazione. Vedere [informazioni sulle proprietà](about-properties.md).

Il termine "Property" si riferisce anche a un attributo di un oggetto di automazione. (Vedere [interfaccia di automazione](automation-interface.md)).

</dd> <dt>

<span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**editrice**
</dt> <dd>

Metodo di [*annuncio*](a-gly.md) di una funzionalità o di un'applicazione. La pubblicazione non popola l'interfaccia utente. Tuttavia, se un'altra applicazione tenta di aprire un'applicazione pubblicata, per il programma di installazione sono disponibili informazioni sufficienti per l'assegnazione dell'applicazione pubblicata. Per ulteriori informazioni, vedere [*assegnazione*](a-gly.md) di [componenti e funzionalità](components-and-features.md).

</dd> </dl>

 

 



