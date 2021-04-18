---
title: LIBMAIN. CPP
description: Nel componente provider di esempio, un esempio di codice del punto di ingresso della DLL standard per Adssmp.dll è in LibMain. cpp. Le routine supportate sono elencate nella tabella seguente.
ms.assetid: aa05fbd1-509d-4ed6-8a49-1ce11ce54c0e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e309d3c6454901b26f5ab67351033b39d73dd7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297668"
---
# <a name="libmaincpp"></a><span data-ttu-id="411a0-104">LIBMAIN. CPP</span><span class="sxs-lookup"><span data-stu-id="411a0-104">LIBMAIN.CPP</span></span>

<span data-ttu-id="411a0-105">Nel componente provider di esempio, un esempio di codice del punto di ingresso della DLL standard per Adssmp.dll è in LibMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="411a0-105">In the example provider component, a code example of the standard DLL entry point for Adssmp.dll is in Libmain.cpp.</span></span> <span data-ttu-id="411a0-106">Le routine supportate sono elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="411a0-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="411a0-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="411a0-107">Item</span></span>                                  | <span data-ttu-id="411a0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="411a0-108">Description</span></span>                                                              |
|---------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="411a0-109">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="411a0-109">**DllGetClassObject**</span></span><br/>      | <span data-ttu-id="411a0-110">Punto di ingresso della DLL standard per individuare le class factory.</span><span class="sxs-lookup"><span data-stu-id="411a0-110">Standard DLL entry point for locating class factories.</span></span><br/>        |
| <span data-ttu-id="411a0-111">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="411a0-111">**DllCanUnloadNow**</span></span><br/>        | <span data-ttu-id="411a0-112">Punto di ingresso DLL standard per determinare se la DLL può essere scaricata.</span><span class="sxs-lookup"><span data-stu-id="411a0-112">Standard DLL entry point to determine if DLL can be unloaded.</span></span><br/> |
| <span data-ttu-id="411a0-113">**LibMain**</span><span class="sxs-lookup"><span data-stu-id="411a0-113">**LibMain**</span></span><br/>                | <span data-ttu-id="411a0-114">Punto di ingresso di inizializzazione DLL standard.</span><span class="sxs-lookup"><span data-stu-id="411a0-114">Standard DLL initialization entry point.</span></span><br/>                      |
| <span data-ttu-id="411a0-115">**IsCompatibleOleVersion**</span><span class="sxs-lookup"><span data-stu-id="411a0-115">**IsCompatibleOleVersion**</span></span><br/> | <span data-ttu-id="411a0-116">Verificare la compatibilità con la fase di esecuzione OLE.</span><span class="sxs-lookup"><span data-stu-id="411a0-116">Verify compatibility with the OLE run time.</span></span><br/>                   |
| <span data-ttu-id="411a0-117">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="411a0-117">**DllMain**</span></span><br/>                | <span data-ttu-id="411a0-118">Punto di ingresso per la maggior parte delle versioni di Windows 2000 o Windows NT.</span><span class="sxs-lookup"><span data-stu-id="411a0-118">Entry point for most Windows 2000 or Windows NT versions.</span></span><br/>     |



 

 

 





