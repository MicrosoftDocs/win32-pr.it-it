---
description: Rappresenta le informazioni su un file di codice sorgente.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura SourceFileInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3e0528e61e830872a3e3b1c0555e541fc41d9d39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481989"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span data-ttu-id="1f6f2-103"><span id="vspixengine.sourcefileinfo"></span>Struttura SourceFileInfo</span><span class="sxs-lookup"><span data-stu-id="1f6f2-103"><span id="vspixengine.sourcefileinfo"></span>SourceFileInfo structure</span></span>

<span data-ttu-id="1f6f2-104">Rappresenta le informazioni su un file di codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="1f6f2-104">Represents information about a source code file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f6f2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f6f2-105">Syntax</span></span>


```C++
} SourceFileInfo;
```

## <a name="members"></a><span data-ttu-id="1f6f2-106">Members</span><span class="sxs-lookup"><span data-stu-id="1f6f2-106">Members</span></span>

<span data-ttu-id="1f6f2-107">**fileName**</span><span class="sxs-lookup"><span data-stu-id="1f6f2-107">**fileName**</span></span>  
<span data-ttu-id="1f6f2-108">Stringa COM che costituisce il FilePath del file di origine associato.</span><span class="sxs-lookup"><span data-stu-id="1f6f2-108">A COM string comtaining the filepath of the associated source file.</span></span>

<span data-ttu-id="1f6f2-109">**checksumByteCount**</span><span class="sxs-lookup"><span data-stu-id="1f6f2-109">**checksumByteCount**</span></span>  
<span data-ttu-id="1f6f2-110">Numero di byte nel checksum.</span><span class="sxs-lookup"><span data-stu-id="1f6f2-110">The number of bytes in the checksum.</span></span> <span data-ttu-id="1f6f2-111">Quando checkSumAlgorithm è uguale a CHECKSUMALGORITHM:: MD5, checkSumByteCount è 16.</span><span class="sxs-lookup"><span data-stu-id="1f6f2-111">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::md5, checkSumByteCount is 16.</span></span> <span data-ttu-id="1f6f2-112">Quando checkSumAlgorithm è uguale a CHECKSUMALGORITHM:: SHA1, checkSumByteCount è 20.</span><span class="sxs-lookup"><span data-stu-id="1f6f2-112">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::sha1, checkSumByteCount is 20.</span></span>

<span data-ttu-id="1f6f2-113">**checkSumAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="1f6f2-113">**checkSumAlgorithm**</span></span>  
<span data-ttu-id="1f6f2-114">Specifica l'algoritmo utilizzato per generare il checksum del file.</span><span class="sxs-lookup"><span data-stu-id="1f6f2-114">Specifies the algorithm used to generate the checksum of the file.</span></span> <span data-ttu-id="1f6f2-115">Gli algoritmi supportati sono MD5 e SHA1.</span><span class="sxs-lookup"><span data-stu-id="1f6f2-115">Supported algorithms are MD5 and SHA1.</span></span> <span data-ttu-id="1f6f2-116">Per ulteriori informazioni, vedere l'enumerazione CHECKSUMALGORITHM.</span><span class="sxs-lookup"><span data-stu-id="1f6f2-116">For more information, see the CHECKSUMALGORITHM enum.</span></span>

<span data-ttu-id="1f6f2-117">**checkSumFirstPart**</span><span class="sxs-lookup"><span data-stu-id="1f6f2-117">**checkSumFirstPart**</span></span>  
<span data-ttu-id="1f6f2-118">Prima parte a 8 byte del checksum.</span><span class="sxs-lookup"><span data-stu-id="1f6f2-118">The first 8 byte portion of the checksum.</span></span>

<span data-ttu-id="1f6f2-119">**checkSumSecondPart**</span><span class="sxs-lookup"><span data-stu-id="1f6f2-119">**checkSumSecondPart**</span></span>  
<span data-ttu-id="1f6f2-120">Parte secondo 8 byte del checksum.</span><span class="sxs-lookup"><span data-stu-id="1f6f2-120">The second 8 byte portion of the checksum.</span></span>

<span data-ttu-id="1f6f2-121">**checkSumThirdPart**</span><span class="sxs-lookup"><span data-stu-id="1f6f2-121">**checkSumThirdPart**</span></span>  
<span data-ttu-id="1f6f2-122">Terza parte del checksum a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="1f6f2-122">The third 8 byte portion of the checksum.</span></span>

<span data-ttu-id="1f6f2-123">**checkSumFourthPart**</span><span class="sxs-lookup"><span data-stu-id="1f6f2-123">**checkSumFourthPart**</span></span>  
<span data-ttu-id="1f6f2-124">Quarta parte di 8 byte del checksum.</span><span class="sxs-lookup"><span data-stu-id="1f6f2-124">The fourth 8 byte portion of the checksum.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f6f2-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f6f2-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1f6f2-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f6f2-126">Header</span></span></p></td><td><span data-ttu-id="1f6f2-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1f6f2-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



