---
description: Ottiene l'utilizzo del disco corrente dell'utente, in byte.
title: Proprietà DIDiskQuotaUser. QuotaUsed
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
ms.openlocfilehash: 7d5068e6f80fd2b0b435d04583e99da929e17fce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128447"
---
# <a name="didiskquotauserquotaused-property"></a><span data-ttu-id="71541-103">Proprietà DIDiskQuotaUser. QuotaUsed</span><span class="sxs-lookup"><span data-stu-id="71541-103">DIDiskQuotaUser.QuotaUsed property</span></span>

<span data-ttu-id="71541-104">Ottiene l'utilizzo del disco corrente dell'utente, in byte.</span><span class="sxs-lookup"><span data-stu-id="71541-104">Gets the user's current disk usage, in bytes.</span></span>

<span data-ttu-id="71541-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="71541-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="71541-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71541-106">Syntax</span></span>


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a><span data-ttu-id="71541-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="71541-107">Property value</span></span>

<span data-ttu-id="71541-108">Valore **intero** impostato sulla quantità di spazio su disco attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="71541-108">The **Integer** value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="71541-109">Se la compressione dei file NTFS è abilitata, **QuotaUsed** riflette la quantità di spazio su disco necessaria per i dati in uno stato non compresso.</span><span class="sxs-lookup"><span data-stu-id="71541-109">If NTFS file compression is enabled, **QuotaUsed** reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="71541-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71541-110">Requirements</span></span>



| <span data-ttu-id="71541-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="71541-111">Requirement</span></span> | <span data-ttu-id="71541-112">Valore</span><span class="sxs-lookup"><span data-stu-id="71541-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71541-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71541-113">Minimum supported client</span></span><br/> | <span data-ttu-id="71541-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="71541-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71541-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71541-115">Minimum supported server</span></span><br/> | <span data-ttu-id="71541-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="71541-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="71541-117">DLL</span><span class="sxs-lookup"><span data-stu-id="71541-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71541-118"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="71541-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71541-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71541-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71541-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="71541-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="71541-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="71541-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="71541-122">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="71541-122">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> <dt>

[<span data-ttu-id="71541-123">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="71541-123">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




