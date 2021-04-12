---
description: Quando si installa un assembly in un percorso isolato per un'applicazione specifica, è necessario specificare l'applicazione nella \_ colonna file Application della tabella MsiAssembly.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Installazione e rimozione di assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44dee05940ab3c05e97a7145f9b2363226bb07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234043"
---
# <a name="installing-and-removing-assemblies"></a><span data-ttu-id="df1b1-103">Installazione e rimozione di assembly</span><span class="sxs-lookup"><span data-stu-id="df1b1-103">Installing and Removing Assemblies</span></span>

<span data-ttu-id="df1b1-104">Quando si installa un assembly in un percorso isolato per un'applicazione specifica, è necessario specificare l'applicazione nella \_ colonna file Application della [tabella MsiAssembly](msiassembly-table.md).</span><span class="sxs-lookup"><span data-stu-id="df1b1-104">When installing an assembly to an isolated location for a specific application, the application must be specified in the File\_Application column of the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="df1b1-105">Questo campo è una chiave nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="df1b1-105">This field is a key into the [File table](file-table.md).</span></span> <span data-ttu-id="df1b1-106">Il programma di installazione utilizza la struttura di directory specificata nella [tabella di directory](directory-table.md) per installare l'assembly nella stessa directory del componente che contiene il file.</span><span class="sxs-lookup"><span data-stu-id="df1b1-106">The installer uses the directory structure that is specified in the [Directory table](directory-table.md) to install the assembly into the same directory as the component that contains this file.</span></span>

<span data-ttu-id="df1b1-107">Quando si installa un assembly nella Global Assembly Cache, il valore nella \_ colonna applicazione file della [tabella MsiAssembly](msiassembly-table.md) deve essere null.</span><span class="sxs-lookup"><span data-stu-id="df1b1-107">When installing an assembly to the global assembly cache, the value in the File\_Application column of the [MsiAssembly Table](msiassembly-table.md) must be Null.</span></span>

<span data-ttu-id="df1b1-108">Le sezioni seguenti descrivono l'installazione di assembly Win32 e Common Language Runtime:</span><span class="sxs-lookup"><span data-stu-id="df1b1-108">The following sections describe the installation of Win32 and common language runtime assemblies:</span></span>

-   [<span data-ttu-id="df1b1-109">Installazione degli assembly Win32</span><span class="sxs-lookup"><span data-stu-id="df1b1-109">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)
-   [<span data-ttu-id="df1b1-110">Installazione degli assembly di Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="df1b1-110">Installation of Common Language Runtime Assemblies</span></span>](installation-of-common-language-runtime-assemblies.md)

 

 



