---
description: Le funzioni, le tabelle e le proprietà Windows Installer elencate in questa pagina non sono supportate da Windows Installer&\# 160; 3.0 e versioni precedenti.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Non supportato in Windows Installer 3,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310514"
---
# <a name="not-supported-in-windows-installer-30"></a>Non supportato in Windows Installer 3,0

Le funzioni, le tabelle e le proprietà Windows Installer elencate in questa pagina non sono supportate da Windows Installer 3,0 e versioni precedenti. L'assenza di una funzionalità da questo elenco non garantisce che la funzionalità sia supportata. Vedere la documentazione principale per determinare quale versione di Windows Installer è necessaria per una determinata funzionalità. Per informazioni sulle altre versioni di Windows Installer, vedere Novità [di Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 3,0 è disponibile per Windows Server 2003, Windows XP o Windows 2000. Per un elenco di tutte le versioni Windows Installer e i ridistribuibili, vedere [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md).

Le funzionalità seguenti non sono supportate in Windows Installer 3,0 e versioni precedenti.

[Funzioni di installazione](installer-functions.md)

-   [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

Prototipo di funzione di callback

-   [**\_record gestore \_ INSTALLUI**](/windows/win32/api/msi/nc-msi-installui_handler_record)

[Tabelle di database](database-tables.md)

-   La colonna valore della [tabella MsiPatchMetadata](msipatchmetadata-table.md) accetta **OptimizedInstallMode** e **MinorUpdateTargetRTM**.

[Proprietà](properties.md)

-   [**Proprietà Msix64**](msix64.md)

[Windows Installer su sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md)

-   La [**proprietà di riepilogo del modello**](template-summary.md) accetta il valore x64.

[Analizzatori di coerenza interni-CIEM](internal-consistency-evaluators-ices.md)

-   [ICE99](ice99.md)

 

 
