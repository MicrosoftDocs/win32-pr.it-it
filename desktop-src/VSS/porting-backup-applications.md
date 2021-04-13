---
description: I file binari di Windows Server 2003 con Service Pack 1 (SP1) sono compatibili con Windows Vista e Windows Server 2008. È tuttavia necessario ricompilare i file binari di versioni precedenti di Windows.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Porting di applicazioni di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528710"
---
# <a name="porting-backup-applications"></a><span data-ttu-id="89a14-104">Porting di applicazioni di backup</span><span class="sxs-lookup"><span data-stu-id="89a14-104">Porting Backup Applications</span></span>

<span data-ttu-id="89a14-105">I file binari di Windows Server 2003 con Service Pack 1 (SP1) sono compatibili con Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="89a14-105">Binaries from Windows Server 2003 with Service Pack 1 (SP1) are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="89a14-106">È tuttavia necessario ricompilare i file binari di versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="89a14-106">However, binaries from earlier versions of Windows must be recompiled.</span></span>

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a><span data-ttu-id="89a14-107">Porting di applicazioni di backup Windows XP a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89a14-107">Porting Windows XP Backup Applications to Windows Vista</span></span>

<span data-ttu-id="89a14-108">Diverse interfacce VSS sono state modificate rispetto a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="89a14-108">Several VSS interfaces have changed since Windows XP.</span></span> <span data-ttu-id="89a14-109">Come minimo, le applicazioni Windows XP devono essere ricompilate utilizzando i file di intestazione e le librerie di VSS 7,2 SDK o Windows Vista o Windows Server 2008 SDK.</span><span class="sxs-lookup"><span data-stu-id="89a14-109">At a minimum, Windows XP applications must be recompiled using header files and libraries from the VSS 7.2 SDK or the Windows Vista or Windows Server 2008 SDK.</span></span>

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a><span data-ttu-id="89a14-110">Porting di applicazioni di backup di Windows Server 2003 SP1 a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89a14-110">Porting Windows Server 2003 SP1 Backup Applications to Windows Vista</span></span>

<span data-ttu-id="89a14-111">I file binari di Windows Server 2003 con SP1 sono compatibili con Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="89a14-111">Binaries from Windows Server 2003 with SP1 are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="89a14-112">Tuttavia, la maggior parte delle applicazioni di backup di Windows Server 2003 con SP1 deve essere aggiornata per tenere conto di nuove funzionalità, descritte nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="89a14-112">However, most Windows Server 2003 with SP1 backup applications must be updated to account for new features, which are described in the following sections.</span></span>

## <a name="compiling-backup-applications-for-windows-vista"></a><span data-ttu-id="89a14-113">Compilazione di applicazioni di backup per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89a14-113">Compiling Backup Applications for Windows Vista</span></span>

<span data-ttu-id="89a14-114">Le applicazioni che usano le interfacce disponibili in Windows Server 2003 possono essere compilate usando i file di intestazione e le librerie fornite in VSS 7,2 SDK.</span><span class="sxs-lookup"><span data-stu-id="89a14-114">Applications that use interfaces available in Windows Server 2003 can be compiled using header files and libraries provided in the VSS 7.2 SDK.</span></span> <span data-ttu-id="89a14-115">Per utilizzare le nuove interfacce, è necessario ricompilare le applicazioni utilizzando i file di intestazione e le librerie incluse in Windows Vista SDK.</span><span class="sxs-lookup"><span data-stu-id="89a14-115">To use new interfaces, applications must be recompiled using the header files and libraries included in the Windows Vista SDK.</span></span>

> [!Note]  
> <span data-ttu-id="89a14-116">I file binari compilati con Windows Vista o Windows Server 2008 non sono compatibili con Windows Server 2003 con SP1 o versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="89a14-116">Binaries compiled using Windows Vista or Windows Server 2008 are not compatible with Windows Server 2003 with SP1 or earlier versions of Windows.</span></span>

 

 

 



