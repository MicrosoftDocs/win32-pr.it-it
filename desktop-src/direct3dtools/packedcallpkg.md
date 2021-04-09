---
description: Rappresenta un pacchetto di quattro chiamate.
MS-HAID: vspixengine.PackedCallPkg
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura PackedCallPkg
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE345C1A-9F6E-4FE0-99C7-6B332A1ED079
api_name:
- PackedCallPkg
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 104e764725213f7030c90a0240641c7c9b063785
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965628"
---
# <a name="span-idvspixenginepackedcallpkgspanpackedcallpkg-structure"></a><span data-ttu-id="0c826-103"><span id="vspixengine.packedcallpkg"></span>Struttura PackedCallPkg</span><span class="sxs-lookup"><span data-stu-id="0c826-103"><span id="vspixengine.packedcallpkg"></span>PackedCallPkg structure</span></span>

<span data-ttu-id="0c826-104">Rappresenta un pacchetto di quattro chiamate.</span><span class="sxs-lookup"><span data-stu-id="0c826-104">Represents a package of four calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c826-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c826-105">Syntax</span></span>


```C++
typedef struct PackedCallPkg {
  UINT pcp1;
  UINT pcp2;
  UINT pcp3;
  UINT pcp4;
} PackedCallPkg;
```

## <a name="members"></a><span data-ttu-id="0c826-106">Members</span><span class="sxs-lookup"><span data-stu-id="0c826-106">Members</span></span>

<span data-ttu-id="0c826-107">**pcp1**</span><span class="sxs-lookup"><span data-stu-id="0c826-107">**pcp1**</span></span>  
<span data-ttu-id="0c826-108">Prima chiamata nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0c826-108">The first call in the package.</span></span>

<span data-ttu-id="0c826-109">**pcp2**</span><span class="sxs-lookup"><span data-stu-id="0c826-109">**pcp2**</span></span>  
<span data-ttu-id="0c826-110">Seconda chiamata nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0c826-110">The second call in the package.</span></span>

<span data-ttu-id="0c826-111">**pcp3**</span><span class="sxs-lookup"><span data-stu-id="0c826-111">**pcp3**</span></span>  
<span data-ttu-id="0c826-112">Terza chiamata nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0c826-112">The third call in the package.</span></span>

<span data-ttu-id="0c826-113">**pcp4**</span><span class="sxs-lookup"><span data-stu-id="0c826-113">**pcp4**</span></span>  
<span data-ttu-id="0c826-114">Quarta chiamata nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0c826-114">The fourth call in the package.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c826-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c826-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0c826-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c826-116">Header</span></span></p></td><td><span data-ttu-id="0c826-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0c826-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



