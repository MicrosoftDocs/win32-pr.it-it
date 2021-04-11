---
description: Uso delle classi di base di DirectShow
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: Uso delle classi di base di DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232287"
---
# <a name="using-the-directshow-base-classes"></a><span data-ttu-id="32a87-103">Uso delle classi di base di DirectShow</span><span class="sxs-lookup"><span data-stu-id="32a87-103">Using the DirectShow Base Classes</span></span>

<span data-ttu-id="32a87-104">Per usare le classi di base in DirectShow, è necessario compilare e collegare la libreria di classi di base.</span><span class="sxs-lookup"><span data-stu-id="32a87-104">To use the base classes in DirectShow, you must build and link the base class library.</span></span>

<span data-ttu-id="32a87-105">La libreria di classi di base viene fornita come esempio SDK in Microsoft Windows Software Development Kit (SDK) ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).</span><span class="sxs-lookup"><span data-stu-id="32a87-105">The base class library is provided as a SDK sample in the Microsoft Windows Software Development Kit (SDK) (<https://go.microsoft.com/fwlink/p/?linkid=62332>).</span></span> <span data-ttu-id="32a87-106">La posizione esatta dipende dalla versione dell'SDK installata, ma dal percorso relativo:</span><span class="sxs-lookup"><span data-stu-id="32a87-106">The exact location depends on the version of the SDK that you have installed, but the relative path is:</span></span>

<span data-ttu-id="32a87-107">*(Radice degli esempi di SDK)* \\ \\BaseClasses DirectShow</span><span class="sxs-lookup"><span data-stu-id="32a87-107">*(SDK samples root)*\\DirectShow\\BaseClasses</span></span>

<span data-ttu-id="32a87-108">Intestazione: Streams. h</span><span class="sxs-lookup"><span data-stu-id="32a87-108">Header: Streams.h</span></span>

<span data-ttu-id="32a87-109">Libreria: nell'esempio vengono compilate le versioni di debug e finale della libreria:</span><span class="sxs-lookup"><span data-stu-id="32a87-109">Library: The sample builds retail and debug versions of the library:</span></span>

-   <span data-ttu-id="32a87-110">Versione definitiva: Strmbase. lib</span><span class="sxs-lookup"><span data-stu-id="32a87-110">Retail version: Strmbase.lib</span></span>
-   <span data-ttu-id="32a87-111">Versione di debug: Strmbasd. lib.</span><span class="sxs-lookup"><span data-stu-id="32a87-111">Debug version: Strmbasd.lib.</span></span>

<span data-ttu-id="32a87-112">Per ulteriori informazioni sulla configurazione dell'ambiente di compilazione, vedere [configurazione dell'ambiente di compilazione](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="32a87-112">For more information on setting up your build environment, see [Setting Up the Build Environment](setting-up-the-build-environment.md).</span></span>

## <a name="preprocessor-symbols"></a><span data-ttu-id="32a87-113">Simboli del preprocessore</span><span class="sxs-lookup"><span data-stu-id="32a87-113">Preprocessor Symbols</span></span>

<span data-ttu-id="32a87-114">Quando si include il file di intestazione Streams. h, i simboli del preprocessore seguenti hanno un significato speciale:</span><span class="sxs-lookup"><span data-stu-id="32a87-114">When you include the header file Streams.h, the following preprocessor symbols have special meaning:</span></span>

-   <span data-ttu-id="32a87-115">PRESTAZIONI: riservato.</span><span class="sxs-lookup"><span data-stu-id="32a87-115">PERF: Reserved.</span></span> <span data-ttu-id="32a87-116">Non usare questo simbolo del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="32a87-116">Do not use this preprocessor symbol.</span></span>
-   <span data-ttu-id="32a87-117">VFWROBUST: Abilita la convalida del puntatore nella versione finale.</span><span class="sxs-lookup"><span data-stu-id="32a87-117">VFWROBUST: Enables pointer validation in retail.</span></span> <span data-ttu-id="32a87-118">Per altre informazioni, vedere [macro Validation Pointer](pointer-validation-macros.md).</span><span class="sxs-lookup"><span data-stu-id="32a87-118">For more information, see [Pointer Validation Macros](pointer-validation-macros.md).</span></span> <span data-ttu-id="32a87-119">Nelle build di debug non è necessario definire VFWROBUST.</span><span class="sxs-lookup"><span data-stu-id="32a87-119">In debug builds, it is not necessary to define VFWROBUST.</span></span>

> [!Note]  
> <span data-ttu-id="32a87-120">In Windows Vista e versioni successive, le macro di convalida del puntatore sono vuote.</span><span class="sxs-lookup"><span data-stu-id="32a87-120">In Windows Vista and later, the pointer validation macros are empty.</span></span>

 

 

 



