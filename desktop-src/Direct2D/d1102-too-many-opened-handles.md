---
title: D1102 Troppi handle aperti
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: È stato trovato un numero elevato di interfacce non riasseedate. Attualmente sono presenti interfacce non assegnate allocate da questa DLL.
keywords:
- D1102 Troppi handle aperti Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2d59e110aece56a31af71e75e9a8eca0bb008961
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548686"
---
# <a name="d1102-too-many-opened-handles"></a><span data-ttu-id="aaa9a-105">D1102: Troppi handle aperti</span><span class="sxs-lookup"><span data-stu-id="aaa9a-105">D1102: Too Many Opened Handles</span></span>

<span data-ttu-id="aaa9a-106">È stato trovato un numero elevato di interfacce non riasseedate.</span><span class="sxs-lookup"><span data-stu-id="aaa9a-106">A large number of unreleased interfaces were found.</span></span> <span data-ttu-id="aaa9a-107">Attualmente questa DLL allocare un numero di interfacce \[  \] non ritirate.</span><span class="sxs-lookup"><span data-stu-id="aaa9a-107">Currently there are \[*number*\] unreleased interfaces allocated by this DLL.</span></span>

## <a name="placeholders"></a><span data-ttu-id="aaa9a-108">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="aaa9a-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="aaa9a-109"><span id="number"></span><span id="NUMBER"></span>*Numero*</span><span class="sxs-lookup"><span data-stu-id="aaa9a-109"><span id="number"></span><span id="NUMBER"></span>*number*</span></span>
</dt> <dd>

<span data-ttu-id="aaa9a-110">Numero di interfacce non assegnate allocate da questa DLL.</span><span class="sxs-lookup"><span data-stu-id="aaa9a-110">The number of unreleased interfaces allocated by this DLL.</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="aaa9a-111">Livello di errore</span><span class="sxs-lookup"><span data-stu-id="aaa9a-111">Error Level</span></span> | <span data-ttu-id="aaa9a-112">Avviso</span><span class="sxs-lookup"><span data-stu-id="aaa9a-112">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="aaa9a-113">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="aaa9a-113">Possible Causes</span></span>

<span data-ttu-id="aaa9a-114">È stato creato un numero elevato di risorse.</span><span class="sxs-lookup"><span data-stu-id="aaa9a-114">A large number of resources were created.</span></span> <span data-ttu-id="aaa9a-115">Anche se Direct2D non ha limiti superiori per il numero di risorse disponibili (ad eccezione della memoria), il livello di debug genererà questo messaggio informativo quando rileva 1001 oggetti live, 2001 oggetti live o 3001 oggetti live e così via, perché ciò potrebbe indicare una perdita nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="aaa9a-115">Although Direct2D has no upper bound on the number of available resources (except memory), the debug layer issues this informational message when it encounters 1001 live objects, 2001 live objects, or 3001 live objects etc, because this might indicate a leak in the application.</span></span>

 

 




