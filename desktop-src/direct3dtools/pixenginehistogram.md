---
description: Rappresenta un istogramma di una trama.
MS-HAID: vspixengine.PixEngineHistogram
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura PixEngineHistogram
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FC720568-6C8E-4B14-BCB1-5FA14D32C785
api_name:
- PixEngineHistogram
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c19b77c962121949cc2495170061fee3adcecfc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124683"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span data-ttu-id="cdc97-103"><span id="vspixengine.pixenginehistogram"></span>Struttura PixEngineHistogram</span><span class="sxs-lookup"><span data-stu-id="cdc97-103"><span id="vspixengine.pixenginehistogram"></span>PixEngineHistogram structure</span></span>

<span data-ttu-id="cdc97-104">Rappresenta un istogramma di una trama.</span><span class="sxs-lookup"><span data-stu-id="cdc97-104">Represents a histogram of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc97-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdc97-105">Syntax</span></span>


```C++
} PixEngineHistogram;
```

## <a name="members"></a><span data-ttu-id="cdc97-106">Members</span><span class="sxs-lookup"><span data-stu-id="cdc97-106">Members</span></span>

<span data-ttu-id="cdc97-107">**horizontalMin**</span><span class="sxs-lookup"><span data-stu-id="cdc97-107">**horizontalMin**</span></span>  
<span data-ttu-id="cdc97-108">Valori minimi per ognuno dei componenti X, Y, Z e W nell'asse orizzontale (dominio) dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="cdc97-108">The minimum values for each of the X, Y, Z, and W components in the horizontal axis (domain) of the histogram.</span></span>

<span data-ttu-id="cdc97-109">**horizontalMax**</span><span class="sxs-lookup"><span data-stu-id="cdc97-109">**horizontalMax**</span></span>  
<span data-ttu-id="cdc97-110">Valori massimi per ognuno dei componenti X, Y, Z e W nell'asse orizzontale (dominio) dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="cdc97-110">The maximum values for each of the X, Y, Z, and W components in the horizontal axis (domain) of the histogram.</span></span>

<span data-ttu-id="cdc97-111">**verticalMin**</span><span class="sxs-lookup"><span data-stu-id="cdc97-111">**verticalMin**</span></span>  
<span data-ttu-id="cdc97-112">Valori minimi per ognuno dei componenti X, Y, Z e W nell'asse verticale (intervallo) dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="cdc97-112">The minimum values for each of the X, Y, Z, and W components in the vertical axis (range) of the histogram.</span></span>

<span data-ttu-id="cdc97-113">**verticalMax**</span><span class="sxs-lookup"><span data-stu-id="cdc97-113">**verticalMax**</span></span>  
<span data-ttu-id="cdc97-114">Valori massimi per ognuno dei componenti X, Y, Z e W nell'asse verticale (intervallo) dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="cdc97-114">The maximum values for each of the X, Y, Z, and W components in the vertical axis (range) of the histogram.</span></span>

<span data-ttu-id="cdc97-115">**dataLength**</span><span class="sxs-lookup"><span data-stu-id="cdc97-115">**dataLength**</span></span>  
<span data-ttu-id="cdc97-116">Numero di campioni considerati nell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="cdc97-116">The number of samples considered in the histogram.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc97-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdc97-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cdc97-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdc97-118">Header</span></span></p></td><td><span data-ttu-id="cdc97-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="cdc97-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



