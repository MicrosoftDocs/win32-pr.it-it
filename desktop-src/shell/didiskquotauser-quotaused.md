---
description: Ottiene l'utilizzo corrente del disco dell'utente, in byte.
title: DiDiskQuotaUser.QuotaUsed - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3e3ade59-b925-4ff5-ae7e-ed97eff506c7
ms.openlocfilehash: a08d7579ad4de51fbc88b7091f2f906ace838883
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841572"
---
# <a name="didiskquotauserquotaused-property"></a><span data-ttu-id="0bbb9-103">DiDiskQuotaUser.QuotaUsed - proprietà</span><span class="sxs-lookup"><span data-stu-id="0bbb9-103">DIDiskQuotaUser.QuotaUsed property</span></span>

<span data-ttu-id="0bbb9-104">Ottiene l'utilizzo corrente del disco dell'utente, in byte.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-104">Gets the user's current disk usage, in bytes.</span></span>

<span data-ttu-id="0bbb9-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bbb9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0bbb9-106">Syntax</span></span>


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a><span data-ttu-id="0bbb9-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0bbb9-107">Property value</span></span>

<span data-ttu-id="0bbb9-108">Valore **Integer** impostato sulla quantità di spazio su disco attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-108">The **Integer** value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="0bbb9-109">Se la compressione file NTFS è abilitata, **QuotaUsed** riflette la quantità di spazio su disco necessaria per i dati in uno stato non compresso.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-109">If NTFS file compression is enabled, **QuotaUsed** reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bbb9-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0bbb9-110">Requirements</span></span>



| <span data-ttu-id="0bbb9-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bbb9-111">Requirement</span></span> | <span data-ttu-id="0bbb9-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0bbb9-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bbb9-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bbb9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0bbb9-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0bbb9-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0bbb9-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bbb9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0bbb9-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0bbb9-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0bbb9-117">DLL</span><span class="sxs-lookup"><span data-stu-id="0bbb9-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bbb9-118"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="0bbb9-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bbb9-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0bbb9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bbb9-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="0bbb9-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="0bbb9-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="0bbb9-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="0bbb9-122">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="0bbb9-122">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> <dt>

[<span data-ttu-id="0bbb9-123">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="0bbb9-123">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




