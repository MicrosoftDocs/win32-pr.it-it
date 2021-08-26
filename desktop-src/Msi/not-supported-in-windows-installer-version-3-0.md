---
description: Le funzioni, le tabelle e le proprietà di Windows Installer elencate in questa pagina non sono supportate da Windows Installer&\# 160;3.0 e versioni precedenti.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Non supportato in Windows Installer 3.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398b4211433762c68ed39af012d895d65aeee8fdc5a17f1e6142df76fcbe056c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926301"
---
# <a name="not-supported-in-windows-installer-30"></a>Non supportato in Windows Installer 3.0

Le Windows installer, le tabelle e le proprietà elencate in questa pagina non sono supportate da Windows Installer 3.0 e versioni precedenti. L'assenza di una funzionalità da questo elenco non garantisce che la funzionalità sia supportata. Vedere la documentazione principale per determinare quale Windows del programma di installazione è necessaria per una particolare funzionalità. Per informazioni su altre versioni Windows Installer, vedere [Novità di Windows Installer.](what-s-new-in-windows-installer.md)

Windows Il programma di installazione 3.0 è disponibile per Windows Server 2003, Windows XP o Windows 2000. Per un elenco di tutte le Windows e ridistribuibili del programma di installazione, vedere [Versioni rilasciate di Windows Installer.](released-versions-of-windows-installer.md)

Le funzionalità seguenti non sono supportate in Windows Installer 3.0 e versioni precedenti.

[Funzioni del programma di installazione](installer-functions.md)

-   [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

Prototipo di funzione di callback

-   [**RECORD DEL GESTORE INSTALLUI \_ \_**](/windows/win32/api/msi/nc-msi-installui_handler_record)

[Tabelle di database](database-tables.md)

-   La colonna Value della tabella [MsiPatchMetadata](msipatchmetadata-table.md) accetta **OptimizedInstallMode** e **MinorUpdateTargetRTM.**

[Proprietà](properties.md)

-   [**Proprietà Msix64**](msix64.md)

[Windows Programma di installazione nei sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md)

-   La [**proprietà Riepilogo modello**](template-summary.md) accetta il valore x64.

[Analizzatori di coerenza interna - ICE](internal-consistency-evaluators-ices.md)

-   [ICE99](ice99.md)

 

 
