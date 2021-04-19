---
description: Rappresenta i campi del layout di input di un buffer di vertice, uno per ogni campo nel buffer del vertice.
MS-HAID: vspixengine.InputLayoutStruct
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura InputLayoutStruct
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC7AAC2F-FDB1-4AD8-9B87-A97EE557FEAC
api_name:
- InputLayoutStruct
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1369d80d202682b67eacbb184b215d9da1711874
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303906"
---
# <a name="span-idvspixengineinputlayoutstructspaninputlayoutstruct-structure"></a><span data-ttu-id="0cb75-103"><span id="vspixengine.inputlayoutstruct"></span>Struttura InputLayoutStruct</span><span class="sxs-lookup"><span data-stu-id="0cb75-103"><span id="vspixengine.inputlayoutstruct"></span>InputLayoutStruct structure</span></span>

<span data-ttu-id="0cb75-104">Rappresenta i campi del layout di input di un buffer di vertice, uno per ogni campo nel buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="0cb75-104">Represents the input layout fields of a vertex buffer, one per field in the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb75-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cb75-105">Syntax</span></span>


```C++
} InputLayoutStruct;
```

## <a name="members"></a><span data-ttu-id="0cb75-106">Members</span><span class="sxs-lookup"><span data-stu-id="0cb75-106">Members</span></span>

<span data-ttu-id="0cb75-107">**Semanticname**</span><span class="sxs-lookup"><span data-stu-id="0cb75-107">**SemanticName**</span></span>  
<span data-ttu-id="0cb75-108">Stringa COM contenente il nome della semantica associata.</span><span class="sxs-lookup"><span data-stu-id="0cb75-108">A COM string containing the name of the associated semantic.</span></span>

<span data-ttu-id="0cb75-109">**SemanticIndex**</span><span class="sxs-lookup"><span data-stu-id="0cb75-109">**SemanticIndex**</span></span>  
<span data-ttu-id="0cb75-110">Indice della semantica associata.</span><span class="sxs-lookup"><span data-stu-id="0cb75-110">The index of the associated semantic.</span></span>

<span data-ttu-id="0cb75-111">**Formato**</span><span class="sxs-lookup"><span data-stu-id="0cb75-111">**Format**</span></span>  
<span data-ttu-id="0cb75-112">Formato del campo.</span><span class="sxs-lookup"><span data-stu-id="0cb75-112">The format of the field.</span></span> <span data-ttu-id="0cb75-113">Per ulteriori informazioni, vedere l' \_ enumerazione del formato dxgi.</span><span class="sxs-lookup"><span data-stu-id="0cb75-113">For more information see the DXGI\_FORMAT enumeration.</span></span>

<span data-ttu-id="0cb75-114">**InputSlot**</span><span class="sxs-lookup"><span data-stu-id="0cb75-114">**InputSlot**</span></span>  
<span data-ttu-id="0cb75-115">Slot di input associato.</span><span class="sxs-lookup"><span data-stu-id="0cb75-115">The associated input slot.</span></span>

<span data-ttu-id="0cb75-116">**AlignedByteOffset**</span><span class="sxs-lookup"><span data-stu-id="0cb75-116">**AlignedByteOffset**</span></span>  

<span data-ttu-id="0cb75-117">**InputSlotClass**</span><span class="sxs-lookup"><span data-stu-id="0cb75-117">**InputSlotClass**</span></span>  

<span data-ttu-id="0cb75-118">**InstanceDataStepRate**</span><span class="sxs-lookup"><span data-stu-id="0cb75-118">**InstanceDataStepRate**</span></span>  

## <a name="requirements"></a><span data-ttu-id="0cb75-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cb75-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0cb75-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0cb75-120">Header</span></span></p></td><td><span data-ttu-id="0cb75-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0cb75-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



