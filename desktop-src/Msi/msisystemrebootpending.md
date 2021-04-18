---
description: Il programma di installazione imposta il valore della proprietà MsiSystemRebootPending su 1 se è presente un'operazione in sospeso per rinominare un file.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Proprietà MsiSystemRebootPending
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330484"
---
# <a name="msisystemrebootpending-property"></a><span data-ttu-id="b84cf-103">Proprietà MsiSystemRebootPending</span><span class="sxs-lookup"><span data-stu-id="b84cf-103">MsiSystemRebootPending property</span></span>

<span data-ttu-id="b84cf-104">Il programma di installazione imposta il valore della proprietà **MsiSystemRebootPending** su 1 se è presente un'operazione in sospeso per rinominare un file.</span><span class="sxs-lookup"><span data-stu-id="b84cf-104">The installer sets the value of the **MsiSystemRebootPending** property to 1 if there is an operation pending to rename a file.</span></span>

<span data-ttu-id="b84cf-105">Gli autori di pacchetti possono basare una condizione nella [tabella LaunchCondition](launchcondition-table.md) in questa proprietà per impedire l'installazione del pacchetto nei casi in cui è presente un'operazione in sospeso per rinominare un file.</span><span class="sxs-lookup"><span data-stu-id="b84cf-105">Package authors can base a condition in the [LaunchCondition table](launchcondition-table.md) on this property to prevent the installation of their package in cases where there is an operation pending to rename a file.</span></span> <span data-ttu-id="b84cf-106">Questa operazione può essere eseguita per impedire il riavvio del sistema operativo causato dalla ridenominazione del file.</span><span class="sxs-lookup"><span data-stu-id="b84cf-106">This may be done to prevent a restart of the operating system caused by the renaming of the file.</span></span> <span data-ttu-id="b84cf-107">Il programma di installazione non imposta la proprietà **MsiSystemRebootPending** in tutti i casi che richiedono il riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="b84cf-107">The installer does not set the **MsiSystemRebootPending** property in all cases that require a restart of the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="b84cf-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b84cf-108">Requirements</span></span>



| <span data-ttu-id="b84cf-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="b84cf-109">Requirement</span></span> | <span data-ttu-id="b84cf-110">Valore</span><span class="sxs-lookup"><span data-stu-id="b84cf-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b84cf-111">Versione</span><span class="sxs-lookup"><span data-stu-id="b84cf-111">Version</span></span><br/> | <span data-ttu-id="b84cf-112">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b84cf-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b84cf-113">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b84cf-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b84cf-114">Windows Installer 4,5 in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b84cf-114">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b84cf-115">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b84cf-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b84cf-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b84cf-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b84cf-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b84cf-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="b84cf-118">Riavvio del sistema</span><span class="sxs-lookup"><span data-stu-id="b84cf-118">System Reboots</span></span>](system-reboots.md)
</dt> <dt>

[<span data-ttu-id="b84cf-119">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="b84cf-119">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




