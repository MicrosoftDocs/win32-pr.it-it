---
description: Rappresenta le informazioni su una singola voce nel layout del buffer di una mesh.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura MeshDataBufferLayoutEntry
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bce67b8316e9eb9b96e641e2a90260fab6bfdaad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747575"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span data-ttu-id="e0c32-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>Struttura MeshDataBufferLayoutEntry</span><span class="sxs-lookup"><span data-stu-id="e0c32-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>MeshDataBufferLayoutEntry structure</span></span>

<span data-ttu-id="e0c32-104">Rappresenta le informazioni su una singola voce nel layout del buffer di una mesh.</span><span class="sxs-lookup"><span data-stu-id="e0c32-104">Represents information about a single entry in the buffer layout of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0c32-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0c32-105">Syntax</span></span>


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a><span data-ttu-id="e0c32-106">Members</span><span class="sxs-lookup"><span data-stu-id="e0c32-106">Members</span></span>

<span data-ttu-id="e0c32-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="e0c32-107">**pName**</span></span>  
<span data-ttu-id="e0c32-108">Stringa COM contenente il nome della voce.</span><span class="sxs-lookup"><span data-stu-id="e0c32-108">A COM string containing the name of the entry.</span></span>

<span data-ttu-id="e0c32-109">**numComponents**</span><span class="sxs-lookup"><span data-stu-id="e0c32-109">**numComponents**</span></span>  
<span data-ttu-id="e0c32-110">Numero di componenti omogenei (valori) che costituiscono questa voce.</span><span class="sxs-lookup"><span data-stu-id="e0c32-110">The number of homogenous components (values) that make up this entry.</span></span>

<span data-ttu-id="e0c32-111">**Posizione**</span><span class="sxs-lookup"><span data-stu-id="e0c32-111">**isPosition**</span></span>  
<span data-ttu-id="e0c32-112">true se la voce è una posizione; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="e0c32-112">true if the entry is a position; otherwise, false.</span></span>

<span data-ttu-id="e0c32-113">**format**</span><span class="sxs-lookup"><span data-stu-id="e0c32-113">**format**</span></span>  
<span data-ttu-id="e0c32-114">Formato dati della voce (Register).</span><span class="sxs-lookup"><span data-stu-id="e0c32-114">The data format of the entry (register).</span></span> <span data-ttu-id="e0c32-115">Per ulteriori informazioni, vedere l' \_ enumerazione del formato Register.</span><span class="sxs-lookup"><span data-stu-id="e0c32-115">For more information, see the REGISTER\_FORMAT enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c32-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0c32-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e0c32-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0c32-117">Header</span></span></p></td><td><span data-ttu-id="e0c32-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e0c32-118">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



