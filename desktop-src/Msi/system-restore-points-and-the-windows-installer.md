---
description: Ripristino configurazione di sistema monitora e registra automaticamente le modifiche di sistema principali nel computer di un utente. Per ulteriori informazioni, vedere Ripristino configurazione di sistema.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Punti di ripristino del sistema e Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fe9bd4b8e22f5aee7e49d3e4c452378f402e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308671"
---
# <a name="system-restore-points-and-the-windows-installer"></a><span data-ttu-id="fbb3a-104">Punti di ripristino del sistema e Windows Installer</span><span class="sxs-lookup"><span data-stu-id="fbb3a-104">System Restore Points and the Windows Installer</span></span>

<span data-ttu-id="fbb3a-105">Ripristino configurazione di sistema monitora e registra automaticamente le modifiche di sistema principali nel computer di un utente.</span><span class="sxs-lookup"><span data-stu-id="fbb3a-105">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="fbb3a-106">Per ulteriori informazioni, vedere [Ripristino configurazione di sistema](../sr/system-restore-portal.md).</span><span class="sxs-lookup"><span data-stu-id="fbb3a-106">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="fbb3a-107">I punti di ripristino del sistema vengono creati dal sistema e vengono creati anche da Windows Installer quando il software viene installato o rimosso.</span><span class="sxs-lookup"><span data-stu-id="fbb3a-107">System restore points are created by the system and are also created by Windows Installer when software is installed or removed.</span></span>

<span data-ttu-id="fbb3a-108">In Windows XP il programma di installazione può creare checkpoint durante la prima installazione di un'applicazione e durante la relativa rimozione.</span><span class="sxs-lookup"><span data-stu-id="fbb3a-108">On Windows XP, the installer may create checkpoints during the first installation of an application, and during its removal.</span></span> <span data-ttu-id="fbb3a-109">In questi casi, il programma di installazione crea solo checkpoint quando la modifica viene eseguita con almeno un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fbb3a-109">The installer only creates checkpoints in these cases when the change is run with at least a [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="fbb3a-110">Le installazioni con il [livello di interfaccia utente](user-interface-levels.md) impostato su None vengono in genere avviate dal sistema o da un'applicazione che deve gestire la creazione di un checkpoint.</span><span class="sxs-lookup"><span data-stu-id="fbb3a-110">Installations having the [user interface level](user-interface-levels.md) set to None are usually initiated by the system or an application that should handle creating a checkpoint.</span></span> <span data-ttu-id="fbb3a-111">Per ulteriori informazioni, vedere [Ripristino configurazione di sistema](../sr/system-restore-portal.md).</span><span class="sxs-lookup"><span data-stu-id="fbb3a-111">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="fbb3a-112">Nelle aziende con molte piccole applicazioni, gli amministratori possono decidere di disabilitare il checkpoint dall'interno del programma di installazione per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="fbb3a-112">In corporations with many small applications, administrators may decide to disable checkpointing from within the installer to improve performance.</span></span> <span data-ttu-id="fbb3a-113">Per altre informazioni, vedere [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) o [impostazione di un punto di ripristino da un'azione personalizzata](setting-a-restore-point-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="fbb3a-113">For more information, see [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) or [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

<span data-ttu-id="fbb3a-114">A partire da Windows Installer 5,0, la proprietà [**MSIFASTINSTALL**](msifastinstall.md) può essere impostata in modo da impedire che un'installazione generi un punto di ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="fbb3a-114">Beginning with Windows Installer 5.0, the [**MSIFASTINSTALL**](msifastinstall.md) property can be set to prevent an installation from generating a system restore point.</span></span>

 

 
