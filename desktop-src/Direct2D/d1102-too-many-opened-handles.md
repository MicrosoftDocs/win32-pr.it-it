---
title: D1102 troppi handle aperti
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: È stato trovato un numero elevato di interfacce non rilasciate. Attualmente sono presenti interfacce non rilasciate allocate da questa DLL.
keywords:
- D1102 troppi handle aperti Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e3c12c2e2a7b47535e830c6ed65a828a16672bbf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718052"
---
# <a name="d1102-too-many-opened-handles"></a><span data-ttu-id="38ae2-105">D1102: troppi handle aperti</span><span class="sxs-lookup"><span data-stu-id="38ae2-105">D1102: Too Many Opened Handles</span></span>

<span data-ttu-id="38ae2-106">È stato trovato un numero elevato di interfacce non rilasciate.</span><span class="sxs-lookup"><span data-stu-id="38ae2-106">A large number of unreleased interfaces were found.</span></span> <span data-ttu-id="38ae2-107">Attualmente sono presenti \[ *numero* \] di interfacce non rilasciate allocate da questa dll.</span><span class="sxs-lookup"><span data-stu-id="38ae2-107">Currently there are \[*number*\] unreleased interfaces allocated by this DLL.</span></span>

## <a name="placeholders"></a><span data-ttu-id="38ae2-108">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="38ae2-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="38ae2-109"><span id="number"></span><span id="NUMBER"></span>*numero*</span><span class="sxs-lookup"><span data-stu-id="38ae2-109"><span id="number"></span><span id="NUMBER"></span>*number*</span></span>
</dt> <dd>

<span data-ttu-id="38ae2-110">Numero di interfacce non rilasciate allocate da questa DLL.</span><span class="sxs-lookup"><span data-stu-id="38ae2-110">The number of unreleased interfaces allocated by this DLL.</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="38ae2-111">Livello di errore</span><span class="sxs-lookup"><span data-stu-id="38ae2-111">Error Level</span></span> | <span data-ttu-id="38ae2-112">Avviso</span><span class="sxs-lookup"><span data-stu-id="38ae2-112">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="38ae2-113">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="38ae2-113">Possible Causes</span></span>

<span data-ttu-id="38ae2-114">È stato creato un numero elevato di risorse.</span><span class="sxs-lookup"><span data-stu-id="38ae2-114">A large number of resources were created.</span></span> <span data-ttu-id="38ae2-115">Sebbene Direct2D non abbia un limite superiore per il numero di risorse disponibili (ad eccezione della memoria), il livello di debug emette questo messaggio informativo quando rileva 1001 oggetti attivi, 2001 oggetti attivi o 3001 oggetti attivi, perché questo potrebbe indicare una perdita nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38ae2-115">Although Direct2D has no upper bound on the number of available resources (except memory), the debug layer issues this informational message when it encounters 1001 live objects, 2001 live objects, or 3001 live objects etc, because this might indicate a leak in the application.</span></span>

 

 




