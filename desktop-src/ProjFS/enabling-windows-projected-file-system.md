---
title: Abilitazione del file System proiettato di Windows
description: Viene descritto come abilitare ProjFS in Windows
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: f903192190877631084e366bcaeafd8b5b0e7e72
ms.sourcegitcommit: 42cdae4d2eca84713ab3f7a5c88f583a352991a8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/23/2019
ms.locfileid: "106297505"
---
# <a name="enabling-windows-projected-file-system"></a>Abilitazione del file System proiettato di Windows

ProjFS viene fornito con Windows come componente facoltativo.  Prima che un provider possa utilizzarlo, è necessario abilitarlo.  È possibile usare <!--the GUI or--> PowerShell per abilitare ProjFS.

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a>Come abilitare ProjFS tramite PowerShell

Per usare PowerShell per abilitare ProjFS, usare il `Enable-WindowsOptionalFeature` cmdlet in una finestra di PowerShell con privilegi elevati:

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

Riavviare il computer se il Enable-WindowsOptionalFeature segnala `RestartNeeded: True` .
