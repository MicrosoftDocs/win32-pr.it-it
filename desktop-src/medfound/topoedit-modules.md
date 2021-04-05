---
description: Moduli TopoEdit
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Moduli TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049799"
---
# <a name="topoedit-modules"></a><span data-ttu-id="10427-103">Moduli TopoEdit</span><span class="sxs-lookup"><span data-stu-id="10427-103">TopoEdit Modules</span></span>

<span data-ttu-id="10427-104">Lo strumento TopoEdit viene fornito con la Windows SDK per Windows Server 2008 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="10427-104">The TopoEdit tool is provided with the Windows SDK for Windows Server 2008 and later.</span></span> <span data-ttu-id="10427-105">Lo strumento richiede Windows Vista o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="10427-105">The tool requires Windows Vista or later.</span></span>

<span data-ttu-id="10427-106">I moduli TopoEdit si trovano nella cartella bin dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="10427-106">The TopoEdit modules are located in the Bin folder of the SDK.</span></span> <span data-ttu-id="10427-107">Questi moduli sono:</span><span class="sxs-lookup"><span data-stu-id="10427-107">These modules are:</span></span>

-   <span data-ttu-id="10427-108">TopoEdit.exe: eseguibile dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="10427-108">TopoEdit.exe—Application executable</span></span>
-   <span data-ttu-id="10427-109">TEDUTIL.dll-DLL di estensione</span><span class="sxs-lookup"><span data-stu-id="10427-109">TEDUTIL.dll—Extension DLL</span></span>

<span data-ttu-id="10427-110">L'installazione dell'SDK registra la DLL.</span><span class="sxs-lookup"><span data-stu-id="10427-110">The SDK installation registers the DLL.</span></span> <span data-ttu-id="10427-111">Tuttavia, in caso di errore, al prompt dei comandi eseguire il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="10427-111">However, if this fails, at a command prompt, run the following.</span></span>


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



<span data-ttu-id="10427-112">Il codice sorgente per TopoEdit viene fornito anche come esempio nell'Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="10427-112">Source code for TopoEdit is also provided as a sample in the Windows SDK.</span></span> <span data-ttu-id="10427-113">Si trova nella directory seguente:</span><span class="sxs-lookup"><span data-stu-id="10427-113">It is located in the following directory:</span></span>

<span data-ttu-id="10427-114"><samples root>\\Multimedia \\ Media Foundation \\ TopoEdit</span><span class="sxs-lookup"><span data-stu-id="10427-114"><samples root>\\Multimedia\\Media Foundation\\TopoEdit</span></span>

## <a name="related-topics"></a><span data-ttu-id="10427-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="10427-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10427-116">Introduzione a TopoEdit</span><span class="sxs-lookup"><span data-stu-id="10427-116">Introduction to TopoEdit</span></span>](introduction-to-topoedit.md)
</dt> <dt>

[<span data-ttu-id="10427-117">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="10427-117">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



