---
description: È possibile utilizzare il Evalcom2.dll per implementare le operazioni di convalida per i pacchetti di installazione e i moduli unione.
ms.assetid: c587a689-0c7e-4862-8567-2cdbc803b92c
title: Automazione della convalida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230e5676fcfabcafa6010a18e300a2d5701ae5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308170"
---
# <a name="validation-automation"></a><span data-ttu-id="03c2a-103">Automazione della convalida</span><span class="sxs-lookup"><span data-stu-id="03c2a-103">Validation Automation</span></span>

<span data-ttu-id="03c2a-104">È possibile utilizzare il Evalcom2.dll per implementare le operazioni di convalida per i pacchetti di installazione e i moduli unione.</span><span class="sxs-lookup"><span data-stu-id="03c2a-104">You can use the Evalcom2.dll to implement validation operations for installation packages and merge modules.</span></span>

<span data-ttu-id="03c2a-105">Le sezioni seguenti di questa documentazione contengono informazioni sull'utilizzo della convalida Windows Installer dall'interno degli strumenti di creazione:</span><span class="sxs-lookup"><span data-stu-id="03c2a-105">The following sections of this documentation contain information about using Windows Installer validation from within authoring tools:</span></span>

-   [<span data-ttu-id="03c2a-106">Uso di Evalcom2</span><span class="sxs-lookup"><span data-stu-id="03c2a-106">Using Evalcom2</span></span>](using-evalcom2.md)
-   [<span data-ttu-id="03c2a-107">Interfacce EvalCom2</span><span class="sxs-lookup"><span data-stu-id="03c2a-107">EvalCom2 Interfaces</span></span>](evalcom2-interfaces.md)

<span data-ttu-id="03c2a-108">Si consiglia di installare Evalcom2.dll utilizzando il Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="03c2a-108">It is recommended that Evalcom2.dll be installed using the Windows Installer.</span></span> <span data-ttu-id="03c2a-109">Il pacchetto di Orca.msi fornito con Microsoft Windows Software Development Kit (SDK) per Windows XP con Service Pack 2 (SP2) o versioni successive installa Evalcom2.dll.</span><span class="sxs-lookup"><span data-stu-id="03c2a-109">The Orca.msi package provided with the Microsoft Windows Software Development Kit (SDK) for Windows XP with Service Pack 2 (SP2) or greater installs Evalcom2.dll.</span></span> <span data-ttu-id="03c2a-110">L'ID componente per il componente che contiene l'interfaccia COM è {53315473-B8D6-470A-9951-D9AE5C11FC91}.</span><span class="sxs-lookup"><span data-stu-id="03c2a-110">The component ID for the component that contains the COM interface is {53315473-B8D6-470A-9951-D9AE5C11FC91}.</span></span>

<span data-ttu-id="03c2a-111">Per informazioni su come ottenere la Windows SDK, vedere [Windows SDK componenti per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="03c2a-111">For information about obtaining the Windows SDK, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

 

 



