---
description: Il programma di installazione imposta la proprietà WindowsVolume sul volume della cartella Windows.
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: Proprietà WindowsVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6220a9844120e061eb680c76a32ce00dbc517f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328750"
---
# <a name="windowsvolume-property"></a><span data-ttu-id="2ff58-103">Proprietà WindowsVolume</span><span class="sxs-lookup"><span data-stu-id="2ff58-103">WindowsVolume property</span></span>

<span data-ttu-id="2ff58-104">Il programma di installazione imposta la proprietà **WindowsVolume** sul volume della cartella Windows.</span><span class="sxs-lookup"><span data-stu-id="2ff58-104">The installer sets the **WindowsVolume** property to the volume of the windows folder.</span></span> <span data-ttu-id="2ff58-105">La proprietà termina sempre con una barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="2ff58-105">The property always ends with a backslash.</span></span> <span data-ttu-id="2ff58-106">Questa operazione può essere utilizzata per impostare il percorso predefinito sul volume in cui si trova la cartella Windows, perché la proprietà [**ROOTDRIVE**](rootdrive.md) non è necessariamente uguale a questa unità.</span><span class="sxs-lookup"><span data-stu-id="2ff58-106">This can be used to set the default location to the volume the Windows folder is on because the [**ROOTDRIVE**](rootdrive.md) property does not necessarily equal this drive.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ff58-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ff58-107">Remarks</span></span>

<span data-ttu-id="2ff58-108">Non utilizzare la proprietà **WindowsVolume** nella colonna directory della tabella [directory](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2ff58-108">Do not use the **WindowsVolume** property in the Directory column of the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="2ff58-109">La proprietà [**WindowsFolder**](windowsfolder.md) contiene il percorso della cartella Windows.</span><span class="sxs-lookup"><span data-stu-id="2ff58-109">The [**WindowsFolder**](windowsfolder.md) property contains the path to the Windows folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff58-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ff58-110">Requirements</span></span>



| <span data-ttu-id="2ff58-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ff58-111">Requirement</span></span> | <span data-ttu-id="2ff58-112">Valore</span><span class="sxs-lookup"><span data-stu-id="2ff58-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff58-113">Versione</span><span class="sxs-lookup"><span data-stu-id="2ff58-113">Version</span></span><br/> | <span data-ttu-id="2ff58-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2ff58-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2ff58-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2ff58-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2ff58-116">Windows Installer in Windows Server 2003 o Windows XP, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack di Windows minimo richiesto da una versione di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2ff58-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ff58-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ff58-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff58-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2ff58-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




