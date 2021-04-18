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
# <a name="enabling-windows-projected-file-system"></a><span data-ttu-id="e14ca-103">Abilitazione del file System proiettato di Windows</span><span class="sxs-lookup"><span data-stu-id="e14ca-103">Enabling Windows Projected File System</span></span>

<span data-ttu-id="e14ca-104">ProjFS viene fornito con Windows come componente facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e14ca-104">ProjFS ships with Windows as an Optional Component.</span></span>  <span data-ttu-id="e14ca-105">Prima che un provider possa utilizzarlo, è necessario abilitarlo.</span><span class="sxs-lookup"><span data-stu-id="e14ca-105">Before a provider can use it, it must be enabled.</span></span>  <span data-ttu-id="e14ca-106">È possibile usare</span><span class="sxs-lookup"><span data-stu-id="e14ca-106">You can use</span></span> <!--the GUI or--> <span data-ttu-id="e14ca-107">PowerShell per abilitare ProjFS.</span><span class="sxs-lookup"><span data-stu-id="e14ca-107">PowerShell to enable ProjFS.</span></span>

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a><span data-ttu-id="e14ca-108">Come abilitare ProjFS tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="e14ca-108">How to enable ProjFS using PowerShell</span></span>

<span data-ttu-id="e14ca-109">Per usare PowerShell per abilitare ProjFS, usare il `Enable-WindowsOptionalFeature` cmdlet in una finestra di PowerShell con privilegi elevati:</span><span class="sxs-lookup"><span data-stu-id="e14ca-109">To use PowerShell to enable ProjFS use the `Enable-WindowsOptionalFeature` cmdlet in an elevated PowerShell window:</span></span>

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

<span data-ttu-id="e14ca-110">Riavviare il computer se il Enable-WindowsOptionalFeature segnala `RestartNeeded: True` .</span><span class="sxs-lookup"><span data-stu-id="e14ca-110">Reboot the computer if the Enable-WindowsOptionalFeature reports `RestartNeeded: True`.</span></span>
