---
description: Se il criterio di sistema per computer è impostato su 1 (uno), Windows Installer non interagisce con Gestione riavvio, ma userà la finestra di dialogo FilesInUse. se il criterio di sistema per computer è impostato su 2 (due), Windows Installer usa la finestra di dialogo filesinus.
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: DisableAutomaticApplicationShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310527"
---
# <a name="disableautomaticapplicationshutdown"></a>DisableAutomaticApplicationShutdown

Se i criteri di sistema per computer sono impostati su 1 (uno), Windows Installer non interagisce con [Gestione riavvio](/windows/desktop/RstMgr/restart-manager-portal), ma userà la finestra di [dialogo filesinus](filesinuse-dialog.md).

Se il criterio di sistema per computer è impostato su 2 (due), Windows Installer usa la [finestra di dialogo Filesinusale](filesinuse-dialog.md). Questa impostazione Disabilita i tentativi da parte di [Gestione riavvio](/windows/desktop/RstMgr/restart-manager-portal) per ridurre i riavvii durante l'installazione di un pacchetto di Windows Installer che non è stato creato per usare Gestione riavvio. Il programma di installazione utilizza ancora Gestione riavvio per rilevare i file utilizzati dalle applicazioni.

Il criterio DisableAutomaticApplicationShutdown è disponibile a partire dalla versione Windows Installer 4,0 in Windows Vista.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
</dt> <dt>

[Non supportato in Windows Installer 3,1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
