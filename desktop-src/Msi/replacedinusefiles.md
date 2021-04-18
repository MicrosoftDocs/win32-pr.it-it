---
description: La proprietà ReplacedInUseFiles viene impostata se il programma di installazione scrive su un file che viene mantenuto in uso.
ms.assetid: cef7d36e-c721-4d47-beaa-53e6749334b6
title: Proprietà ReplacedInUseFiles
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d6826f1db2ec1844234cf32f1137e43c89528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330608"
---
# <a name="replacedinusefiles-property"></a><span data-ttu-id="9b64e-103">Proprietà ReplacedInUseFiles</span><span class="sxs-lookup"><span data-stu-id="9b64e-103">ReplacedInUseFiles property</span></span>

<span data-ttu-id="9b64e-104">La proprietà **ReplacedInUseFiles** viene impostata se il programma di installazione scrive su un file che viene mantenuto in uso.</span><span class="sxs-lookup"><span data-stu-id="9b64e-104">The **ReplacedInUseFiles** property is set if the installer writes over a file that is being held in use.</span></span> <span data-ttu-id="9b64e-105">Questa proprietà viene utilizzata dalle azioni personalizzate per rilevare che è necessario riavviare il computer per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9b64e-105">This property is used by custom actions to detect that a reboot is required to complete the installation.</span></span>

<span data-ttu-id="9b64e-106">Impostato durante le azioni [InstallExecute](installexecute-action.md) e [InstallFinalize](installfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="9b64e-106">Set during the [InstallExecute](installexecute-action.md) and [InstallFinalize](installfinalize-action.md) actions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b64e-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b64e-107">Requirements</span></span>



| <span data-ttu-id="9b64e-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b64e-108">Requirement</span></span> | <span data-ttu-id="9b64e-109">Valore</span><span class="sxs-lookup"><span data-stu-id="9b64e-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b64e-110">Versione</span><span class="sxs-lookup"><span data-stu-id="9b64e-110">Version</span></span><br/> | <span data-ttu-id="9b64e-111">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9b64e-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9b64e-112">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9b64e-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9b64e-113">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9b64e-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9b64e-114">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9b64e-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9b64e-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b64e-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b64e-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9b64e-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




