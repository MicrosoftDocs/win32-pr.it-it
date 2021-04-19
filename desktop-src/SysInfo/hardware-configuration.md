---
description: Le funzioni di configurazione hardware recuperano informazioni quali processore, profilo hardware e informazioni sulla tastiera.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Configurazione hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee4abe543f0603ab6cf80ef395fe56e4e3300c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317660"
---
# <a name="hardware-configuration"></a><span data-ttu-id="1f7db-103">Configurazione hardware</span><span class="sxs-lookup"><span data-stu-id="1f7db-103">Hardware Configuration</span></span>

<span data-ttu-id="1f7db-104">Le funzioni di configurazione hardware recuperano informazioni quali processore, profilo hardware e informazioni sulla tastiera.</span><span class="sxs-lookup"><span data-stu-id="1f7db-104">The hardware configuration functions retrieve information such as processor, hardware profile, and keyboard information.</span></span>

<span data-ttu-id="1f7db-105">La funzione [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) recupera le informazioni sul processore e sulla memoria, ad esempio le dimensioni della pagina, l'identificatore OEM (Original Equipment Manufacturer), il numero e il tipo di processori, l'intervallo di indirizzi delle applicazioni e così via.</span><span class="sxs-lookup"><span data-stu-id="1f7db-105">The [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function retrieves processor and memory information, such as the page size, original equipment manufacturer (OEM) identifier, number and type of processors, application address range, and so on.</span></span> <span data-ttu-id="1f7db-106">La funzione [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) recupera informazioni sulle operazioni a virgola mobile e sui set di istruzioni supportati dal processore.</span><span class="sxs-lookup"><span data-stu-id="1f7db-106">The [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) function retrieves information about the floating-point operations and instruction sets supported by the processor.</span></span>

<span data-ttu-id="1f7db-107">La funzione [**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) recupera le informazioni sul profilo hardware.</span><span class="sxs-lookup"><span data-stu-id="1f7db-107">The [**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) function retrieves information about the hardware profile.</span></span> <span data-ttu-id="1f7db-108">Il profilo hardware include informazioni quali lo stato di ancoraggio, l'identificatore univoco globale (GUID) e il nome visualizzato per il profilo.</span><span class="sxs-lookup"><span data-stu-id="1f7db-108">The hardware profile includes information such as the docking state, globally unique identifier (GUID), and display name for the profile.</span></span> <span data-ttu-id="1f7db-109">La funzione [**GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) recupera informazioni come il tipo di tastiera e il numero di tasti funzione sulla tastiera corrente.</span><span class="sxs-lookup"><span data-stu-id="1f7db-109">The [**GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) function retrieves such information as the type of keyboard and the number of function keys on the current keyboard.</span></span>

 

 
